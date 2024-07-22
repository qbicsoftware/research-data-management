# Raw Data Introduction

The raw data summary view shows detailed information about the raw data already [registered](raw_data_upload.md) for the measurements within your experiment.
Additionally, it enables you to generate the [URLs](#raw-data-url-generation) necessary
to start the command line based [raw data download](#download-raw-data). 

## Process

1. Create a [personal access token](#personal-access-token) (PAT)
2. Navigate to the raw data summary [view](#raw-data-navigation)
3. Acquire [download URLs](#raw-data-url-generation) for the registered measurement raw data. 
4. Start the measurement raw data [download](#download-raw-data) measurement and get a coffee :coffee:

## Personal access token

Before you can begin with downloading any data via HTTPS, you need to tell the download server
who you are. We enforce a token-based authentication (personal access token: PAT) so you are not
required to expose you password
with anyone or with any system.

!!! tip "multiple tokens"
    You can create as many tokens as you like, however consider them as a secret.

### Generate a token

First of all, navigate to your PAT overview page in your profile overview (top-right corner)

![profile menu](images/raw_data_create_pat_profile_menu.png)

You should now be able to see the PAT token overview page:

![pat overview](images/raw_data_create_pat_overview_no_pats.png)

Personal access tokens have a life-time, which can be set based on your requirements. Your token
expires automatically, there is nothing you have to do manually.

![generate token](images/raw_data_create_pat_generate_token.png)

!!! warning "Token accessibility"
    A generated token will be only visible in its raw notation once! Make sure to store it safely in
    your local password manager, you will not be able to access the token value again.

### Manage tokens

You can see your created tokens in the overview, however since they are instantly encrypted after generation,
you cannot access their raw value anymore. We encourage you to use meaningful descriptions for your tokens,
so you remember for what purpose you have created them.

![token overview](images/raw_data_create_pat_token_overview.png)

!!! danger "Token security"
    If you are unsure, if your PAT got exposed or shared with untrusted parties, delete them right
    away.

## Raw Data Navigation

To navigate to the raw data summary view start by [navigating](../project/project_introduction.md#project-navigation) to the project summary view of your project of interest.
From there [navigate](../experiment/experiment_introduction.md#experiment-navigation) into the experiment summary view of interest.
From within the experiment summary you can navigate into the raw data summary view.
To do so, click on the "Download Raw Data" tab within the experiment navigation bar on the top.
![experiment_summary.png](../experiment/images/experimental_summary.png)

This will take you to the raw data summary view
![raw_data_summary_no_data.png](images/raw_data_summary_no_data.png)

### Raw Data URL Generation

To acquire the URLS necessary for the measurement data download the following steps have to be taken:

1. Navigate to the [raw data summary view](#raw-data-navigation)
2. Select the measurements for which the raw data URLS should be generated.
   ![raw_data_download_measurement_selection.png](images/raw_data_download_URL_generation_measurement_selection.png)
3. Press the "Generate URL List" button to download a text file containing the URLs of the selected measurements
   ![raw_data_download_URL_downloaded.png](images/raw_data_download_URL_downloaded.png)

### Download Raw Data

To download the raw data for your measurements basic command line/terminal knowledge is required. 
First start by opening the command line in your operating system of choice. 

#### Open command line on Mac

Open the terminal via the spotlight search function by clicking on the magnifying glass on the top right or via pressing the command and spacebar key on your keyboard.
Input "terminal" into the text field and select the terminal application from the suggestions. 

![data_download_mac_command_line.png](images/data_download_mac_command_line.png)

#### Open command line on Windows

Click on the magnifying glass in the toolbar at the bottom of the screen. 
Input "terminal" into the search field and select the terminal application from the suggestions.

![data_download_windows_command_line.png](images/data_download_windows_command_line.png)

#### Download data via command line

We show how to run the download via the two popular command line clients [cURL](https://curl.se/docs/manpage.html) and [GNU Wget](https://www.gnu.org/software/wget/).
Of course, you can use any other software that supports HTTP.

!!! warning
    The data will be downloaded into the directory in which the command is run.
    Please ensure that it's the correct directory and there is enough space before running the download

The commands contain two placeholders, where you have to provide your custom input:

- *ACCESS_TOKEN*: your generated [personal access token](#personal-access-token)
- *MEASUREMENT_URL*: the [URL](#raw-data-url-generation) associated with the data of the measurement

=== "curl"

    ``` bash
    curl -OJ -H "Authorization: Bearer <ACCESS_TOKEN>" <MEASUREMENT_URL>
    ```

=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer <ACCESS_TOKEN>" <MEASUREMENT_URL>
    ```
For example to download the raw data associated with measurement **MSQ7645002AL-182987406699583** the commands would look as follows:

=== "curl"

    ``` bash
    curl --parallel --fail -OJ -H "Authorization: Bearer v71E00f750Z78oBW4SKs90Vrd39h98eG" https://download.qbic.uni-tuebingen.de/measurements/MSQ7645002AL-182987406699583
    ```

=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer v71E00f750Z78oBW4SKs90Vrd39h98eG"  https://download.qbic.uni-tuebingen.de/measurements/MSQ7645002AL-182987406699583
    ```

To download multiple measurements using one command, you can provide a text file containing one measurement URL per line (as in the one you can download in the raw data summary!).

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

!!! warning
    To ensure character validity in the text file, please format it in the *UTF-8* format

The easiest way to generate such a text file is to navigate into the raw data view and select the measurements for which you want to download the raw data for and click the "download url list" button.

![data_download_selected_measurements.png](images/data_download_selected_measurements.png)

This will download the text file containing the urls for the selected measurements 

![raw_data_download_text_file.png](images/raw_data_download_text_file.png)

For example to download the raw data for all measurements within the text file **download_urls.txt** the command would look as follows:

=== "curl"

    ``` bash
    curl --remote-name-all -OJ -H "Authorization: Bearer v71E00f750Z78oBW4SKs90Vrd39h98eG" $(cat /Your/awesome/path/download_urls.txt)
    ```

=== "wget"

    ``` bash
    wget --content-disposition --trust-server-names --header "Authorization: Bearer v71E00f750Z78oBW4SKs90Vrd39h98eG" -i /Your/awesome/path/download_urls.txt
    ```
