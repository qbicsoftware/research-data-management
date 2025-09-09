# Data Modalities

## Quick Reference Table

| Concept                     | Description                                                                    |                           
|-----------------------------|--------------------------------------------------------------------------------|
| [User](#user)               | Learn more about the metadata of your user account and its authentication      | 
| [Project](#project)         | Information about a projects metadata such as contact, funding and objective   | 
| [Ontology](#ontology)       | Find out more about the ontology terms employed within experiments and samples | 
| [Experiment](#experiment)   | Everything related to the metadata within an experimental design               | 
| [Sample](#sample)           | Detailed information concerning the metadata of sample and batches             | 
| [Measurement](#measurement) | Everything related to NGS and PxP measurement metadata                         | 
| [Raw Data](#raw-data)       | Find out more about the metadata surrounding Data Upload and Download          | 

### User

In our documentation you can find detailed information on how
to [register](../user/user_registration.md)
and [edit](../user/user_edit.md) your account within the Data Manager.

Below you can find an overview of the information associated with a user account within the Data
Manager

| Concept           | Description                                                             | Example                              | Mandatory          | Type                                                                                                                                                     |                          
|-------------------|-------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Email             | Email address associated with the account                               | John.Doe@<br/>example.mail                | :white_check_mark: | Text, validated against [RFC5322](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification                   |
| Full name         | First and last name of the user                                         | John Doe                             | :white_check_mark: | Text, divided by a singular space <br/>into first and last name                                                                                               |
| Oidc id           | Unique Id identifying the account within the Oidc provider (e.g. Orcid) | 0009-0006-<br/>0929-9338                  | :white_check_mark: | Text, dependent on the oidc issuer (e.g. [orcid definition](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier)  |
| Oidc issuer       | Oidc Issuer enabling the oauth process (e.g. via Orcid)                 | https://www.orcid.org                | :white_check_mark: | Link,  dependent on the oidc issuer (e.g. [orcid definition](https://support.orcid.org/hc/en-us/articles/360006897674-Structure-of-the-ORCID-Identifier) |
| Registration date | Timestamp when the account was created within the system                | 2025-04-28<br/> 08:24:25.000000           | :white_check_mark: | Date                                                                                                                                                     |
| User name         | Unique name specified for the account                                   | JohnDoe                              | :white_check_mark: | Text                                                                                                                                                     |
| User id           | Unique Id associated with the user automatically assigned by the system | b1d536ce-fe29-4967-<br/>843f-2189bf971ae9 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification             |

#### Personal Access Token

Downloading your data is handled via the registration of a personal access token. Check out our
dedicated sections to find out how
to [register](../rawdata/raw_data_download.md#generate-a-token)
and [edit](../rawdata/raw_data_download.md#manage-tokens) your personal access tokens.

### Project

For detailed information visit the [project documentation](../project/project_introduction.md)
There you will find detailed information on how to [register](../project/project_registration.md)
and [edit](../project/project_edit.md) a project within the Data Manager.
Additionally, it outlines how to grant or revoke [access](../project/project_access.md) to your
project to other users within the Data Manager.

Below you can find an overview of the information associated with a project within the Data
Manager

| Concept                              | Description                                                          | Example                                                           | Mandatory          | Type                                                                                                                                         |            
|--------------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Code                                 | Human Readable unique Project Code of the project                    | Q2ABCD                                                            | :white_check_mark: | Text, always starts with 'Q2' <br/>and has a total length of 6.                                                                                   |
| Id                                   | Identifier of the project automatically assigned by the Data Manager | cdd81764-db7c-4635-<br/>b7f4-6e711b411e3c                         | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Modification date                    | Timestamp when the project was last modified                         | 2025-04-28<br/> 08:24:25.000000                                   | :white_check_mark: | Date                                                                                                                                         |
| Objective                            | Objective detailing the purpose and goal of the project              | Investigating the substance<br/> of interest with<br/> XXX to determine YYY | :white_check_mark: | Text, with a maximum length of 2000 characters                                                                                               |
| Principal investigator full name     | Full name of the principal investigator handling the project         | John Doe                                                          | :white_check_mark: | Text, divided by a singular space <br/>into first and last name                                                                                   |
| Principal investigator email address | Email address of the principal investigator handling the project     | John.Doe@<br/>example.mail                                        | :white_check_mark: | Text, validated against [RFC5322](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification       |
| ProjectManager full name             | Full name of the project manager handling the project                | Jane Doe                                                          | :white_check_mark: | Text, divided by a singular space <br/>into first and last name                                                                                   |
| ProjectManager email address         | Email address of the project manager handling the project            | Jane.Doe@<br/>example.mail                                        | :white_check_mark: | Text, validated against [RFC5322](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc5322) <br/>format specification       |
| Title                                | Clear and concise title of the project                               | Analysis of the transcriptome<br/> of liver cancer sample         | :white_check_mark: | Text                                                                                                                                         |
| Grant name                           | Name of the grant funding the project                                | DFG                                                               | :x:                | Text                                                                                                                                         |
| Grant id                             | Unique Id identifying the grant funding the project                  | 213896434                                                         | :x:                | Text                                                                                                                                         |
| ResponsiblePerson full name          | Full name of the person responsible for the project                  | Max Mustermann                                                    | :x:                | Text, divided by a singular space <br/>into first and last name                                                                                   |
| ResponsiblePerson email address      | Email address of the person responsible for the project              | Max.Mustermann@<br/>example.mail                                       | :x:                | Text, validated against [RFC5322](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc5322)<br/> format specification       |

#### Offer

For detailed information visit
the [project editing documentation](../project/project_edit.md)

There you will find detailed information on how
to [register](../project/project_edit.md#offer-upload)
and [edit](../project/project_edit.md#offer-upload) your offer file within the Data Manager.

Below you can find an overview of the information associated with an offer file within the Data
Manager.

| Concept    | Description                                                | Example                              | Mandatory          | Type                                                                                                                                         |                                         
|------------|------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Name       | Filename of the uploaded offer                             | Q2ABCD_Offer.pdf                     | :white_check_mark: | Text                                                                                                                                         |
| Project id | Identifier of the project to which this offer was uploaded | cdd81764-db7c-4635-<br/>b7f4-6e711b411e3c | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Signed     | Uploaded Offer was signed by the customer                  | yes/no                               | :white_check_mark: | Boolean                                                                                                                                      |

#### Sample QC

For detailed information visit
the [project editing documentation](../project/project_edit.md)

There you will find detailed information on how
to [register](../project/project_edit.md#quality-control-upload)
and [edit](../project/project_edit.md#quality-control-upload) your sample qc file within the Data
Manager.

Below you can find an overview of the information associated with a quality control file within the
Data Manager.

| Concept       | Description                                                  | Example                              | Mandatory          | Type                                                                                                                                         |                                                                    
|---------------|--------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Experiment id | Identifier of the Experiment to which this sample QC belongs | dfcd156d-eb17-4cb0-<br/>99e1-68c5b1683237 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Name          | Filename of the uploaded Sample QC report                    | Q2ABCD_SampleQC.pdf                  | :white_check_mark: | Text                                                                                                                                         |
| Project id    | Identifier of the project to which the QC was uploaded       | cdd81764-db7c-4635-<br/>b7f4-6e711b411e3c | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |

### Experiment

For detailed information visit
the [experiment documentation](../experiment/experiment_introduction.md)

There you will find detailed information on how to [register](../experiment/experiment_creation.md)
and [edit](../experiment/experiment_creation.md) an experiment within the Data Manager.

Below you can find an overview of the information associated with an experiment within the Data
Manager.

| Concept                | Description                                                                                                     | Example                                                                        | Mandatory          | Type                                                                                                                       |                                 
|------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------|
| Analytes               | One or more substances or compounds of interest, whose expression changes are of interest within the experiment | BAO:0000270                                                                    | :white_check_mark: | List of Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification |
| Biological replicates  | Number of biologically distinct samples subjected to the same treatment during the experiment                   | 20                                                                             | :white_check_mark: | Number                                                                                                                     |
| Experimental groups    | Group of subjects exposed to a unique combination (condition) of experimental variables                         | control, treatment_cohort_1                                                    | :white_check_mark: | List of [Experimental Groups](concepts.md#experimental-groups)                                                             |
| Experimental variables | An Experimental factor defined to observe its effect on the subjects of an experiment.                          | temperature, time                                                              | :white_check_mark: | List of [Experimental Variables](concepts.md#experimental-variables)                                                       |
| Id                     | Identifier of the experiment automatically assigned by the Data Manager                                         | dfcd156d-eb17-4cb0-<br/>99e1-68c5b1683237                                           | :white_check_mark: | Identifier, validated against [RFC4122]/https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                       |
| Modification date      | Timestamp when the experiment was last modified                                                                 | 2025-04-28<br/> 08:24:25.000000                                                     | :white_check_mark: | Date                                                                                                                       |
| Name                   | Unique name of the experiment                                                                                   | Pilot Experiment                                                               | :white_check_mark: | Text                                                                                                                       |
| Specimen               | One or more specific parts of the species from which the analytes are collected.                                | NCIT:C12392                                                                    | :white_check_mark: | List of Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification |
| Species                | One ore more Organisms from which the samples were collected                                                    | NCBITaxon:9606                                                                 | :white_check_mark: | List of Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification |
| Confounding variables  | A variable possibly influencing independent and dependent experimental variables.                               | Varies See [here](../experiment/confounding-variables.md) <br/>for more information | :x:                | List of [Confounding Variables](concepts.md#confounding-variables)                                                         |

#### Experimental Variables

For detailed information visit
the [experiment documentation](../experiment/experiment_introduction.md)

There you will find detailed information on how
to [register](../experiment/experiment_creation.md#experimental-variable-creation)
and [edit](../experiment/experiment_creation.md#experimental-variable-creation) your experimental
variables within the Data Manager.

Below you can find an overview of the information associated with an experiment variable within the
Data
Manager.

| Concept       | Description                                                                                            | Example                              | Mandatory          | Type                                                                                                                                         |                              
|---------------|--------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Id            | Running Number representing the experimental variable within the system                                | 3                                    | :white_check_mark: | Number                                                                                                                                       |
| Experiment id | Identifier of the experiment with the experimental variable automatically assigned by the Data Manager | dfcd156d-eb17-4cb0-<br/>99e1-68c5b1683237 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Levels        | One or more specific expression settings to which the variable can be set.                             | 0, 10, 100                           | :white_check_mark: | List of Texts                                                                                                                                |
| Name          | Unique name of the experimental variable                                                               | Temperature                          | :white_check_mark: | Text                                                                                                                                         |
| Unit          | Measurement Unit representing the specific setting of the variable                                     | °C                                   | :x:                | Text                                                                                                                                         |

#### Experimental Groups

For detailed information visit
the [experiment documentation](../experiment/experiment_introduction.md)

There you will find detailed information on how
to [register](../experiment/experiment_creation.md#experimental-group-creation)
and [edit](../experiment/experiment_creation.md#experimental-group-creation) your experimental
variables within the Data Manager.

Below you can find an overview of the information associated with an experiment group within the
Data
Manager.

| Concept               | Description                                                                                   | Example                              | Mandatory          | Type                                                                                                                                         |                        
|-----------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Id                    | Running Number representing the experimental group within the system                          | 3                                    | :white_check_mark: | Number                                                                                                                                       |
| Biological replicates | Number of biologically distinct samples subjected to the same treatment during the experiment | 20                                   | :white_check_mark: | Number                                                                                                                                       |
| Condition             | Unique combination of experimental variables                                                  | control, <br/>treatment_cohort_1          | :white_check_mark: | List of [Experimental Variables](concepts.md#experimental-variables)                                                                         |
| Experiment id         | Identifier of the experiment automatically assigned by the Data Manager                       | dfcd156d-eb17-4cb0-<br/>99e1-68c5b1683237 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |

#### Confounding Variables

For detailed information visit
the [experiment documentation](../experiment/confounding-variables.md)

There you will find detailed information on how
to [register](../experiment/confounding-variables.md#define-confounding-variables-in-your-experiment)
and [edit](../experiment/confounding-variables.md#rename-a-confounding-variable) your experimental
variables within the Data Manager.

Below you can find an overview of the information associated with a confounding variable within the
Data Manager.

| Concept       | Description                                                                                           | Example                              | Mandatory          | Type                                                                                                                                         |                            
|---------------|-------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Experiment id | Identifier of the experiment with the confounding variable automatically assigned by the Data Manager | dfcd156d-eb17-4cb0-<br/>99e1-68c5b1683237 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Name          | Unique name of the experimental variable                                                              | Time                                 | :white_check_mark: | Text                                                                                                                                         |

### Ontology

In our documentation you can find detailed information on how
to [search](../ontology_search/ontology_search_introduction.md#ontology-search-introduction)
for your ontology terms of interest.
Detailed information for each field can additionally be found within the documentation of
the [ontology service API](https://www.ebi.ac.uk/ols4/)

Below you can find an overview of the information associated with the ontology terms within the Data
Manager.

| Concept               | Description                                                    | Example                                                                     | Mandatory          | Type                                                                                                               |                     
|-----------------------|----------------------------------------------------------------|-----------------------------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------|
| Class IRI             | Unique resource identifier for the term                        | http://purl.obolibrary.org/obo/NCIT_C105979                                 | :white_check_mark: | Identifier                                                                                                         |
| Description           | Description providing explanation for the term                 | A protein complex <br/>that plays a role <br/>in neurotransmitter-gated ion transport | :white_check_mark: | Text                                                                                                               |
| Label                 | Common human-readable label of the term                        | 5-HT3 Receptor                                                              | :white_check_mark: | Text                                                                                                               |
| Name                  | the OBO-style identifier, usually in the form PREFIX:ID        | NCIT:C105979                                                                | :white_check_mark: | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification |
| Ontology term IRI     | Unique resource identifier for the ontology providing the term | http://purl.obolibrary.org/obo/ncbitaxon.owl                                | :white_check_mark: | Identifier                                                                                                         |
| Ontology term version | Specific Version of the ontology providing the term            | http://purl.obolibrary.org/obo/ncbitaxon/2023-09-19/ncbitaxon.owl           | :white_check_mark: | Identifier                                                                                                         |

### Sample

In our documentation you can find detailed information on how
to [register](../batch/sample-batch.md#creating-and-registering-sample-batches)
and [edit](../batch/sample-batch.md#editing-sample-batches) your batches and samples.

Below you can find an overview of the information associated with a sample within the Data
Manager. This information can also be found in the "property information" tab within the sample
registration template sheet.

| Concept              | Description                                                                                                                                                | Example                                   | Mandatory          | Type                                                                                                                                                                                                                                                                      |                        
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analysis method      | The test performed on samples for the purpose of finding and measuring chemical substances.                                                                | PROTEOMICS                                | :white_check_mark: | Enumeration, Selectable values can be found <br/>in the abbreviation field <br/>of the [AnalysisMethod](https://github.com/qbicsoftware/data-manager-app/blob/main/project-management/src/main/java/life/qbic/projectmanagement/domain/model/sample/AnalysisMethod.java) class |
| Analyte              | The chemical substance extracted from the biological material that is identified and measured. Selection from the ones defined within the experiment       | BAO:0000270                               | :white_check_mark: | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                                                                                                                   |
| Batch id             | Identifier of the batch the sample belonged to during its registration automatically assigned by the Data Manager                                          | 01422b86-407e-47e3-<br/>9cf6-093c4882d6b2 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                                                                         |
| Condition            | Condition to which the sample was subjected to. Selectable from the experimental groups within the experiment with each variable seperated by a semicolon. | Temperature: 0°C; <br/>Time: 100s;             | :white_check_mark: | Number of the [Experimental Group](concepts.md#experimental-groups) in Question                                                                                                                                                                                           |
| Id                   | Identifier of the sample automatically assigned by the Data Manager                                                                                        | 00058431-df92-48a6-<br/>891b-671d714bb723 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                                                                         |
| Label                | Common human-readable name of the sample. Can also be internal lab identifier                                                                              | Lab_Id_01                                 | :white_check_mark: | Text                                                                                                                                                                                                                                                                      |
| Sample code          | Human readable unique sample code, automatically assigned by the Data Manager                                                                              | Q2ABCD001AA                               | :white_check_mark: | Text, beginning with the [ProjectCode](concepts.md#project) <br/>followed by the running number of samples <br/>within the project and ending with randomly generated unique letters                                                                                                |
| Species              | Scientific name of the organism(s) from which the biological material is derived.  Selection from the ones defined within the experiment                   | NCBITaxon:9606                            | :white_check_mark: | Identifier, structured as prefix:reference as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                                                                                                                   |
| Specimen             | Name of the biological material from which the analytes would be extracted.       Selection from the ones defined within the experiment                    | NCIT:C12392                               | :white_check_mark: | Identifier, structured as prefix:reference as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                                                                                                                   |
| Biological Replicate | Specify if the samples belong to the same biological source within your experiment.                                                                        | "Mouse_WT_1"                              | :x:                | Text                                                                                                                                                                                                                                                                      |
| Comment              | Free Text, can contain any notes related to a specific sample in question                                                                                  | "Redone QC"                               | :x:                | Text                                                                                                                                                                                                                                                                      |

The current sample registration template sheet can be found here
[sample-metadata-template.xlsx](templates/sample-metadata-template.xlsx)

#### Batch

A batch can be defined as a group of samples processed or analyzed together under the same
experimental conditions with the aim to minimize technical variation.
Below you can find an overview of the information associated with a sample batch within the Data
Manager.

| Concept           | Description                                                                                                                                        | Example                              | Mandatory          | Type                                                                                                                                         |                         
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Id                | Identifier of the batch the sample belonged to during its registration automatically assigned by the Data Manager                                  | 01422b86-407e-47e3-<br/>9cf6-093c4882d6b2 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification |
| Modification date | Timestamp when the batch was last modified                                                                                                         | 2025-04-28<br/> 08:24:25.000000           | :white_check_mark: | Date                                                                                                                                         |
| Name              | Common human-readable label of the batch                                                                                                           | Pxp_Analysis_Trial_1                 | :white_check_mark: | Text                                                                                                                                         |
| Registration date | Timestamp when the batch was created within the Data Manager                                                                                       | 2025-04-28<br/> 08:24:25.000000           | :white_check_mark: | Date                                                                                                                                         |
| Sample count      | Number of samples contained within the batch, automatically determined by the Data Manager from the number of samples provided during registration | 20                                   | :white_check_mark: | Number                                                                                                                                       |

### Measurement

For detailed information visit
the [measurement documentation](../measurement/measurement_introduction.md)

#### Genomics

In our documentation you can find detailed information on how
to [register](../measurement/measurement_registration.md#genomics)
or [edit](../measurement/measurement_edit.md#genomics) your proteomics measurement

Below you can find an overview of the information associated with a genomic measurement within the
Data Manager. This information can also be found in the "property information" tab within the
genomic measurement
registration template sheet.

| Concept            | Description                                                                                                                         | Example                                   | Mandatory                              | Type                                                                                                                                                                                                            |  
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facility           | The facilities name within the organisation (group name, etc.)                                                                      | Quantitative Biology Center               | :white_check_mark:                     | Text                                                                                                                                                                                                            |
| Id                 | Identifier of the measurement automatically assigned by the Data Manager                                                            | 001d7e11-55a3-4d8f<br/>-82e6-04466e868a64      | :white_check_mark:                     | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                    |
| Instrument         | Ontology Identifier of the instrument that has been used for the measurement, usually in the form PREFIX:REFERENCE                  | OBI:0002750                               | :white_check_mark:                     | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                                                              |
| Measurement code   | Human readable unique measurement code, automatically assigned by the Data Manager,usually in the form "NGS"SAMPLECODE"-"Timestamp" | NGSQ2ABCD001AA-<br/>118569093700875            | :white_check_mark:                     | Text, beginning with the domain(NGS) prefix <br/>followed by the [SampleCode](concepts.md#sample), <br/>seperated by a hyphen with its unique creation timestamp                                                          |
| Organization IRI   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted  | https://ror.org/03a1kwz48                 | :white_check_mark:                     | Identifier, validated according to the structure <br/>defined by the [RoR](https://ror.readme.io/docs/identifier)                                                                                                    |
| Organization label | Human Readable Name of the organization, automatically received from the RoR by the Organization IRI                                | University Tuebingen                      | :white_check_mark:                     | Text                                                                                                                                                                                                            |
| Read type          | The sequencing read type used to generate the sequence data.                                                                        | paired-end                                | :white_check_mark:                     | Enumeration, Selectable values can be found [here](https://github.com/qbicsoftware/data-manager-app/blob/main/user-interface/src/main/java/life/qbic/datamanager/files/export/measurement/NGSWorkbooks.java#L16) |
| Registration date  | Timestamp when the batch was created within the Data Manager                                                                        | 2025-04-28<br/> 08:24:25.000000                | :white_check_mark:                     | Date                                                                                                                                                                                                            |
| Sample id          | Identifier of the sample employed within the measurement                                                                            | 00058431-df92-48a6-<br/>891b-671d714bb723      | :white_check_mark:                     | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                    |
| Comment            | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                     | Repeated Measurement <br/>after Bad QC         | :x:                                    | Text                                                                                                                                                                                                            |
| Flow cell          | The flow cell type used for sequencing.                                                                                             | S4                                        | :x:                                    | Text                                                                                                                                                                                                            |
| Index I5           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S579            | :x: <br/> :white_check_mark: if pooled | Text                                                                                                                                                                                                            |
| Index I7           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S789            | :x: <br/> :white_check_mark: if pooled | Text                                                                                                                                                                                                            |
| Library kit        | The library kit employed during sequencing processing                                                                               | NEBNext Ultra II Directional RNA mRNA UMI | :x:                                    | Text                                                                                                                                                                                                            |
| Run protocol       | Information on how many cycles were used for each read and index during sequencing                                                  | 104+19+10+104                             | :x:                                    | Text                                                                                                                                                                                                            |
| Sample name        | Common human-readable name of the sample. Can also be internal lab identifier                                                       | Lab_Id_01                                 | :x:                                    | Text                                                                                                                                                                                                            |
| Sample pool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.              | Pool_1                                    | :x:                                    | Text                                                                                                                                                                                                            |

The current NGS Measurement Registration Template can be found here
[ngs_measurement_registration_sheet.xlsx](templates/ngs_measurement_registration_sheet.xlsx)

#### Proteomics

In our documentation you can find detailed information on how
to [register](../measurement/measurement_registration.md#proteomics)
or [edit](../measurement/measurement_edit.md#proteomics) your proteomics measurement

Below you can find an overview of the information associated with a proteomics measurement within
the Data Manager. This information can also be found in the "property information" tab within the
proteomics measurement
registration template sheet.

| Concept            | Description                                                                                                                                      | Example                                   | Mandatory          | Type                                                                                                                                                                                                                                                    |                             
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Digestion enzyme   | Information about the enzymes used for the proteolytic step.                                                                                     | Trypsin                                   | :white_check_mark: | Text                                                                                                                                                                                                                                                    |
| Digestion method   | Method that has been used to break proteins into peptides, Selectable from the methods "in gel", "in solution", "iST proteomics kit", "on beads" | in gel                                    | :white_check_mark: | Enumeration, Selectable values can be found [here](https://github.com/qbicsoftware/data-manager-app/blob/main/project-management/src/main/java/life/qbic/projectmanagement/application/measurement/validation/MeasurementProteomicsValidator.java#L166) |
| Facility           | The facilities name within the organisation (group name, etc.)                                                                                   | "Quantitative Biology Center"             | :white_check_mark: | Text                                                                                                                                                                                                                                                    |
| Id                 | Identifier of the measurement automatically assigned by the Data Manager                                                                         | 001d7e11-55a3-4d8f-<br/>82e6-04466e868a64 | :white_check_mark: | Identifier, validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                                                            |
| Instrument         | Ontology Identifier of the instrument that has been used for the measurement, usually in the form PREFIX:CODE                                    | BAO:0002733                               | :white_check_mark: | Identifier, structured as prefix:reference <br/>as seen in the [W3C](https://www.w3.org/TR/curie/) <br/>format specification                                                                                                                                      |
| Lc column          | The type of column that has been used.                                                                                                           | ProteoSil_100-C18                         | :white_check_mark: | Text                                                                                                                                                                                                                                                    |
| Measurement code   | Human readable unique measurement code, automatically assigned by the Data Manager,usually in the form "MS"SAMPLECODE"-"Timestamp"               | MSQ2ABCD001AA-<br/>118569093700875             | :white_check_mark: | Text, beginning with the domain(MS) prefix <br/>followed by the [SampleCode](concepts.md#sample), <br/>seperated by a hyphen with its unique creation timestamp                                                                                                   |
| Organization IRI   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted               | https://ror.org/03a1kwz48                 | :white_check_mark: | Identifier, validated according to the structure <br/>defined by the [RoR](https://ror.readme.io/docs/identifier)                                                                                                                                            |
| Organization label | Human Readable Name of the organization, automatically received from the RoR by the Organization IRI                                             | University Tuebingen                      | :white_check_mark: | Text                                                                                                                                                                                                                                                    |
| Registration date  | Timestamp when the batch was created within the Data Manager                                                                                     | 2025-04-28<br/> 08:24:25.000000           | :white_check_mark: | Date                                                                                                                                                                                                                                                    |
| Sample id          | Identifier of the sample employed within the measurement                                                                                         | 00058431-df92-48a6-<br/>891b-671d714bb723 | :white_check_mark: | Identifier , validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                                                                                                           |
| Comment            | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                                  | Repeated Measurement <br/>after Bad QC         | :x:                | Text                                                                                                                                                                                                                                                    |
| Enrichment method  | Enrichment of proteins or peptides of different characteristics.                                                                                 | Phosphopeptide Enrichment                 | :x:                | Text                                                                                                                                                                                                                                                    |
| Fraction name      | If the sample was fractionated this label can be used to indicate which fraction was measured.                                                   | Fraction01                                | :x:                | Text                                                                                                                                                                                                                                                    |
| Injection volume   | The sample volume injected into the LC column in microliter(µl).                                                                                 | 10                                        | :x:                | Number                                                                                                                                                                                                                                                  |
| Label              | The label value for the label type that has been used.                                                                                           | Heavy                                     | :x:                | Text                                                                                                                                                                                                                                                    |
| Label type         | The label type that has been used to label the sample for measurement.                                                                           | SILAC                                     | :x:                | Text                                                                                                                                                                                                                                                    |
| LCMS method        | Laboratory specific methods that have been used for LCMS measurement.                                                                            | APCI                                      | :x:                | Text                                                                                                                                                                                                                                                    |
| Replicate name     | Label to distinguish between technical replicates for repeated measurements of the same sample.                                                  | Replicate_1                               | :x:                | Text                                                                                                                                                                                                                                                    |
| Sample name        | Common human-readable name of the sample. Can also be internal lab identifier                                                                    | Lab_Id_01                                 | :x:                | Text                                                                                                                                                                                                                                                    |
| Sample pool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.                           | Pool_1                                    | :x:                | Text                                                                                                                                                                                                                                                    |

The current proteomics Measurement Registration Template can be found here
[proteomics_measurement_registration_sheet.xlsx](templates/proteomics_measurement_registration_sheet.xlsx)

#### Immunopeptidomics (Coming Soon)

### Raw Data

Please visit the raw data documentation
for detailed information on how to [upload](../rawdata/raw_data_upload.md)
or [download](../rawdata/raw_data_download.md) your raw data.

Below you can find an overview of the information associated with a raw data dataset within the Data
Manager

| Concept           | Description                                                                                                         | Example                              | Mandatory          | Type                                                                                                                                                                             |                                 
|-------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| File count        | Number of Files contained within the raw data upload, automatically determined by the Data Manager                  | 20                                   | :white_check_mark: | Number                                                                                                                                                                           |
| File size         | Size of all Files within the raw data upload, automatically determined by the Data Manager                          | 2000Mb                               | :white_check_mark: | Text                                                                                                                                                                             |
| File suffixes     | List of File suffixes for all files within a raw data upload, automatically determined by the Data Manager          | fastq, tar, txt                      | :white_check_mark: | List of Text                                                                                                                                                                     |
| Measurement code  | Human readable unique measurement code for which the raw data upload is associated with                             | NGSQ2ABCD001AA-<br/>118569093700875       | :white_check_mark: | Text, beginning with their respective domain(MS/NGS) prefix <br/>followed by the [SampleCode](concepts.md#sample), <br/>seperated by a hyphen with its unique creation timestamp |
| Measurement id    | Identifier of the measurement with which the raw data upload is associated with                                     | 001d7e11-55a3-4d8f-<br/>82e6-04466e868a64 | :white_check_mark: | Identifier, <br/>validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                           |
| Registration date | Timestamp when the raw data was uploaded within the Data Manager                                                    | 2025-04-28<br/> 08:24:25.000000@          | :white_check_mark: | Date                                                                                                                                                                             |
| Sample ids        | List of Identifiers of the samples which were measured resulting in the raw data generation and upload.             | 00058431-df92-48a6-<br/>891b-671d714bb723 | :white_check_mark: | List of Identifiers, <br/>validated against [RFC4122](https://www.rfc-editor.org/rfc/rfc5322">https://www.rfc-editor.org/rfc/rfc4122) <br/>format specification                  |
| Sample name       | List of the human-readable name of the samples which were measured resulting in the raw data generation and upload. | Lab_Id_01, Lab_Id_02                 | :white_check_mark: | Text                                                                                                                                                                             |

### Result Data (Coming Soon)
