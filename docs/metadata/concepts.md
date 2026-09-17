# Metadata glossary

This glossary describes every metadata field in the Data Manager. Use it as a reference when filling in registration templates or interpreting exported data.

## Quick reference

| Section | Description |
|---|---|
| [User](#user) | Account metadata and authentication |
| [Project](#project) | Project contacts, funding, and objectives |
| [Terminology](#terminology) | Ontology terms used in experiments and samples |
| [Experiment](#experiment) | Experimental design metadata |
| [Sample](#sample) | Sample and batch metadata |
| [Measurement](#measurement) | Genomics and proteomics measurement metadata |
| [Raw data](#raw-data) | Upload and download metadata |

### User

Check our documentation to find out how
to [register](../user/user_registration.md) and [edit](../user/user_edit.md) your account.

The following concepts are associated with a user account.

| Concept           | Example                         | Mandatory                  | Type                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                                   |
|-------------------|---------------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Full name         | Jane Doe                        | <span title="Yes">✅</span> | Text, divided by a singular space <br/>into first and last name                                                                                                                                    | <details class="info">First and last name of the user<summary>View Description</summary></details>                                                                                                                                                                                                                            |
| Oidc id           | 0009-0006-<br/>0929-9338        | <span title="Yes">✅</span> | Text, dependent on the [oidc](https://openid.net/developers/how-connect-works/) issuer (e.g. [ORCID](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier))  | <details class="info">Unique ID identifying the account within the [OIDC](https://openid.net/developers/how-connect-works/) provider (e.g. [ORCID](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier))<summary>View Description</summary></details>                                  |
| Oidc issuer       | https://www.orcid.org           | <span title="Yes">✅</span> | Link, dependent on the [oidc](https://openid.net/developers/how-connect-works/) issuer (e.g. [ORCID](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier)) | <details class="info">[OIDC](https://openid.net/developers/how-connect-works/) issuer enabling the [OAuth](https://datatracker.ietf.org/doc/html/rfc6749) process (e.g. via [ORCID](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier))<summary>View Description</summary></details> |
| Registration date | 2025-04-28<br/> 08:24:25.000000 | <span title="Yes">✅</span> | Date                                                                                                                                                                                               | <details class="info">Timestamp when the account was created within the system<summary>View Description</summary></details>                                                                                                                                                                                                   |
| User email        | Jane.Doe@<br/>example.mail      | <span title="Yes">✅</span> | Text, validated against [RFC 5322](https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification                                                        | <details class="info">Email address associated with the account<summary>View Description</summary></details>                                                                                                                                                                                                                  |
| User name         | JaneDoe                         | <span title="Yes">✅</span> | Text                                                                                                                                                                                               | <details class="info">Unique name specified for the account<summary>View Description</summary></details>                                                                                                                                                                                                                      |

#### Personal access token

!!! warning
    Personal access tokens are used as app credentials. They are connected to the user that
    created them and must not be shared.

Check out our documentation to find out how
to [generate](../rawdata/raw_data_download.md#generate-a-token)
and [manage](../rawdata/raw_data_download.md#manage-tokens) your personal access tokens.

### Project

Visit the [documentation](../project/project_introduction.md)
to find out how to [register](../project/project_registration.md)
and [edit](../project/project_edit.md) a project.
<br/>Additionally, it outlines how to grant or revoke [access](../project/project_access.md) to your
project for other users.

The following concepts are associated with a project.

| Concept                              | Example                                                                     | Mandatory                  | Type                                                                                                                                        | Description                                                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id                                   | Q2ABCD                                                                      | <span title="Yes">✅</span> | Text, always starts with 'Q2' <br/>and has a total length of 6.                                                                             | <details class="info">Human-readable unique project identifier<summary>View Description</summary></details>          |
| Modification date                    | 2025-04-28<br/> 08:24:25.000000                                             | <span title="Yes">✅</span> | Date                                                                                                                                        | <details class="info">Timestamp when the project was last modified<summary>View Description</summary></details>                     |
| Objective                            | Investigating the substance<br/> of interest with<br/> XXX to determine YYY | <span title="Yes">✅</span> | Text, with a maximum length of 2000 characters                                                                                              | <details class="info">Objective detailing the purpose and goal of the project<summary>View Description</summary></details>          |
| Principal investigator full name     | Jane Doe                                                                    | <span title="Yes">✅</span> | Text, divided by a singular space <br/>into first and last name                                                                             | <details class="info">Full name of the principal investigator handling the project<summary>View Description</summary></details>     |
| Principal investigator email address | Jane.Doe@<br/>example.mail                                                  | <span title="Yes">✅</span> | Text, validated against [RFC 5322](https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification | <details class="info">Email address of the principal investigator handling the project<summary>View Description</summary></details> |
| Project manager full name            | Alex Smith                                                                  | <span title="Yes">✅</span> | Text, divided by a singular space <br/>into first and last name                                                                             | <details class="info">Full name of the project manager handling the project<summary>View Description</summary></details>            |
| Project manager email address        | Alex.Smith@<br/>example.mail                                                | <span title="Yes">✅</span> | Text, validated against [RFC 5322](https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification | <details class="info">Email address of the project manager handling the project<summary>View Description</summary></details>        |
| Title                                | Analysis of the transcriptome<br/> of liver cancer sample                   | <span title="Yes">✅</span> | Text                                                                                                                                        | <details class="info">Clear and concise title of the project<summary>View Description</summary></details>                           |
| Grant name                           | DFG                                                                         | <span title="No">❌</span>  | Text                                                                                                                                        | <details class="info">Name of the grant funding the project<summary>View Description</summary></details>                            |
| Grant id                             | 213896434                                                                   | <span title="No">❌</span>  | Text                                                                                                                                        | <details class="info">Unique ID identifying the grant funding the project<summary>View Description</summary></details>              |
| Responsible person full name         | Taylor Brown                                                                | <span title="No">❌</span>  | Text, divided by a singular space <br/>into first and last name                                                                             | <details class="info">Full name of the person responsible for the project<summary>View Description</summary></details>              |
| Responsible person email address     | Taylor.Brown@<br/>example.mail                                              | <span title="No">❌</span>  | Text, validated against [RFC 5322](https://www.rfc-editor.org/rfc/rfc5322)<br/> format specification | <details class="info">Email address of the person responsible for the project<summary>View Description</summary></details>          |

#### Offer

Visit
the [documentation](../project/project_edit.md) to find out how
to [upload](../project/project_edit.md#offer-upload)
and [edit](../project/project_edit.md#offer-upload) your offer file.

The following concepts are associated with an offer file.

| Concept | Example          | Mandatory                  | Type    | Description                                                                                                  |
|---------|------------------|----------------------------|---------|--------------------------------------------------------------------------------------------------------------|
| Name    | Q2ABCD_Offer.pdf | <span title="Yes">✅</span> | Text    | <details class="info">Filename of the uploaded offer<summary>View Description</summary></details>            |
| Signed  | yes/no           | <span title="Yes">✅</span> | Boolean | <details class="info">Uploaded offer was signed by the customer<summary>View Description</summary></details> |

### Experiment

Visit our [documentation](../experiment/experiment_introduction.md) to find out how
to [create](../experiment/experiment_creation.md)
and [edit](../experiment/experiment_creation.md) an experiment.

The following concepts are associated with an experiment.

| Concept                | Example                                                                             | Mandatory                  | Type                                                                                                         | Description                                                                                                                                                                        |
|------------------------|-------------------------------------------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analytes               | BAO:0000270                                                                         | <span title="Yes">✅</span> | List of Identifier, <br/>validated against the [W3C](https://www.w3.org/TR/curie/) <br/>format specification | <details class="info">One or more substances or compounds of interest, whose expression changes are of interest within the experiment<summary>View Description</summary></details> |
| Biological replicates  | 20                                                                                  | <span title="Yes">✅</span> | Number                                                                                                       | <details class="info">Number of biologically distinct samples subjected to the same treatment during the experiment<summary>View Description</summary></details>                   |
| Experimental groups    | control, treatment_cohort_1                                                         | <span title="Yes">✅</span> | List of [Experimental Groups](concepts.md#experimental-groups)                                               | <details class="info">Group of subjects exposed to a unique combination (condition) of experimental variables<summary>View Description</summary></details>                         |
| Experimental variables | temperature, time                                                                   | <span title="Yes">✅</span> | List of [Experimental Variables](concepts.md#experimental-variables)                                         | <details class="info">An experimental factor defined to observe its effect on the subjects of an experiment<summary>View Description</summary></details>                          |
| Modification date      | 2025-04-28<br/> 08:24:25.000000                                                     | <span title="Yes">✅</span> | Date                                                                                                         | <details class="info">Timestamp when the experiment was last modified<summary>View Description</summary></details>                                                                 |
| Name                   | Pilot Experiment                                                                    | <span title="Yes">✅</span> | Text                                                                                                         | <details class="info">Unique name of the experiment<summary>View Description</summary></details>                                                                                   |
| Specimen               | NCIT:C12392                                                                         | <span title="Yes">✅</span> | List of Identifier, <br/>validated against the [W3C](https://www.w3.org/TR/curie/) <br/>format specification | <details class="info">One or more specific parts of the species from which the analytes are collected<summary>View Description</summary></details>                                |
| Species                | NCBITaxon:9606                                                                      | <span title="Yes">✅</span> | List of Identifier, <br/>validated against the [W3C](https://www.w3.org/TR/curie/) <br/>format specification | <details class="info">One or more organisms from which the samples were collected<summary>View Description</summary></details>                                                    |
| Confounding variables  | Varies. See [here](../experiment/confounding-variables.md) <br/>for more information | <span title="No">❌</span>  | List of [Confounding Variables](concepts.md#confounding-variables)                                           | <details class="info">A variable possibly influencing independent and dependent experimental variables<summary>View Description</summary></details>                               |

#### Experimental variables

Visit our [documentation](../experiment/experiment_introduction.md) to find out how
to [create](../experiment/experiment_creation.md#define-experimental-variables)
and [edit](../experiment/experiment_creation.md#define-experimental-variables) your experimental
variables.

The following concepts are associated with an experimental variable.

| Concept | Example     | Mandatory                  | Type          | Description                                                                                                                                   |
|---------|-------------|----------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Levels  | 0, 10, 100  | <span title="Yes">✅</span> | List of Texts | <details class="info">One or more specific expression settings to which the variable can be set<summary>View Description</summary></details> |
| Name    | Temperature | <span title="Yes">✅</span> | Text          | <details class="info">Unique name of the experimental variable<summary>View Description</summary></details>                                   |
| Unit    | °C          | <span title="No">❌</span>  | Text          | <details class="info">Measurement unit representing the specific setting of the variable<summary>View Description</summary></details>         |

#### Experimental groups

Visit our [documentation](../experiment/experiment_introduction.md) to find out how
to [create](../experiment/experiment_creation.md#define-experimental-groups)
and [edit](../experiment/experiment_creation.md#define-experimental-groups) your experimental
groups.

The following concepts are associated with an experimental group.

| Concept               | Example                          | Mandatory                  | Type                                                                 | Description                                                                                                                                                      |
|-----------------------|----------------------------------|----------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Biological replicates | 20                               | <span title="Yes">✅</span> | Number                                                               | <details class="info">Number of biologically distinct samples subjected to the same treatment during the experiment<summary>View Description</summary></details> |
| Condition             | control, <br/>treatment_cohort_1 | <span title="Yes">✅</span> | List of [Experimental Variables](concepts.md#experimental-variables) | <details class="info">Unique combination of experimental variables<summary>View Description</summary></details>                                                  |

#### Confounding variables

Visit our [documentation](../experiment/confounding-variables.md) to find out how
to [define](../experiment/confounding-variables.md#define-a-confounding-variable)
and [rename](../experiment/confounding-variables.md#rename-a-variable) your confounding
variables.

Values for confounding variables can be provided per [sample](#sample) and are defined in the
experiment.

| Concept | Example    | Mandatory                  | Type | Description                                                                                                      |
|---------|------------|----------------------------|------|------------------------------------------------------------------------------------------------------------------|
| Name    | Time       | <span title="Yes">✅</span> | Text | <details class="info">Unique name of the confounding variable<summary>View Description</summary></details>      |
| Values  | [6pm, 8pm] | <span title="No">❌</span>  | List | <details class="info">Possible values of the confounding variable<summary>View Description</summary></details> |

### Terminology

Visit our documentation to find out how
to [search](../ontology_search/ontology_search_introduction.md)
for your terminology of interest.

The following concepts are associated with the terminology terms.

| Concept                  | Example                                                                               | Mandatory                  | Type                                                                                                                         | Description                                                                                                                       |
|--------------------------|---------------------------------------------------------------------------------------|----------------------------|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Class IRI                | http://purl.obolibrary.org/obo/NCIT_C105979                                           | <span title="Yes">✅</span> | Identifier                                                                                                                   | <details class="info">Unique resource identifier for the term<summary>View Description</summary></details>                        |
| Description              | A protein complex <br/>that plays a role <br/>in neurotransmitter-gated ion transport | <span title="Yes">✅</span> | Text                                                                                                                         | <details class="info">Description providing explanation for the term<summary>View Description</summary></details>                 |
| Label                    | 5-HT3 Receptor                                                                        | <span title="Yes">✅</span> | Text                                                                                                                         | <details class="info">Common human-readable label of the term<summary>View Description</summary></details>                        |
| Name                     | NCIT:C105979                                                                          | <span title="Yes">✅</span> | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification | <details class="info">The OBO-style identifier, usually in the form PREFIX:ID<summary>View Description</summary></details>        |
| Terminology term IRI     | http://purl.obolibrary.org/obo/ncbitaxon.owl                                          | <span title="Yes">✅</span> | Identifier                                                                                                                   | <details class="info">Unique resource identifier for the ontology providing the term<summary>View Description</summary></details> |
| Terminology term version | http://purl.obolibrary.org/obo/ncbitaxon/2023-09-19/ncbitaxon.owl                     | <span title="Yes">✅</span> | Identifier                                                                                                                   | <details class="info">Specific version of the ontology providing the term<summary>View Description</summary></details>            |

For more information check the documentation of
the [ontology service API](https://terminology.tib.eu/ts/).

### Sample

Visit our documentation to find out how
to [register](../batch/sample-batch.md#creating-and-registering-sample-batches)
and [edit](../batch/sample-batch.md#editing-sample-batches) your batches and samples.

The following concepts are associated with a sample.

| Concept               | Example                            | Mandatory                  | Type                                                                                                                                                                                | Description                                                                                                                                                                                                                   |
|-----------------------|------------------------------------|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analysis method       | PROTEOMICS                         | <span title="Yes">✅</span> | Enumeration                                                                                                                                                                         | <details class="info">The test performed on samples for the purpose of finding and measuring chemical substances<summary>View Description</summary></details>                                                                |
| Analyte               | BAO:0000270                        | <span title="Yes">✅</span> | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                        | <details class="info">The chemical substance extracted from the biological material that is identified and measured. Selection from the ones defined within the experiment<summary>View Description</summary></details>       |
| Condition             | Temperature: 0°C; <br/>Time: 100s; | <span title="Yes">✅</span> | Number of the [Experimental Group](concepts.md#experimental-groups) in question                                                                                                     | <details class="info">Condition to which the sample was subjected. Selectable from the experimental groups within the experiment with each variable separated by a semicolon<summary>View Description</summary></details> |
| Label                 | Lab_Id_01                          | <span title="Yes">✅</span> | Text                                                                                                                                                                                | <details class="info">Common human-readable name of the sample. Can also be an internal lab identifier<summary>View Description</summary></details>                                                                              |
| Sample id             | Q2ABCD001AA                        | <span title="Yes">✅</span> | Text, beginning with the [project id](concepts.md#project) <br/>followed by the running number of samples <br/>within the project and ending with randomly generated unique letters | <details class="info">Human-readable unique sample ID, automatically assigned by the Data Manager<summary>View Description</summary></details>                                                                                |
| Species               | NCBITaxon:9606                     | <span title="Yes">✅</span> | Identifier, structured as prefix:reference as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                             | <details class="info">Scientific name of the organism(s) from which the biological material is derived. Selection from the ones defined within the experiment<summary>View Description</summary></details>                   |
| Specimen              | NCIT:C12392                        | <span title="Yes">✅</span> | Identifier, structured as prefix:reference as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                             | <details class="info">Name of the biological material from which the analytes would be extracted. Selection from the ones defined within the experiment<summary>View Description</summary></details>                          |
| Biological replicate  | Mouse_WT_1                         | <span title="No">❌</span>  | Text                                                                                                                                                                                | <details class="info">Specify if the samples belong to the same biological source within your experiment<summary>View Description</summary></details>                                                                        |
| Comment               | Redone QC                          | <span title="No">❌</span>  | Text                                                                                                                                                                                | <details class="info">Free text, can contain any notes related to a specific sample in question<summary>View Description</summary></details>                                                                                  |
| Confounding variables | color: red, location: labA         | <span title="No">❌</span>  | List of key-value pairs                                                                                                                                                             | <details class="info">Confounding variables are a good way to annotate measured variables that are suspected to have an influence on your dependent variable<summary>View Description</summary></details>                    |

Additional information can be found in the **Property Information** tab within the sample
registration [template sheet](templates/sample-metadata-template.xlsx).

#### Batch

!!! info
    A batch is a group of samples processed together under the same
    experimental conditions. This is done to document and minimise technical variation.

The following concepts are associated with a sample batch.

| Concept           | Example                         | Mandatory                  | Type   | Description                                                                                                                                                                                                           |
|-------------------|---------------------------------|----------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modification date | 2025-04-28<br/> 08:24:25.000000 | <span title="Yes">✅</span> | Date   | <details class="info">Timestamp when the batch was last modified<summary>View Description</summary></details>                                                                                                         |
| Name              | Pxp_Analysis_Trial_1            | <span title="Yes">✅</span> | Text   | <details class="info">Common human-readable label of the batch<summary>View Description</summary></details>                                                                                                           |
| Registration date | 2025-04-28<br/> 08:24:25.000000 | <span title="Yes">✅</span> | Date   | <details class="info">Timestamp when the batch was created within the Data Manager<summary>View Description</summary></details>                                                                                       |
| Sample count      | 20                              | <span title="Yes">✅</span> | Number | <details class="info">Number of samples contained within the batch, automatically determined by the Data Manager from the number of samples provided during registration<summary>View Description</summary></details> |

### Measurement

For detailed information visit
our [measurement documentation](../measurement/measurement_introduction.md).

#### Genomics

Visit our documentation to find out how
to [register](../measurement/measurement_registration.md)
or [edit](../measurement/measurement_edit.md) your genomics measurements.

The following concepts are associated with a genomic measurement.

| Concept            | Example                                   | Mandatory                                          | Type                                                                                                                                                            | Description                                                                                                                                                                                           |
|--------------------|-------------------------------------------|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facility           | Quantitative Biology Center               | <span title="Yes">✅</span>                         | Text                                                                                                                                                            | <details class="info">The facility's name within the organisation (group name, etc.)<summary>View Description</summary></details>                                                                     |
| Index I5           | NEBNext UDI UMI Set 1 B12 S579            | <span title="Yes">✅</span> for pooled measurements | Text                                                                                                                                                            | <details class="info">Index used for multiplexing<summary>View Description</summary></details>                                                                                                       |
| Index I7           | NEBNext UDI UMI Set 1 B12 S789            | <span title="Yes">✅</span> for pooled measurements | Text                                                                                                                                                            | <details class="info">Index used for multiplexing<summary>View Description</summary></details>                                                                                                       |
| Instrument         | OBI:0002750                               | <span title="Yes">✅</span>                         | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                    | <details class="info">Ontology identifier of the instrument that has been used for the measurement, usually in the form PREFIX:REFERENCE<summary>View Description</summary></details>                 |
| Measurement id     | NGSQ2ABCD001AA-<br/>118569093700875       | <span title="Yes">✅</span>                         | Text, beginning with the domain (NGS) prefix <br/>followed by the [sample id](concepts.md#sample), <br/>separated by a hyphen with its unique creation timestamp | <details class="info">Human-readable unique measurement ID, automatically assigned by the Data Manager, in the form NGS + SAMPLE_ID + "-" + Timestamp<summary>View Description</summary></details>   |
| Organisation IRI   | https://ror.org/03a1kwz48                 | <span title="Yes">✅</span>                         | Identifier, validated according to the structure <br/>defined by [ROR](https://ror.readme.io/docs/identifier)                                               | <details class="info">Research Organisation Registry identifier ([ROR ID](https://ror.org/)) of the organisation where the measurement was conducted<summary>View Description</summary></details> |
| Organisation label | University Tuebingen                      | <span title="Yes">✅</span>                         | Text                                                                                                                                                            | <details class="info">Human-readable name of the organisation, automatically received from ROR by the Organisation IRI<summary>View Description</summary></details>                               |
| Read type          | paired-end                                | <span title="Yes">✅</span>                         | Enumeration                                                                                                                                                     | <details class="info">The sequencing read type used to generate the sequence data<summary>View Description</summary></details>                                                                       |
| Registration date  | 2025-04-28<br/> 08:24:25.000000           | <span title="Yes">✅</span>                         | Date                                                                                                                                                            | <details class="info">Timestamp when the measurement was created within the Data Manager<summary>View Description</summary></details>                                                                       |
| Comment            | Repeated measurement <br/>after bad QC    | <span title="No">❌</span>                          | Text                                                                                                                                                            | <details class="info">Free text, can contain any notes related to a measurement in question with up to 500 characters<summary>View Description</summary></details>                                    |
| Flow cell          | S4                                        | <span title="No">❌</span>                          | Text                                                                                                                                                            | <details class="info">The flow cell type used for sequencing<summary>View Description</summary></details>                                                                                            |
| Library kit        | NEBNext Ultra II Directional RNA mRNA UMI | <span title="No">❌</span>                          | Text                                                                                                                                                            | <details class="info">The library kit employed during sequencing processing<summary>View Description</summary></details>                                                                              |
| Measurement name   | Lab_Id_01                                 | <span title="No">❌</span>                          | Text                                                                                                                                                            | <details class="info">Common human-readable name of the measurement. Can also be the internal lab identifier<summary>View Description</summary></details>                                             |
| Run protocol       | 104+19+10+104                             | <span title="No">❌</span>                          | Text                                                                                                                                                            | <details class="info">Information on how many cycles were used for each read and index during sequencing<summary>View Description</summary></details>                                                 |

Additional information can be found in the **Property Information** tab within the
genomic measurement registration [template sheet](templates/ngs_measurement_registration_sheet.xlsx).

#### Proteomics

Visit our documentation to find out how
to [register](../measurement/measurement_registration.md)
or [edit](../measurement/measurement_edit.md) your proteomics measurements.

The following concepts are associated with a proteomics measurement.

| Concept            | Example                                | Mandatory                  | Type                                                                                                                                                           | Description                                                                                                                                                                                                         |
|--------------------|----------------------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Digestion enzyme   | Trypsin                                | <span title="Yes">✅</span> | Text                                                                                                                                                           | <details class="info">Information about the enzymes used for the proteolytic step<summary>View Description</summary></details>                                                                                     |
| Digestion method   | in gel                                 | <span title="Yes">✅</span> | Enumeration                                                                                                                                                    | <details class="info">Method used to break proteins into peptides. Selectable from: "in gel", "in solution", "iST proteomics kit", "on beads"<summary>View Description</summary></details> |
| Facility           | Quantitative Biology Center            | <span title="Yes">✅</span> | Text                                                                                                                                                           | <details class="info">The facility's name within the organisation (group name, etc.)<summary>View Description</summary></details>                                                                                   |
| Instrument         | BAO:0002733                            | <span title="Yes">✅</span> | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                   | <details class="info">Ontology identifier of the instrument that has been used for the measurement<summary>View Description</summary></details>                                                                     |
| LC column          | ProteoSil_100-C18                      | <span title="Yes">✅</span> | Text                                                                                                                                                           | <details class="info">The type of column that has been used<summary>View Description</summary></details>                                                                                                           |
| Measurement id     | MSQ2ABCD001AA-<br/>118569093700875     | <span title="Yes">✅</span> | Text, beginning with the domain (MS) prefix <br/>followed by the [sample id](concepts.md#sample), <br/>separated by a hyphen with its unique creation timestamp | <details class="info">Human-readable unique measurement ID, automatically assigned by the Data Manager, in the form MS + SAMPLE_ID + "-" + Timestamp<summary>View Description</summary></details>                  |
| Organisation IRI   | https://ror.org/03a1kwz48              | <span title="Yes">✅</span> | Identifier, validated according to the structure <br/>defined by [ROR](https://ror.readme.io/docs/identifier)                                              | <details class="info">Research Organisation Registry identifier ([ROR ID](https://ror.org/)) of the organisation where the measurement was conducted<summary>View Description</summary></details>               |
| Organisation label | University Tuebingen                   | <span title="Yes">✅</span> | Text                                                                                                                                                           | <details class="info">Human-readable name of the organisation, automatically received from ROR by the Organisation IRI<summary>View Description</summary></details>                                             |
| Registration date  | 2025-04-28<br/> 08:24:25.000000        | <span title="Yes">✅</span> | Date                                                                                                                                                           | <details class="info">Timestamp when the measurement was created within the Data Manager<summary>View Description</summary></details>                                                                                     |
| Comment            | Repeated measurement <br/>after bad QC | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">Free text, can contain any notes related to a measurement in question with up to 500 characters<summary>View Description</summary></details>                                                  |
| Enrichment method  | Phosphopeptide Enrichment              | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">Enrichment of proteins or peptides of different characteristics<summary>View Description</summary></details>                                                                                 |
| Fraction name      | Fraction01                             | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">If the sample was fractionated, this label can be used to indicate which fraction was measured<summary>View Description</summary></details>                                                   |
| Injection volume   | 10                                     | <span title="No">❌</span>  | Number                                                                                                                                                         | <details class="info">The sample volume injected into the LC column in microlitres (µl)<summary>View Description</summary></details>                                                                                 |
| Label              | Heavy                                  | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">The label value for the label type that has been used<summary>View Description</summary></details>                                                                                           |
| Label type         | SILAC                                  | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">The label type that has been used to label the sample for measurement<summary>View Description</summary></details>                                                                           |
| Measurement name   | Lab_Id_01                              | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">Common human-readable name of the measurement. Can also be the internal lab identifier<summary>View Description</summary></details>                                                           |
| LCMS method        | APCI                                   | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">Laboratory-specific methods that have been used for LCMS measurement<summary>View Description</summary></details>                                                                            |
| Replicate name     | Replicate_1                            | <span title="No">❌</span>  | Text                                                                                                                                                           | <details class="info">Label to distinguish between technical replicates for repeated measurements of the same sample<summary>View Description</summary></details>                                                  |

Additional information can be found in the **Property Information** tab within the
proteomics measurement
registration [template sheet](templates/proteomics_measurement_registration_sheet.xlsx).

### Raw data

Visit our documentation to find out how to [upload](../rawdata/raw_data_upload.md)
or [download](../rawdata/raw_data_download.md) your raw data.

The following concepts are associated with a raw data dataset.

| Concept           | Example                          | Mandatory                  | Type         | Description                                                                                                                                                                   |
|-------------------|----------------------------------|----------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| File count        | 20                               | <span title="Yes">✅</span> | Number       | <details class="info">Number of files contained within the raw data upload, automatically determined by the Data Manager<summary>View Description</summary></details>         |
| File size         | 2000 MB                          | <span title="Yes">✅</span> | Text         | <details class="info">Size of all files within the raw data upload, automatically determined by the Data Manager<summary>View Description</summary></details>                 |
| File suffixes     | fastq, tar, txt                  | <span title="Yes">✅</span> | List of Text | <details class="info">List of file suffixes for all files within a raw data upload, automatically determined by the Data Manager<summary>View Description</summary></details> |
| Registration date | 2025-04-28<br/> 08:24:25.000000  | <span title="Yes">✅</span> | Date         | <details class="info">Timestamp when the raw data was uploaded within the Data Manager<summary>View Description</summary></details>                                           |


---

## See also

- [Ontology search](../ontology_search/ontology_search_introduction.md) — find standardised terms and copy their identifiers
- [Process overview](../get_started/process_overview.md) — the end-to-end Data Manager workflow
