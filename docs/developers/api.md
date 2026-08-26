# Data Manager API

Access to resources in Data Manager via a RESTful API.

!!! info "API endpoints"
    The download API provides endpoints to fetch the raw data of a measurement, including the
    listing of its files and the download of single files, which supports resumable range requests.

## Swagger API docs

Detailed API documentation is available via Swagger UI and [hosted on the web service](https://download.qbic.uni-tuebingen.de/swagger-ui/index.html).

!!! info "Language-agnostic client code"
    The API is described by an [OpenAPI](https://www.openapis.org/) specification that is also
    published by the web service. This specification serves as the **single source of truth** for the
    API contract (including the model schemas, e.g. the manifest used for raw data downloads). Instead
    of hardcoding the schema yourself, you can feed the OpenAPI document into an OpenAPI/JSON-Schema
    code generator of your choice to generate typed client models in your programming language. You
    can retrieve the machine-readable specification directly from the
    [OpenAPI document](https://download.qbic.uni-tuebingen.de/v3/api-docs).

## Authentication

All download endpoints are secured with a [personal access token][PAT], which must be provided in the
`Authorization` header, prefixed with `Bearer `:

```bash
curl -H "Authorization: Bearer <ACCESS_TOKEN>" <ENDPOINT_URL>
```

### List the files of a measurement (manifest)

`GET /measurements/{measurementId}/files`

Returns a JSON manifest describing the files belonging to a measurement in a **stable order**.
The manifest contains for each file its **index**, which is used to address the file during download,
as well as a ready-to-use download URL in its `_links` section.

Field-level details (types, descriptions and examples) are documented in the
[Swagger UI](https://download.qbic.uni-tuebingen.de/swagger-ui/index.html) /
[OpenAPI document](https://download.qbic.uni-tuebingen.de/v3/api-docs), which serve as the single
source of truth for this schema.

### Download a single file

`GET /measurements/{measurementId}/files/{index}`

Downloads a single file of a measurement, addressed by the zero-based `index` within the manifest.
The endpoint supports **resumable range requests** via the `Range` header, so partially downloaded
files can be resumed and large downloads can be split into chunks.

## Deprecated endpoint

!!! danger "Discontinued soon: download a measurement as archive"
    The endpoint `GET /measurements/{measurementId}` that bundles the whole dataset into a single
    ZIP archive is **deprecated** and will be **discontinued soon**. It should no longer be used for
    new integrations and will stop working without further notice. Creating a ZIP archive on the
    server for huge datasets caused severe load on the production infrastructure.

    **Please migrate to the file-based [download workflow](../rawdata/raw_data_download.md) instead.** This
    lists the files of a measurement and downloads them individually, scales to datasets of any size
    and allows resuming interrupted downloads.

[PAT]: ../rawdata/raw_data_download.md#personal-access-token