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
| UserId           | Unique Id associated with the user within the system                    | b1d536ce-fe29-4967-843f-2189bf971ae9 |

#### Personal Access Token

In our documentation you can find detailed information on how
to [register](../rawdata/raw_data_download.md#generate-a-token)
and [edit](../rawdata/raw_data_download.md#manage-tokens) your personal access tokens.

Below you can find an overview of the information associated with a personal access token within the
Data Manager

| Section          | Description                                                             | Example                              |                           
|------------------|-------------------------------------------------------------------------|--------------------------------------|
| Description      | Description identifying the personal access token                       | Project XXX Data Download            |
| Duration         | Timeframe for which the access token is valid                           | 30 days                              |
| Id               | Unique Id for the personal access token within the system               | 449c5bd7-3674-4797-98b7-ae2c2eb40e75 |
| RegistrationDate | Date when the access token was created within the system                | 01.02.9876                           |
| Value            | Value within the personal access token, shown only once during creation | 6J10PkciR6eG61656Y0cA178J74V8bZ5     |
| UserId           | User with which the personal access token is associated                 | b1d536ce-fe29-4967-843f-2189bf971ae9 |

### Project

For detailed information visit the [project documentation](../project/project_introduction.md)
There you will find detailed information on how to [register](../project/project_registration.md)
and [edit](../project/project_edit.md) a project within the data manager.
Additionally, it outlines how to grant or revoke [access](../project/project_access.md) to your
project to other users within the data manager.

Below you can find an overview of the information associated with a project within the Data
Manager

| Section                           | Description                                                      | Example                                                           |                           
|-----------------------------------|------------------------------------------------------------------|-------------------------------------------------------------------|
| Code                              | Human Readable unique Project Code of the project                | Q2ABCD                                                            |
| GrantName                         | Name of the grant funding the project                            | DFG                                                               |
| GrantId                           | Unique Id identifying the grant funding the project              | 213896434                                                         |
| Id                                | Type 4 uniquely random generated Id of the project               | cdd81764-db7c-4635-b7f4-6e711b411e3c                              |
| ModificationDate                  | Timestamp when the project was last modified                     | 01.02.9876                                                        |
| Objective                         | Objective detailing the purpose and goal of the project          | Investigating the substance of interest with XXX to determine YYY |
| PrincipalInvestigatorFullName     | Full name of the principal investigator handling the project     | John Doe                                                          |
| PrincipalInvestigatorEmailAddress | Email address of the principal investigator handling the project | John.Doe@example.mail                                             |
| ProjectManagerFullName            | Full name of the project manager handling the project            | Jane Doe                                                          |
| ProjectManagerEmailAddress        | Email address of the project manager handling the project        | Jane.Doe@example.mail                                             |
| ResponsiblePersonFullName         | Full name of the person responsible for the project              | Max Mustermann                                                    |
| ResponsiblePersonEmailAddress     | Email address of the person responsible for the project          | Max.Mustermann@example.mail                                       |
| Title                             | Clear and concise title of the project                           | Analysis of the transcriptome of liver cancer sample              |

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

| Section               | Description                                                                         | Example                              |                            
|-----------------------|-------------------------------------------------------------------------------------|--------------------------------------|
| Analytes              | Project Title                                                                       | RNA                                  |
| BiologicalReplicates  | Biologically distinct samples subjected to the same treatment during the experiment | 20                                   |
| ConfoundingVariables  | FillMe                                                                              | FillMe                               |
| ExperimentalGroups    | Objective of the project                                                            | control, treatment_cohort_1          |
| ExperimentalVariables | FillMe                                                                              | tissue_type, treatment               |
| Id                    | UUID of the experiment                                                              | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| ModificationDate      | FillMe                                                                              | 01.02.9876                           |
| Name                  | Unique name of the experiment                                                       | Pilot Experiment                     |
| Specimen              | FillMe                                                                              | Liver                                |
| Species               | FillMe                                                                              | Homo Sapiens                         |

#### Experimental Variables

| Section      | Description | Example                              |                            
|--------------|-------------|--------------------------------------|
| ExperimentId | FillMe      | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| Levels       | FillMe      | FillMe                               |
| Name         | FillMe      | FillMe                               |
| Unit         | FillMe      | FillMe                               |

#### Experimental Groups

| Section              | Description | Example                              |                            
|----------------------|-------------|--------------------------------------|
| BiologicalReplicates | FillMe      | FillMe                               |
| Condition            | FillMe      | FillMe                               |
| ExperimentId         | FillMe      | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |

#### Confounding Variables

| Section      | Description | Example                              |                            
|--------------|-------------|--------------------------------------|
| ExperimentId | FillMe      | dfcd156d-eb17-4cb0-99e1-68c5b1683237 |
| Name         | FillMe      | FillMe                               |

### Ontology

In our documentation you can find detailed information on how
to [search](../ontology_search/ontology_search_introduction.md#ontology-search-introduction)
for your ontology of interest.

Below you can find an overview of the information associated with an ontology within the Data
Manager.

| Section              | Description | Example |                            
|----------------------|-------------|---------|
| ClassIri             | FillMe      | FillMe  |
| Description          | FillMe      | FillMe  |
| Label                | FillMe      | FillMe  |
| Name                 | FillMe      | FillMe  |
| OntologyAbbreviation | FillMe      | FillMe  |
| OntologyIri          | FillMe      | FillMe  |
| OntologyVersion      | FillMe      | FillMe  |

### Sample

In our documentation you can find detailed information on how
to [register](../batch/sample-batch.md#creating-and-registering-sample-batches)
and [edit](../batch/sample-batch.md#editing-sample-batches) your batches and samples.

Below you can find an overview of the information associated with a sample within the Data
Manager

| Section           | Description | Example |                          
|-------------------|-------------|---------|
| AnalysisMethod    | FillMe      | FillMe  |
| Analyte           | FillMe      | FillMe  |
| BatchId           | FillMe      | FillMe  |
| ExperimentalGroup | FillMe      | FillMe  |
| Id                | FillMe      | FillMe  |
| Label             | FillMe      | FillMe  |
| OrganismId        | FillMe      | FillMe  |
| SampleCode        | FillMe      | FillMe  |
| Species           | FillMe      | FillMe  |
| Specimen          | FillMe      | FillMe  |

The current sample registration template sheet can be found here
[sample-metadata-template.xlsx](templates/sample-metadata-template.xlsx)

#### Batch

Below you can find an overview of the information associated with a sample batch within the Data
Manager

| Section          | Description | Example |                          
|------------------|-------------|---------|
| Id               | FillMe      | FillMe  |
| ModificationDate | FillMe      | FillMe  |
| Name             | FillMe      | FillMe  |
| RegistrationDate | FillMe      | FillMe  |
| SampleCounter    | FillMe      | FillMe  |

### Measurement

For detailed information visit
the [measurement documentation](../measurement/measurement_introduction.md)

#### Genomics

In our documentation you can find detailed information on how
to [register](../measurement/measurement_registration.md#genomics)
or [edit](../measurement/measurement_edit.md#genomics) your proteomics measurement

Below you can find an overview of the information associated with a genomic measurement within the
Data Manager

| Section           | Description | Example |                          
|-------------------|-------------|---------|
| Comment           | FillMe      | FillMe  |
| DigestionEnzyme   | FillMe      | FillMe  |
| DigestionMethod   | FillMe      | FillMe  |
| EnrichmentMethod  | FillMe      | FillMe  |
| Facility          | FillMe      | FillMe  |
| FractionName      | FillMe      | FillMe  |
| Id                | FillMe      | FillMe  |
| InjectionVolume   | FillMe      | FillMe  |
| Instrument        | FillMe      | FillMe  |
| Label             | FillMe      | FillMe  |
| LabelType         | FillMe      | FillMe  |
| LcColumn          | FillMe      | FillMe  |
| LcmsMethod        | FillMe      | FillMe  |
| MeasurementCode   | FillMe      | FillMe  |
| OrganizationIRI   | FillMe      | FillMe  |
| OrganizationLabel | FillMe      | FillMe  |
| RegistrationDate  | FillMe      | FillMe  |
| ReplicateName     | FillMe      | FillMe  |
| SampleId          | FillMe      | FillMe  |
| SamplePool        | FillMe      | FillMe  |

The current NGS Measurement Registration Template can be found here
[ngs_measurement_registration_sheet.xlsx](templates/ngs_measurement_registration_sheet.xlsx)

#### Proteomics

In our documentation you can find detailed information on how
to [register](../measurement/measurement_registration.md#proteomics)
or [edit](../measurement/measurement_edit.md#proteomics) your proteomics measurement

Below you can find an overview of the information associated with a proteomics measurement within
the Data Manager

| Section           | Description | Example |                          
|-------------------|-------------|---------|
| Comment           | FillMe      | FillMe  |
| Facility          | FillMe      | FillMe  |
| Flowcell          | FillMe      | FillMe  |
| Id                | FillMe      | FillMe  |
| IndexI5           | FillMe      | FillMe  |
| IndexI7           | FillMe      | FillMe  |
| Instrument        | FillMe      | FillMe  |
| LibraryKit        | FillMe      | FillMe  |
| MeasurementCode   | FillMe      | FillMe  |
| OrganizationIRI   | FillMe      | FillMe  |
| OrganizationLabel | FillMe      | FillMe  |
| ReadType          | FillMe      | FillMe  |
| RegistrationDate  | FillMe      | FillMe  |
| RunProtocol       | FillMe      | FillMe  |
| SamplePool        | FillMe      | FillMe  |
| SampleId          | FillMe      | FillMe  |

The current genomic Measurement Registration Template can be found here
[proteomics_measurement_registration_sheet.xlsx](templates/proteomics_measurement_registration_sheet.xlsx)

#### Immunopeptidomics (Coming Soon)

### Raw Data

Please visit the raw data documentation
for detailed information on how to [upload](../rawdata/raw_data_upload.md)
or [download](../rawdata/raw_data_download.md) your raw data.

Below you can find an overview of the information associated with a raw data dataset within the Data
Manager

| Section          | Description | Example |                          
|------------------|-------------|---------|
| FileCount        | FillMe      | FillMe  |
| FileSize         | FillMe      | FillMe  |
| FileSuffixes     | FillMe      | FillMe  |
| MeasurementId    | FillMe      | FillMe  |
| RegistrationDate | FillMe      | FillMe  |
| SampleIds        | FillMe      | FillMe  |
| SampleName       | FillMe      | FillMe  |

### Result Data (Coming Soon)
