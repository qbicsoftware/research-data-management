# Download Raw Data

We show how to run the download via the two popular command line clients [cURL](https://curl.se/docs/manpage.html) and [GNU Wget](https://www.gnu.org/software/wget/).
Of course, you can use any other software that supports HTTP.

Keep in mind that you need to be [granted access](../project/project_access.md)
by the project owner to download the associated measurement data.

The commands contain two placeholders, where you have to provide your custom input:

- *ACCESS_TOKEN*: your generated [personal access token](raw_data_download_create_pat.md)
- *MEASUREMENT_URL*: the [URL](raw_data_download_acquire_urls.md) associated with the data of the measurement

=== "curl"
    
    ``` bash
    curl -OJ -H "Authorization: Bearer <ACCESS_TOKEN>" <MEASUREMENT_URL>
    ```


=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer <ACCESS_TOKEN>" <MEASUREMENT_URL>
    ```


To download multiple measurements using one command, you can provide a file containing one measurement URL per line (as in the one you can download in the raw data summary!).
```txt
<MEASUREMENT_URL_1>
<MEASUREMENT_URL_2>
```

The corresponding commands need to be adapted accordingly.

=== "curl"
    
    ``` bash
    curl --remote-name-all -OJ -H "Authorization: Bearer <ACCESS_TOKEN>" $(cat <file-with-urls>)
    ```


=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer <ACCESS_TOKEN>" -i <file-with-urls>
    ```
