# Download datasets

We show how to run the download via the two popular command line clients [cURL](https://curl.se/docs/manpage.html) and [GNU Wget](https://www.gnu.org/software/wget/).

Of course, you can use any other software that supports HTTP.

The commands contain two placeholders, where you have to provide your custom input:

- *ACCESS_TOKEN*: your generated personal access token
- *MEASUREMENT_ID*: the id of the measurement of interest to download

=== "curl"
    
    ``` bash
    curl -OJ -H "Authorization: Bearer <ACCESS_TOKEN>" https://download.qbic.uni-tuebingen.de/measurements/<MEASUREMENT_ID>
    ```


=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer <ACCESS_TOKEN>" https://download.qbic.uni-tuebingen.de/measurements/<MEASUREMENT_ID>
    ```


You can download multiple measurements. All you have to do is provide the URLs in separate lines.
```txt
https://download.qbic.uni-tuebingen.de/measurements/<MEASUREMENT_ID_1>
https://download.qbic.uni-tuebingen.de/measurements/<MEASUREMENT_ID_2>
```

The corresponding commands need to be adapted accordingly.

=== "curl"
    
    ``` bash
    curl --remote-name-all --parallel -OJ -H "Authorization: Bearer <ACCESS_TOKEN>" $(cat <file-with-urls>)
    ```


=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer <ACCESS_TOKEN>" -i <file-with-urls>
    ```
