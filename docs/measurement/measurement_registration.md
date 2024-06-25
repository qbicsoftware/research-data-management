# Measurement Registration

To register measurements, start by [navigating](measurement_introduction.md#measurement-navigation) into the measurement summary view.
![measurement_summary](images/measurement_summary_no_measurements.png)
Once within the measurement summary view, measurements can be registered via the following steps:

1. [Download](#download-template) the domain specific metadata template spreadsheet
2. [Prepare](#prepare-metadata) the downloaded metadata sheet with the domain specific mandatory information
3. [Upload](#measurement-upload) the filled in measurement metadata sheet

!!! info "Project role"
    Should you not see the registration and download buttons,
    please make sure that you have been granted the "write" or "admin" role to the project by the owner/admin!

## Download Template

### Proteomics

Within this view download the proteomic specific template's _.xlsx_ file via the template component on the top right by clicking
on the download icon (down arrow).
![register_measurements_proteomics_download_template.png](images/measurement_registration_proteomics_download_template.png)

### Genomics

Within this view download the genomic specific template's xlsx file via the template component on the top right by clicking
on the download icon (down arrow).

Once downloaded open the template file in Microsoft Excel, which contains the two sheets "Property Information" and "Metadata".
![register_measurements_ngs_measurement_template.png](images/measurement_registration_ngs_measurement_template.png)

## Prepare Metadata

### Proteomics

Start by opening the downloaded proteomics template file in Microsoft Excel. It contains the two sheets "Property Information" and "Metadata".
![register_measurement_proteomics_measurement_template.png](images/measurement_registration_proteomics_measurement_template.png)

The "Property Information" Sheet provides detailed information about which properties are required and what values are permitted for each property within the sheet.
![register_measurement_proteomics_measurement_template_property_sheet.png](images/measurement_registration_proteomics_measurement_template_property_sheet.png)

Use these Guidelines to fill in the "Metadata" sheet with the mandatory necessary information for the performed measurement.
![register_measurement_proteomics_measurement_filled.png](images/measurement_registration_proteomics_measurement_filled.png)

!!! tip "Sample Id"
    You can copy the Sample IDs from the [downloadable](../batch/batch_registration.md#batch-metadata-download) batch metadata sheet

**Notes:**
Mandatory metadata properties are marked with an asterisk next to the column header

The "Instrument" column expects an ontology [CURIE](https://link.springer.com/article/10.1007/s12599-022-00744-0) of the instrument.
You can use our [ontology search](../ontology_search/ontology_search_introduction.md#ontology-search) to find the CURIE

The "Organisation Id" column expects the full [RoR Id](https://ror.org/about/) URL of the organisation.
Use the [ROR registry search](https://ror.org/search) to determine the URL of the organisation RoR Id.

Once the mandatory measurement metadata has been provided, export "Metadata" sheet into a tab seperated UTF-16BE Unicode Text (*.txt) text file. This encoding ensures that special symbols like 'μ' (think volumes in sample preparation) are correctly transferred and can be displayed with your sample information.
![register_measurement_proteomics_measurement_export.png](images/measurement_registration_proteomics_measurement_export.png)

Finally, [upload](#measurement-upload) the exported text file into the data manager application.

### Genomics

Start by opening the downloaded genomic template file in Microsoft Excel. It contains the two sheets "Property Information" and "Metadata".
![register_measurements_ngs_measurement_template.png](images/measurement_registration_ngs_measurement_template.png)

The "Property Information" Sheet provides detailed information about which properties are required and what values are permitted for each property within the sheet.
![register_measurements_ngs_measurement_template_property_sheet.png](images/measurement_registration_ngs_measurement_template_property_sheet.png)

Use these Guidelines to fill in the "Metadata" sheet with the mandatory necessary information for the performed measurement.
![register_measurement_proteomics_measurement_filled.png](images/measurement_registration_proteomics_measurement_filled.png)

!!! tip "Sample Id"
    You can copy the Sample IDs from the [downloadable](../batch/batch_registration.md#batch-metadata-download) batch metadata sheet

**Notes:**
Mandatory metadata properties are marked with an asterisk next to the column header

The "Instrument" column expects an ontology [CURIE](https://link.springer.com/article/10.1007/s12599-022-00744-0) of the instrument.
You can use our [ontology search](../ontology_search/ontology_search_introduction.md#ontology-search) to find the CURIE

The "Organisation Id" column expects the full [RoR Id](https://ror.org/about/) URL of the organisation.
Use the [ROR registry search](https://ror.org/search) to determine the URL of the organisation RoR Id.

Once the mandatory measurement metadata has been provided, export "Metadata" sheet into a tab seperated UTF-16BE Unicode Text (*.txt) text file. This encoding ensures that special symbols like 'μ' (think volumes in sample preparation) are correctly transferred and can be displayed with your sample information.
![register_measurement_proteomics_measurement_export.png](images/measurement_registration_proteomics_measurement_export.png)

Finally, [upload](#measurement-upload) the exported text file into the data manager application. 

## Measurement Upload

Once the measurement metadata has been [prepared](#prepare-metadata) according to the domain specifications, 
the exported _txt_ file can be uploaded into the data manager application. 
To start the measurement registration process press the "Register Measurements" button within the measurement summary view. 
![measurement_summary](images/measurement_summary_no_measurements.png)

This will open the measurement registration dialog with which the metadata can be registered. 
![register_measurements_upload_template.png](images/measurement_registration_upload_template.png)

Within the dialog you are able to upload your measurement files either via clicking the upload files button and selecting the files of interest in your file system
or by drag and dropping the files into the dashed box saying "drop your files here".
![register_measurements_proteomics_upload_template_filled.png](images/measurement_registration_upload_template_filled.png)

Should you have uploaded one or more wrong files, you can easily delete them via a press of the cross icon next to their respective file names

!!! warning "File constraints"
    Please adhere to the file format and maximum file size outlined in the dialog.
    Currently, we support the _txt_ or _tsv_ file formats with a maximum file size of 16Mb

The registration dialog will validate the provided information and show invalid properties in below the file name. 

Finally, upload the measurement metadata files to the experiment via pressing the "Register" button on the bottom right of the dialog.

!!! note "Measurement Id"
    During measurement registration each measurement will be assigned a unique measurement ID,
    distinguishing it from other measurement within the system.

Your uploaded measurement metadata will be shown in the grid within their domain specific tab in the measurement summary view.
![measurement_summary](images/measurement_summary_with_measurements.png)

## Measurement Metadata Download

You can download the measurement specific metadata via the "Download Metadata" button, which will download the metadata of all measurements of the **currently selected tab** in an _xlsx_ file.
![batch_registration_downloaded_metadata.png](images/measurement_registration_downloaded_metadata.png)
