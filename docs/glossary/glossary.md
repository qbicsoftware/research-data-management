# Data Modalities

## Quick Reference Table

| Concept                     | Description                                                                  |                           
|-----------------------------|------------------------------------------------------------------------------|
| [User](#user)               | Learn more about the metadata of your user account and its authentication    | 
| [Project](#project)         | Information about a projects metadata such as contact, funding and objective | 
| [Ontology](#ontology)       | Find out more about the ontologies employed within experiments and samples   | 
| [Experiment](#experiment)   | Everything related to the metadata within an experimental design             | 
| [Sample](#sample)           | Detailed information concerning the metadata of sample and batches           | 
| [Measurement](#measurement) | Everything related to NGS and PxP measurement metadata                       | 
| [Raw Data](#raw-data)       | Find out more about the metadata surrounding Data Upload and Download        | 

### User

In our documentation you can find detailed information on how
to [register](../user/user_registration.md)
and [edit](../user/user_edit.md) your account within the Data Manager.

Below you can find an overview of the information associated with a user account within the Data
Manager

| Concept           | Description                                                             | Example                              | Mandatory          |                          
|-------------------|-------------------------------------------------------------------------|--------------------------------------|--------------------|
| Email             | Email address associated with the account                               | John.Doe@example.mail                | :white_check_mark: |
| Full name         | First and last name of the user                                         | John Doe                             | :white_check_mark: |
| Oidc id           | Unique Id identifying the account within the Oidc provider (e.g. Orcid) | 0009-0006-0929-9338                  | :white_check_mark: |
| Oidc issuer       | Oidc Issuer enabling the oauth process (e.g. via Orcid)                 | https://www.orcid.org                | :white_check_mark: |
| Registration date | Timestamp when the account was created within the system                | 01.02.9876                           | :white_check_mark: |
| User name         | Unique name specified for the account                                   | JohnDoe                              | :white_check_mark: |
| User id           | Unique Id associated with the user automatically assigned by the system | b1d536ce-fe29-4967-843f-2189bf971ae9 | :white_check_mark: |

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

| Concept                              | Description                                                                                         | Example                                                           | Mandatory          |               
|--------------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------|
| Code                                 | Human Readable unique Project Code of the project                                                   | Q2ABCD                                                            | :white_check_mark: |
| Id                                   | Type 4 uniquely random generated Id(UUID) of the project automatically assigned by the Data Manager | cdd81764-db7c-4635-b7f4-6e711b411e3c                              | :white_check_mark: |
| Modification date                    | Timestamp when the project was last modified                                                        | 01.02.9876                                                        | :white_check_mark: |
| Objective                            | Objective detailing the purpose and goal of the project                                             | Investigating the substance of interest with XXX to determine YYY | :white_check_mark: |
| Principal investigator full name     | Full name of the principal investigator handling the project                                        | John Doe                                                          | :white_check_mark: |
| Principal investigator email address | Email address of the principal investigator handling the project                                    | John.Doe@example.mail                                             | :white_check_mark: |
| ProjectManager full name             | Full name of the project manager handling the project                                               | Jane Doe                                                          | :white_check_mark: |
| ProjectManager email address         | Email address of the project manager handling the project                                           | Jane.Doe@example.mail                                             | :white_check_mark: |
| Title                                | Clear and concise title of the project                                                              | Analysis of the transcriptome of liver cancer sample              | :white_check_mark: |
| Grant name                           | Name of the grant funding the project                                                               | DFG                                                               | :x:                |
| Grant id                             | Unique Id identifying the grant funding the project                                                 | 213896434                                                         | :x:                |
| ResponsiblePerson full name          | Full name of the person responsible for the project                                                 | Max Mustermann                                                    | :x:                |
| ResponsiblePerson email address      | Email address of the person responsible for the project                                             | Max.Mustermann@example.mail                                       | :x:                |

#### Offer

For detailed information visit
the [project editing documentation](../project/project_edit.md)

There you will find detailed information on how
to [register](../project/project_edit.md#offer-upload)
and [edit](../project/project_edit.md#offer-upload) your offer file within the Data Manager.

Below you can find an overview of the information associated with an offer file within the Data
Manager.

| Concept    | Description                                          | Example                              | Mandatory          |                              
|------------|------------------------------------------------------|--------------------------------------|--------------------|
| Name       | Filename of the uploaded offer                       | Q2ABCD_Offer.pdf                     | :white_check_mark: |
| Project id | UUID of the project to which this offer was uploaded | cdd81764-db7c-4635-b7f4-6e711b411e3c | :white_check_mark: |
| Signed     | Uploaded Offer was signed by the customer            | yes/no                               | :white_check_mark: |

#### Sample QC

For detailed information visit
the [project editing documentation](../project/project_edit.md)

There you will find detailed information on how
to [register](../project/project_edit.md#quality-control-upload)
and [edit](../project/project_edit.md#quality-control-upload) your sample qc file within the Data
Manager.

Below you can find an overview of the information associated with a quality control file within the
Data Manager.

| Concept       | Description                                            | Example                              | Mandatory          |                             
|---------------|--------------------------------------------------------|--------------------------------------|--------------------|
| Experiment id | UUID of the Experiment to which this sample QC belongs | dfcd156d-eb17-4cb0-99e1-68c5b1683237 | :white_check_mark: |
| Name          | Filename of the uploaded Sample QC report              | Q2ABCD_SampleQC.pdf                  | :white_check_mark: |
| Project id    | UUID of the project to which the QC was uploaded       | cdd81764-db7c-4635-b7f4-6e711b411e3c | :white_check_mark: |

### Experiment

For detailed information visit
the [experiment documentation](../experiment/experiment_introduction.md)

There you will find detailed information on how to [register](../experiment/experiment_creation.md)
and [edit](../experiment/experiment_creation.md) an experiment within the Data Manager.

Below you can find an overview of the information associated with an experiment within the Data
Manager.

| Concept                | Description                                                                                                     | Example                                                                        | Mandatory          |                                  
|------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------|
| Analytes               | One or more substances or compounds of interest, whose expression changes are of interest within the experiment | RNA                                                                            | :white_check_mark: |
| Biological replicates  | Number of biologically distinct samples subjected to the same treatment during the experiment                   | 20                                                                             | :white_check_mark: |
| Experimental groups    | Group of subjects exposed to a unique combination (condition) of experimental variables                         | control, treatment_cohort_1                                                    | :white_check_mark: |
| Experimental variables | An Experimental factor defined to observe its effect on the subjects of an experiment.                          | temperature, time                                                              | :white_check_mark: |
| Id                     | UUID of the experiment automatically assigned by the Data Manager                                               | dfcd156d-eb17-4cb0-99e1-68c5b1683237                                           | :white_check_mark: |
| Modification date      | Timestamp when the experiment was last modified                                                                 | 01.02.9876                                                                     | :white_check_mark: |
| Name                   | Unique name of the experiment                                                                                   | Pilot Experiment                                                               | :white_check_mark: |
| Specimen               | One or more specific parts of the species from which the analytes are collected.                                | Liver                                                                          | :white_check_mark: |
| Species                | One ore more Organisms from which the samples were collected                                                    | Homo Sapiens                                                                   | :white_check_mark: |
| Confounding variables  | A variable possibly influencing independent and dependent experimental variables.                               | Varies See [here](../experiment/confounding-variables.md) for more information | :x:                |

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

| Concept       | Description                                                                                      | Example                              | Mandatory          |                        
|---------------|--------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Experiment id | UUID of the experiment with the experimental variable automatically assigned by the Data Manager | dfcd156d-eb17-4cb0-99e1-68c5b1683237 | :white_check_mark: |
| Levels        | One or more specific expression settings to which the variable can be set.                       | 0, 10, 100                           | :white_check_mark: |
| Name          | Unique name of the experimental variable                                                         | Temperature                          | :white_check_mark: |
| Unit          | Measurement Unit representing the specific setting of the variable                               | °C                                   | :x:                |

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

| Concept               | Description                                                                                   | Example                              | Mandatory          |                       
|-----------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Biological replicates | Number of biologically distinct samples subjected to the same treatment during the experiment | 20                                   | :white_check_mark: |
| Condition             | Unique combination of experimental variables                                                  | control, treatment_cohort_1          | :white_check_mark: |
| Experiment id         | UUID of the experiment automatically assigned by the Data Manager                             | dfcd156d-eb17-4cb0-99e1-68c5b1683237 | :white_check_mark: |

#### Confounding Variables

For detailed information visit
the [experiment documentation](../experiment/confounding-variables.md)

There you will find detailed information on how
to [register](../experiment/confounding-variables.md#define-confounding-variables-in-your-experiment)
and [edit](../experiment/confounding-variables.md#rename-a-confounding-variable) your experimental
variables within the Data Manager.

Below you can find an overview of the information associated with a confounding variable within the
Data Manager.

| Concept       | Description                                                                                     | Example                              | Mandatory          |                           
|---------------|-------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Experiment id | UUID of the experiment with the confounding variable automatically assigned by the Data Manager | dfcd156d-eb17-4cb0-99e1-68c5b1683237 | :white_check_mark: |
| Name          | Unique name of the experimental variable                                                        | Time                                 | :white_check_mark: |

### Ontology

In our documentation you can find detailed information on how
to [search](../ontology_search/ontology_search_introduction.md#ontology-search-introduction)
for your ontology of interest.
Detailed information for each field can additionally be found within the documentation of
the [ontology service API](https://www.ebi.ac.uk/ols4/)

Below you can find an overview of the information associated with an ontology within the Data
Manager.

| Concept               | Description                                                          | Example                                                                     | Mandatory          |                          
|-----------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------------|
| Class iri             | Unique resource identifier (IRI) for the term                        | http://purl.obolibrary.org/obo/NCIT_C105979                                 | :white_check_mark: |
| Description           | Description providing explanation for the term                       | A protein complex that plays a role in neurotransmitter-gated ion transport | :white_check_mark: |
| Label                 | Common human-readable label of the term                              | 5-HT3 Receptor                                                              | :white_check_mark: |
| Name                  | the OBO-style identifier, usually in the form PREFIX:ID              | NCIT:C105979                                                                | :white_check_mark: |
| Ontology abbreviation | Unused?                                                              | Unused?                                                                     | :white_check_mark: |
| Ontology iri          | Unique resource identifier (IRI) for the ontology providing the term | http://purl.obolibrary.org/obo/ncbitaxon.owl                                | :white_check_mark: |
| Ontology version      | Specific Version of the ontology providing the term                  | http://purl.obolibrary.org/obo/ncbitaxon/2023-09-19/ncbitaxon.owl           | :white_check_mark: |

### Sample

In our documentation you can find detailed information on how
to [register](../batch/sample-batch.md#creating-and-registering-sample-batches)
and [edit](../batch/sample-batch.md#editing-sample-batches) your batches and samples.

Below you can find an overview of the information associated with a sample within the Data
Manager. This information can also be found in the "property information" tab within the sample
registration template sheet.

| Concept              | Description                                                                                                                                                | Example                              | Mandatory          |                         
|----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Analysis method      | The test performed on samples for the purpose of finding and measuring chemical substances.                                                                | PROTEOMICS                           | :white_check_mark: |
| Analyte              | The chemical substance extracted from the biological material that is identified and measured. Selection from the ones defined within the experiment       | RNA                                  | :white_check_mark: |
| Batch id             | UUID of the batch the sample belonged to during its registration automatically assigned by the Data Manager                                                | 01422b86-407e-47e3-9cf6-093c4882d6b2 | :white_check_mark: |
| Condition            | Condition to which the sample was subjected to. Selectable from the experimental groups within the experiment with each variable seperated by a semicolon. | Temperature: 0°C; Time: 100s;        | :white_check_mark: |
| Id                   | UUID of the sample automatically assigned by the Data Manager                                                                                              | 00058431-df92-48a6-891b-671d714bb723 | :white_check_mark: |
| Label                | Common human-readable name of the sample. Can also be internal lab identifier                                                                              | Lab_Id_01                            | :white_check_mark: |
| Sample code          | Human readable unique sample code, automatically assigned by the Data Manager                                                                              | Q2ABCD001AA                          | :white_check_mark: |
| Species              | Scientific name of the organism(s) from which the biological material is derived.  Selection from the ones defined within the experiment                   | Homo Sapiens                         | :white_check_mark: |
| Specimen             | Name of the biological material from which the analytes would be extracted.       Selection from the ones defined within the experiment                    | Liver                                | :white_check_mark: |
| Biological Replicate | Specifiy if the samples belong to the same biological source within your experiment.                                                                       | "Mouse_WT_1"                         | :x:                |
| Comment              | Free Text, can contain any notes related to a specific sample in question                                                                                  | "Redone QC"                          | :x:                |

The current sample registration template sheet can be found herel
[sample-metadata-template.xlsx](templates/sample-metadata-template.xlsx)

#### Batch

A batch can be defined as a group of samples processed or analyzed together under the same
experimental conditions with the aim to minimize technical variation.
Below you can find an overview of the information associated with a sample batch within the Data
Manager.

| Concept           | Description                                                                                                                                        | Example                              | Mandatory          |                         
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Id                | UUID of the batch the sample belonged to during its registration automatically assigned by the Data Manager                                        | 01422b86-407e-47e3-9cf6-093c4882d6b2 | :white_check_mark: |
| Modification date | Timestamp when the batch was last modified                                                                                                         | 01.02.9876                           | :white_check_mark: |
| Name              | Common human-readable label of the batch                                                                                                           | Pxp_Analysis_Trial_1                 | :white_check_mark: |
| Registration date | Timestamp when the batch was created within the Data Manager                                                                                       | 01.02.9876                           | :white_check_mark: |
| Sample count      | Number of samples contained within the batch, automatically determined by the Data Manager from the number of samples provided during registration | 20                                   | :white_check_mark: |

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

| Concept            | Description                                                                                                                         | Example                                   | Mandatory                              |                          
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|----------------------------------------|
| Facility           | The facilities name within the organisation (group name, etc.)                                                                      | Quantitative Biology Center               | :white_check_mark:                     |
| Id                 | UUID of the measurement automatically assigned by the Data Manager                                                                  | 001d7e11-55a3-4d8f-82e6-04466e868a64      | :white_check_mark:                     |
| Instrument         | Ontology Curie of the instrument that has been used for the measurement, usually in the form PREFIX:CODE                            | OBI:0002750                               | :white_check_mark:                     |
| Measurement code   | Human readable unique measurement code, automatically assigned by the Data Manager,usually in the form "NGS"SAMPLECODE"-"Timestamp" | NGSQ2ABCD001AA-118569093700875            | :white_check_mark:                     |
| Organization iri   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted  | https://ror.org/03a1kwz48                 | :white_check_mark:                     |
| Organization label | Human Readable Name of the organization, automatically received from the RoR by the OrganizationIRI                                 | University Tuebingen                      | :white_check_mark:                     |
| Read type          | The sequencing read type used to generate the sequence data.                                                                        | paired-end                                | :white_check_mark:                     |
| Registration date  | Timestamp when the batch was created within the Data Manager                                                                        | 01.02.9876                                | :white_check_mark:                     |
| Sample id          | UUID of the sample employed within the measurement                                                                                  | 00058431-df92-48a6-891b-671d714bb723      | :white_check_mark:                     |
| Comment            | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                     | Repeated Measurement after Bad QC         | :x:                                    |
| Flow cell          | The flow cell type used for sequencing.                                                                                             | S4                                        | :x:                                    |
| Index I5           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S579            | :x: <br/> :white_check_mark: if pooled |
| Index I7           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S789            | :x: <br/> :white_check_mark: if pooled |
| Library kit        | The library kit employed during sequencing processing                                                                               | NEBNext Ultra II Directional RNA mRNA UMI | :x:                                    |
| Run protocol       | Information on how many cycles were used for each read and index during sequencing                                                  | 104+19+10+104                             | :x:                                    |
| Sample name        | Common human-readable name of the sample. Can also be internal lab identifier                                                       | Lab_Id_01                                 | :x:                                    |
| Sample pool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.              | Pool_1                                    | :x:                                    |

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

| Concept            | Description                                                                                                                                      | Example                              | Mandatory          |                              
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| Digestion enzyme   | Information about the enzymes used for the proteolytic step.                                                                                     | Trypsin                              | :white_check_mark: |
| Digestion method   | Method that has been used to break proteins into peptides, Selectable from the methods "in gel", "in solution", "iST proteomics kit", "on beads" | in gel                               | :white_check_mark: |
| Facility           | The facilities name within the organisation (group name, etc.)                                                                                   | "Quantitative Biology Center"        | :white_check_mark: |
| Id                 | UUID of the measurement automatically assigned by the Data Manager                                                                               | 001d7e11-55a3-4d8f-82e6-04466e868a64 | :white_check_mark: |
| Instrument         | Ontology Curie of the instrument that has been used for the measurement, usually in the form PREFIX:CODE                                         | BAO:0002733                          | :white_check_mark: |
| Lc column          | The type of column that has been used.                                                                                                           | ProteoSil_100-C18                    | :white_check_mark: |
| Measurement code   | Human readable unique measurement code, automatically assigned by the Data Manager,usually in the form "MS"SAMPLECODE"-"Timestamp"               | MSQ2ABCD001AA-118569093700875        | :white_check_mark: |
| Organization iri   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted               | https://ror.org/03a1kwz48            | :white_check_mark: |
| Organization label | Human Readable Name of the organization, automatically received from the RoR by the OrganizationIRI                                              | University Tuebingen                 | :white_check_mark: |
| Registration date  | Timestamp when the batch was created within the Data Manager                                                                                     | 01.02.9876                           | :white_check_mark: |
| Sample id          | UUID of the sample employed within the measurement                                                                                               | 00058431-df92-48a6-891b-671d714bb723 | :white_check_mark: |
| Comment            | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                                  | Repeated Measurement after Bad QC    | :x:                |
| Enrichment method  | Enrichment of proteins or peptides of different characteristics.                                                                                 | Phosphopeptide Enrichment            | :x:                |
| Fraction name      | If the sample was fractionated this label can be used to indicate which fraction was measured.                                                   | Fraction01                           | :x:                |
| Injection volume   | The sample volume injected into the LC column in microliter(µl).                                                                                 | 10                                   | :x:                |
| Label              | The label value for the label type that has been used.                                                                                           | Heavy                                | :x:                |
| Label type         | The label type that has been used to label the sample for measurement.                                                                           | SILAC                                | :x:                |
| LCMS method        | Laboratory specific methods that have been used for LCMS measurement.                                                                            | APCI                                 | :x:                |
| Replicate name     | Label to distinguish between technical replicates for repeated measurements of the same sample.                                                  | Replicate_1                          | :x:                |
| Sample name        | Common human-readable name of the sample. Can also be internal lab identifier                                                                    | Lab_Id_01                            | :x:                |
| Sample pool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.                           | Pool_1                               | :x:                |

The current proteomics Measurement Registration Template can be found here
[proteomics_measurement_registration_sheet.xlsx](templates/proteomics_measurement_registration_sheet.xlsx)

#### Immunopeptidomics (Coming Soon)

### Raw Data

Please visit the raw data documentation
for detailed information on how to [upload](../rawdata/raw_data_upload.md)
or [download](../rawdata/raw_data_download.md) your raw data.

Below you can find an overview of the information associated with a raw data dataset within the Data
Manager

| Concept           | Description                                                                                                         | Example                              | Mandatory          |                         
|-------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------|--------------------|
| File count        | Number of Files contained within the raw data upload, automatically determined by the Data Manager                  | 20                                   | :white_check_mark: |
| File size         | Size of all Files within the raw data upload, automatically determined by the Data Manager                          | 2000Mb                               | :white_check_mark: |
| File suffixes     | List of File suffixes for all files within a raw data upload, automatically determined by the Data Manager          | fastq, tar, txt                      | :white_check_mark: |
| Measurement code  | Human readable unique measurement code for which the raw data upload is associated with                             | NGSQ2ABCD001AA-118569093700875       | :white_check_mark: |
| Measurement id    | UUID of the measurement with which the raw data upload is associated with                                           | 001d7e11-55a3-4d8f-82e6-04466e868a64 | :white_check_mark: |
| Registration date | Timestamp when the raw data was uploaded within the Data Manager                                                    | 01.02.9876                           | :white_check_mark: |
| Sample ids        | List of UUIDs of the samples which were measured resulting in the raw data generation and upload.                   | 00058431-df92-48a6-891b-671d714bb723 | :white_check_mark: |
| Sample name       | List of the human-readable name of the samples which were measured resulting in the raw data generation and upload. | Lab_Id_01, Lab_Id_02                 | :white_check_mark: |

### Result Data (Coming Soon)
