# Download datasets

We show how to run the download via the two popular command line clients [cURL](https://curl.se/docs/manpage.html) and [GNU Wget](https://www.gnu.org/software/wget/).

Of course, you can use any other software that supports HTTP.

The commands contain two placeholders, where you have to provide your custom input:

- *ACCESS_TOKEN*: your generated personal access token
- *MEASUREMENT_ID*: the id of the measurement of interest to download

=== "curl"
    
    ``` bash
    curl -H "Authorization: Bearer <ACCESS_TOKEN>" -O https://rdm.qbic/download/measurements/<MEASUREMENT_ID> 
    ```

=== "wget"

    ``` bash
    wget -H "Authorization: Bearer <ACCESS_TOKEN>" https://rdm.qbic/download/measurements/measurements/<MEASUREMENT_ID>
    ```
