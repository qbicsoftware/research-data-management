# Life Science Data Management

Behind every great research project should be great research data management!
Start your voyage towards a __FAIR__ and __Open Data__ future and include
the [data manager](https://rdm.qbic.uni-tuebingen.de/login) platform early on in your research!

## What's new?

### Confounding variable support
<div style="font-size: smaller; color: rgba(122,122,122,1)">February 12th, 2025 </div>

- Experimental design: The management of confounding variables on experiment and sample level is now possible
- Ontology: Ontology terms are now queried from TIB's new [APIv3](https://terminology.tib.eu/ts/api) by default, which uses the improved OLS4 backend
- Measurements: Technical replicate information is now shown for measurements
- Measurements: Sample pool names are now displayed in the measurement overview
- Metadata: Improved Excel file export that also displays the ontology terms CURIE

Check out the full [release notes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.8.0) on GitHub.

## Update notes

### New project summary layout
<div style="font-size: smaller; color: rgba(122,122,122,1)">November 14th, 2024 </div>

- A completely new design of the project summary, that targets many improvements for accessing and updating high level project information
- Enhances the spreadsheet templates with examples using what Microsoft calls [Input Messages](https://support.microsoft.com/en-us/office/more-on-data-validation-f38dee73-9900-4ca6-9301-8a5f6e1f0c4c) and links to further information resources
- Spreadsheet templates are no static documents anymore, but generated dynamically

### Excel spreadsheets now supported for sample batch registration
<div style="font-size: smaller; color: rgba(122,122,122,1)">October 23rd, 2024 </div>

- Sample Batches can now be registered and updated
  directly [with XLSX spreadsheets](batch/sample-batch.md).
- RO-Crate Export: The project summary information can now be [downloaded](project/project_edit.md#download-project-metadata) as an
  RO-Crate to your local filesystem within the project summary.
  For more information on RO-Crates visit [here](https://www.researchobject.org/ro-crate/).
- Some smaller [bug fixes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.5.0).

### Excel spreadsheets now supported for measurements
<div style="font-size: smaller; color: rgba(122,122,122,1)">September 4th, 2024 </div>

- Measurements can now be registered and updated
  directly [with XLSX spreadsheets](measurement/measurement_introduction.md). TSV is still
  supported.
- Sample metadata: the term `Organism ID` has been renamed to `Biological Replicate` to match its
  purpose of use.
- The data manager is now connected to the [TIB terminology service](https://terminology.tib.eu).  
  The [queried ontologies](ontology_search/ontology_search_introduction.md) are restricted to life science specific ones. You miss one? Please let us
  know and submit
  a [feature request](https://github.com/qbicsoftware/data-manager-app/issues/new/choose). Currently
  included ontologies are:
  - Bio-assay Ontology (__BAO__)
  - Brenda Tissue Ontology (__BTO__)
  - Chemical Entities of Biological Interest (__CHEBI__)
    Bioinformatics operations, data types, formats, identifiers and topics (__EDAM__)
  - Experimental Factor Ontology (__EFO__)
  - Environmental Factor Ontology (__ENVO__)
  - Gene Ontology (__GO__)
  - Molecular Interaction (__MI__)
  - PSI Mass Spectrometry Ontology (__MS__)
  - National Cancer Institute Thesaurus (__NCIT__)
  - Plant Ontology (__PO__)
- For
  species, [terms can be selected](ontology_search/ontology_search_introduction.md)
  from [NCBI's tree of life](https://doi.org/10.1371/journal.pgen.1005912).
- Some smaller [bug fixes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.4.0).
