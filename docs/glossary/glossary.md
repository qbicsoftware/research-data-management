# Data Modalities

## Quick Reference Table

| Section                     | Description                                                                  |                           
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
and [edit](../user/user_edit.md) your account within the data manager.

Below you can find an overview of the information associated with a user account within the Data
Manager

| Section          | Description                                                             | Example                              |                           
|------------------|-------------------------------------------------------------------------|--------------------------------------|
| Email            | Email address associated with the account                               | John.Doe@example.mail                |
| FullName         | First and last name of the user                                         | John Doe                             |
| OidcID           | Unique Id identifying the account within the Oidc provider (e.g. Orcid) | 0009-0006-0929-9338                  |
| OidcIssuer       | Oidc Issuer enabling the oauth process (e.g. via Orcid)                 | www.orcid.org                        |
| Password         | Password provided by the user during registration                       | YourAwesomePassword                  |
| RegistrationDate | Timestamp when the account was created within the system                | 01.02.9876                           |
| UserName         | Unique name specified for the account                                   | JohnDoe                              |
| UserId           | Unique Id associated with the user automatically assigned by the system | b1d536ce-fe29-4967-843f-2189bf971ae9 |

#### Personal Access Token

In our documentation you can find detailed information on how
to [register](../rawdata/raw_data_download.md#generate-a-token)
and [edit](../rawdata/raw_data_download.md#manage-tokens) your personal access tokens.

Below you can find an overview of the information associated with a personal access token within the
Data Manager

| Section          | Description                                                                  | Example                              |                           
|------------------|------------------------------------------------------------------------------|--------------------------------------|
| Description      | Description identifying the personal access token                            | Project XXX Data Download            |
| Duration         | Timeframe for which the access token is valid                                | 30 days                              |
| Id               | Unique Id for the personal access token automatically assigned by the system | 449c5bd7-3674-4797-98b7-ae2c2eb40e75 |
| RegistrationDate | Date when the access token was created within the system                     | 01.02.9876                           |
| Value            | Value within the personal access token, shown only once during creation      | 6J10PkciR6eG61656Y0cA178J74V8bZ5     |
| UserId           | User with which the personal access token is associated                      | b1d536ce-fe29-4967-843f-2189bf971ae9 |

### Project

For detailed information visit the [project documentation](../project/project_introduction.md)
There you will find detailed information on how to [register](../project/project_registration.md)
and [edit](../project/project_edit.md) a project within the data manager.
Additionally, it outlines how to grant or revoke [access](../project/project_access.md) to your
project to other users within the data manager.

Below you can find an overview of the information associated with a project within the Data
Manager

| Section                           | Description                                                                                         | Example                                                           |                           
|-----------------------------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Code                              | Human Readable unique Project Code of the project                                                   | Q2ABCD                                                            |
| GrantName                         | Name of the grant funding the project                                                               | DFG                                                               |
| GrantId                           | Unique Id identifying the grant funding the project                                                 | 213896434                                                         |
| Id                                | Type 4 uniquely random generated Id(UUID) of the project automatically assigned by the data manager | cdd81764-db7c-4635-b7f4-6e711b411e3c                              |
| ModificationDate                  | Timestamp when the project was last modified                                                        | 01.02.9876                                                        |
| Objective                         | Objective detailing the purpose and goal of the project                                             | Investigating the substance of interest with XXX to determine YYY |
| PrincipalInvestigatorFullName     | Full name of the principal investigator handling the project                                        | John Doe                                                          |
| PrincipalInvestigatorEmailAddress | Email address of the principal investigator handling the project                                    | John.Doe@example.mail                                             |
| ProjectManagerFullName            | Full name of the project manager handling the project                                               | Jane Doe                                                          |
| ProjectManagerEmailAddress        | Email address of the project manager handling the project                                           | Jane.Doe@example.mail                                             |
| ResponsiblePersonFullName         | Full name of the person responsible for the project                                                 | Max Mustermann                                                    |
| ResponsiblePersonEmailAddress     | Email address of the person responsible for the project                                             | Max.Mustermann@example.mail                                       |
| Title                             | Clear and concise title of the project                                                              | Analysis of the transcriptome of liver cancer sample              |

#### Offer

| Section   | Description                                          | Example                              |                            
|-----------|------------------------------------------------------|--------------------------------------|
| Name      | Filename of the uploaded offer                       | Q2ABCD_Offer.pdf                     |
| ProjectId | UUID of the project to which this offer was uploaded | cdd81764-db7c-4635-b7f4-6e711b411e3c |
| Signed    | Uploaded Offer was signed by the customer            | yes                                  |

#### Sample QC

| Section      | Description                                            | Example                              |                            
|--------------|--------------------------------------------------------|--------------------------------------|
| ExperimentId | UUID of the Experiment to which this sample QC belongs | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| Name         | Filename of the uploaded Sample QC report              | Q2ABCD_SampleQC.pdf                  |
| ProjectId    | UUID of the project to which the QC was uploaded       | cdd81764-db7c-4635-b7f4-6e711b411e3c |

### Experiment

For detailed information visit
the [experiment documentation](../experiment/experiment_introduction.md)

There you will find detailed information on how to [register](../experiment/experiment_creation.md)
and [edit](../experiment/experiment_creation.md) an experiment within the data manager.

Below you can find an overview of the information associated with an experiment within the Data
Manager.

| Section               | Description                                                                                                     | Example                                                                        |                            
|-----------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Analytes              | One or more substances or compounds of interest, whose expression changes are of interest within the experiment | RNA                                                                            |
| BiologicalReplicates  | Number of biologically distinct samples subjected to the same treatment during the experiment                   | 20                                                                             |
| ConfoundingVariables  | A variable possibly influencing independent and dependent experimental variables.                               | Varies See [here](../experiment/confounding-variables.md) for more information |
| ExperimentalGroups    | Group of subjects exposed to a unique combination (condition) of experimental variables                         | control, treatment_cohort_1                                                    |
| ExperimentalVariables | An Experimental factor defined to observe its effect on the subjects of an experiment.                          | temperature, time                                                              |
| Id                    | UUID of the experiment automatically assigned by the data manager                                               | dfcd156d-eb17-4cb0-99e1-68c5b1683237                                           |
| ModificationDate      | Timestamp when the experiment was last modified                                                                 | 01.02.9876                                                                     |
| Name                  | Unique name of the experiment                                                                                   | Pilot Experiment                                                               |
| Specimen              | One or more specific parts of the species from which the analytes are collected.                                | Liver                                                                          |
| Species               | One ore more Organisms from which the samples were collected                                                    | Homo Sapiens                                                                   |

#### Experimental Variables

| Section      | Description                                                                                      | Example                              |                            
|--------------|--------------------------------------------------------------------------------------------------|--------------------------------------|
| ExperimentId | UUID of the experiment with the experimental variable automatically assigned by the data manager | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| Levels       | One or more specific expression settings to which the variable can be set.                       | 0, 10, 100                           |
| Name         | Unique name of the experimental variable                                                         | Temperature                          |
| Unit         | Measurement Unit representing the specific setting of the variable                               | °C                                   |

#### Experimental Groups

| Section              | Description                                                                                   | Example                              |                            
|----------------------|-----------------------------------------------------------------------------------------------|--------------------------------------|
| BiologicalReplicates | Number of biologically distinct samples subjected to the same treatment during the experiment | 20                                   |
| Condition            | Unique combination of experimental variables                                                  | control, treatment_cohort_1          |
| ExperimentId         | UUID of the experiment automatically assigned by the data manager                             | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |

#### Confounding Variables

| Section      | Description                                                                                     | Example                              |                            
|--------------|-------------------------------------------------------------------------------------------------|--------------------------------------|
| ExperimentId | UUID of the experiment with the confounding variable automatically assigned by the data manager | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| Name         | Unique name of the experimental variable                                                        | Time                                 |

### Ontology

In our documentation you can find detailed information on how
to [search](../ontology_search/ontology_search_introduction.md#ontology-search-introduction)
for your ontology of interest.
Detailed information for each field can additionally be found within the documentation of
the [ontology service API](https://www.ebi.ac.uk/ols4/)

Below you can find an overview of the information associated with an ontology within the Data
Manager.

| Section              | Description                                                          | Example                                                                     |                            
|----------------------|----------------------------------------------------------------------|-----------------------------------------------------------------------------|
| ClassIri             | Unique resource identifier (IRI) for the term                        | http://purl.obolibrary.org/obo/NCIT_C105979                                 |
| Description          | Description providing explanation for the term                       | A protein complex that plays a role in neurotransmitter-gated ion transport |
| Label                | Common human-readable label of the term                              | 5-HT3 Receptor                                                              |
| Name                 | the OBO-style identifier, usually in the form PREFIX:ID              | NCIT:C105979                                                                |
| OntologyAbbreviation | Unused?                                                              | Unused?                                                                     |
| OntologyIri          | Unique resource identifier (IRI) for the ontology providing the term | http://purl.obolibrary.org/obo/ncbitaxon.owl                                |
| OntologyVersion      | Specific Version of the ontology providing the term                  | http://purl.obolibrary.org/obo/ncbitaxon/2023-09-19/ncbitaxon.owl           |

### Sample

In our documentation you can find detailed information on how
to [register](../batch/sample-batch.md#creating-and-registering-sample-batches)
and [edit](../batch/sample-batch.md#editing-sample-batches) your batches and samples.

Below you can find an overview of the information associated with a sample within the Data
Manager. This information can also be found in the "property information" tab within the sample
registration template sheet.

| Section        | Description                                                                                                                                                | Example                              |                          
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| AnalysisMethod | The test performed on samples for the purpose of finding and measuring chemical substances.                                                                | PROTEOMICS                           |
| Analyte        | The chemical substance extracted from the biological material that is identified and measured. Selection from the ones defined within the experiment       | RNA                                  |
| BatchId        | UUID of the batch the sample belonged to during its registration automatically assigned by the data manager                                                | 01422b86-407e-47e3-9cf6-093c4882d6b2 |
| Comment        | Free Text, can contain any notes related to a specific sample in question                                                                                  | "Redone QC"                          |
| Condition      | Condition to which the sample was subjected to. Selectable from the experimental groups within the experiment with each variable seperated by a semicolon. | Temperature: 0°C; Time: 100s;        |
| Id             | UUID of the sample automatically assigned by the data manager                                                                                              | 00058431-df92-48a6-891b-671d714bb723 |
| Label          | Common human-readable name of the sample. Can also be internal lab identifier                                                                              | Lab_Id_01                            |
| OrganismId     | Unused?                                                                                                                                                    | ????                                 |
| SampleCode     | Human readable unique sample code, automatically assigned by the data manager                                                                              | Q2ABCD001AA                          |
| Species        | Scientific name of the organism(s) from which the biological material is derived.  Selection from the ones defined within the experiment                   | Homo Sapiens                         |
| Specimen       | Name of the biological material from which the analytes would be extracted.       Selection from the ones defined within the experiment                    | Liver                                |

The current sample registration template sheet can be found here
[sample-metadata-template.xlsx](templates/sample-metadata-template.xlsx)

#### Batch

A batch can be defined as a group of samples processed or analyzed together under the same
experimental conditions with the aim to minimize technical variation.
Below you can find an overview of the information associated with a sample batch within the Data
Manager.

| Section          | Description                                                                                                 | Example                              |                          
|------------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Id               | UUID of the batch the sample belonged to during its registration automatically assigned by the data manager | 01422b86-407e-47e3-9cf6-093c4882d6b2 |
| ModificationDate | Timestamp when the batch was last modified                                                                  | 01.02.9876                           |
| Name             | Common human-readable label of the batch                                                                    | Pxp_Analysis_Trial_1                 |
| RegistrationDate | Timestamp when the batch was created within the data manager                                                | 01.02.9876                           |
| SampleCounter    | Number of samples contained within the batch                                                                | 20                                   |

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

| Section           | Description                                                                                                                         | Example                                   |                          
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Comment           | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                     | Repeated Measurement after Bad QC         |
| Facility          | The facilities name within the organisation (group name, etc.)                                                                      | Quantitative Biology Center               |
| Flowcell          | The flow cell type used for sequencing.                                                                                             | S4                                        |
| Id                | UUID of the measurement automatically assigned by the data manager                                                                  | 001d7e11-55a3-4d8f-82e6-04466e868a64      |
| IndexI5           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S579            |
| IndexI7           | Index used for multiplexing.                                                                                                        | NEBNext UDI UMI Set 1 B12 S789            |
| Instrument        | Ontology Curie of the instrument that has been used for the measurement, usually in the form PREFIX:CODE                            | OBI:0002750                               |
| LibraryKit        | The library kit employed during sequencing processing                                                                               | NEBNext Ultra II Directional RNA mRNA UMI |
| MeasurementCode   | Human readable unique measurement code, automatically assigned by the data manager,usually in the form "NGS"SAMPLECODE"-"Timestamp" | NGSQ2ABCD001AA-118569093700875            |
| OrganizationIRI   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted  | https://ror.org/03a1kwz48                 |
| OrganizationLabel | Human Readable Name of the organization, automatically received from the RoR by the OrganizationIRI                                 | University Tuebingen                      |
| ReadType          | The sequencing read type used to generate the sequence data.                                                                        | paired-end                                |
| RegistrationDate  | Timestamp when the batch was created within the data manager                                                                        | 01.02.9876                                |
| RunProtocol       | Information on how many cycles were used for each read and index during sequencing                                                  | 104+19+10+104                             |
| SampleId          | UUID of the sample employed within the measurement                                                                                  | 00058431-df92-48a6-891b-671d714bb723      |
| SamplePool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.              | Pool_1                                    |

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

| Section           | Description                                                                                                                                      | Example                              |                          
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Comment           | Free Text, can contain any notes related to a measurement in question with up to 500 characters                                                  | Repeated Measurement after Bad QC    |
| DigestionEnzyme   | Information about the enzymes used for the proteolytic step.                                                                                     | Trypsin                              |
| DigestionMethod   | Method that has been used to break proteins into peptides, Selectable from the methods "in gel", "in solution", "iST proteomics kit", "on beads" | in gel                               |
| EnrichmentMethod  | Enrichment of proteins or peptides of different characteristics.                                                                                 | Phosphopeptide Enrichment            |
| Facility          | The facilities name within the organisation (group name, etc.)                                                                                   | "Quantitative Biology Center"        |
| FractionName      | If the sample was fractionated this label can be used to indicate which fraction was measured.                                                   | Fraction01                           |
| Id                | UUID of the measurement automatically assigned by the data manager                                                                               | 001d7e11-55a3-4d8f-82e6-04466e868a64 |
| InjectionVolume   | The sample volume injected into the LC column in microliter(µl).                                                                                 | 10                                   |
| Instrument        | Ontology Curie of the instrument that has been used for the measurement, usually in the form PREFIX:CODE                                         | BAO:0002733                          |
| Label             | The label value for the label type that has been used.                                                                                           | Heavy                                |
| LabelType         | The label type that has been used to label the sample for measurement.                                                                           | SILAC                                |
| LcColumn          | The type of column that has been used.                                                                                                           | ProteoSil_100-C18                    |
| LcmsMethod        | Laboratory specific methods that have been used for LCMS measurement.                                                                            | APCI                                 |
| MeasurementCode   | Human readable unique measurement code, automatically assigned by the data manager,usually in the form "MS"SAMPLECODE"-"Timestamp"               | MSQ2ABCD001AA-118569093700875        |
| OrganizationIRI   | Research organization registry identifier([RoR Id](https://ror.org/)) of the organisation where the measurement has been conducted               | https://ror.org/03a1kwz48            |
| OrganizationLabel | Human Readable Name of the organization, automatically received from the RoR by the OrganizationIRI                                              | University Tuebingen                 |
| RegistrationDate  | Timestamp when the batch was created within the data manager                                                                                     | 01.02.9876                           |
| ReplicateName     | Label to distinguish between technical replicates for repeated measurements of the same sample.                                                  | Replicate_1                          |
| SampleId          | UUID of the sample employed within the measurement                                                                                               | 00058431-df92-48a6-891b-671d714bb723 |
| SamplePool        | A group of samples that are pooled together for a measurement. All samples in a pool group should have the same label.                           | Pool_1                               |

The current proteomics Measurement Registration Template can be found here
[proteomics_measurement_registration_sheet.xlsx](templates/proteomics_measurement_registration_sheet.xlsx)

#### Immunopeptidomics (Coming Soon)

### Raw Data

Please visit the raw data documentation
for detailed information on how to [upload](../rawdata/raw_data_upload.md)
or [download](../rawdata/raw_data_download.md) your raw data.

Below you can find an overview of the information associated with a raw data dataset within the Data
Manager

| Section          | Description                                                                                                         | Example                              |                          
|------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| FileCount        | Number of Files contained within the raw data upload                                                                | 20                                   |
| FileSize         | Size of all Files within the raw data upload                                                                        | 2000Mb                               |
| FileSuffixes     | List of File suffixes for all files within a raw data upload                                                        | fastq, tar, txt                      |
| MeasurementCode  | Human readable unique measurement code for which the raw data upload is associated with                             | NGSQ2ABCD001AA-118569093700875       |
| MeasurementId    | UUID of the measurement with which the raw data upload is associated with                                           | 001d7e11-55a3-4d8f-82e6-04466e868a64 |
| RegistrationDate | Timestamp when the raw data was uploaded within the data manager                                                    | 01.02.9876                           |
| SampleIds        | List of UUIDs of the samples which were measured resulting in the raw data generation and upload.                   | 00058431-df92-48a6-891b-671d714bb723 |
| SampleName       | List of the human-readable name of the samples which were measured resulting in the raw data generation and upload. | Lab_Id_01, Lab_Id_02                 |

### Result Data (Coming Soon)
