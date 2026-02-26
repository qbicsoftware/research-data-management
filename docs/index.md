# Life Science Data Management

Good science starts with good data management. The [QBiC Data Manager](https://rdm.qbic.uni-tuebingen.de/login) helps you keep your research data organised, findable, and ready to share — from your first experiment through to publication.

Not sure where to begin? Head to the **[Get started guide](get_started/process_overview.md)**.

---

## What's new

### Data submission from outside the University of Tübingen network

<div style="font-size: smaller; color: rgba(122,122,122,1)">October 10th, 2025</div>

- **External data submission:** Collaborators outside the university network can now upload measurement data. See how to [request server access](rawdata/raw_data_request_server_access.md) and [upload your data](rawdata/raw_data_upload.md).
- **ORCID linking:** Connect your ORCID account to an existing Data Manager profile at any time from your [user profile](user/user_edit.md#link-orcid).

---

## Update history

### ORCID linking and simpler template registration

<div style="font-size: smaller; color: rgba(122,122,122,1)">September 18th, 2025</div>

📌 Full [release notes (v1.11.0)](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.11.0) on GitHub.

Highlights:

- **ORCID linking:** Link your ORCID from your user profile — no need to re-register.
- **Simpler sample registration:** Download the batch template directly from the registration dialog.
- **Simpler measurement registration:** Pick your domain (proteomics or genomics) and download the template in one step.
- **Optional measurement name:** Both registration sheets now include a `Measurement Name` column for your internal lab identifier.
- **Raw data filtering:** Filter registered datasets by properties using the search field.
- **Filtered download URLs:** URL export now includes only the datasets matching your current filter.

### Metadata glossary

<div style="font-size: smaller; color: rgba(122,122,122,1)">September 18th, 2025</div>

- A new [Metadata glossary](metadata/concepts.md) explains every field with plain-language descriptions and example values.

### Faster sample and experiment updates

<div style="font-size: smaller; color: rgba(122,122,122,1)">June 10th, 2025</div>

- Sample and experiment updates now run in the background. A notification confirms when the process is complete.

### Background project creation

<div style="font-size: smaller; color: rgba(122,122,122,1)">March 4th, 2025</div>

- Project creation now runs in the background with progress notifications.

### Confounding variable support

<div style="font-size: smaller; color: rgba(122,122,122,1)">February 12th, 2025</div>

- **Confounding variables:** Track factors that might influence your results at the experiment and sample level.
- **Updated ontology search:** Terms now come from the improved [TIB Terminology Service](https://terminology.tib.eu/ts/api).
- **Measurement details:** Technical replicate information and sample pool names are now visible in the measurement overview.
- **Better metadata export:** Excel exports now include the ontology identifier (CURIE) alongside each human-readable label.

Full [release notes (v1.8.0)](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.8.0).

### Redesigned project summary

<div style="font-size: smaller; color: rgba(122,122,122,1)">November 14th, 2024</div>

- New project summary layout with easier access to project information.
- Spreadsheet templates now include helpful examples and validation tooltips.
- Templates are generated dynamically — always up to date.

### Excel support for sample batch registration

<div style="font-size: smaller; color: rgba(122,122,122,1)">October 23rd, 2024</div>

- Register and update sample batches with [Excel spreadsheets](batch/sample-batch.md).
- **RO-Crate export:** Download your project metadata as a [structured, machine-readable package](project/project_edit.md#download-project-metadata). Learn more about [RO-Crate](https://www.researchobject.org/ro-crate/).
- [Bug fixes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.5.0).

### Excel support for measurements

<div style="font-size: smaller; color: rgba(122,122,122,1)">September 4th, 2024</div>

- Register and update measurements with [Excel spreadsheets](measurement/measurement_introduction.md). TSV still supported.
- The sample field `Organism ID` has been renamed to `Biological Replicate` to better reflect its purpose.
- Connected to the [TIB Terminology Service](https://terminology.tib.eu) for standardised scientific vocabulary. Currently supported ontologies:

    | Abbreviation | Full name |
    |---|---|
    | **BAO** | Bio-assay Ontology |
    | **BTO** | Brenda Tissue Ontology |
    | **CHEBI** | Chemical Entities of Biological Interest |
    | **EDAM** | Bioinformatics operations, data types, formats, identifiers and topics |
    | **EFO** | Experimental Factor Ontology |
    | **ENVO** | Environmental Ontology |
    | **GO** | Gene Ontology |
    | **MI** | Molecular Interaction |
    | **MS** | PSI Mass Spectrometry Ontology |
    | **NCIT** | National Cancer Institute Thesaurus |
    | **PO** | Plant Ontology |

    Missing an ontology? [Submit a feature request](https://github.com/qbicsoftware/data-manager-app/issues/new/choose).

- Species terms come from [NCBI's tree of life](https://doi.org/10.1371/journal.pgen.1005912).
- [Bug fixes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.4.0).
