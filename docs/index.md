# Life Science Data Management

Behind every great research project should be great research data management!
Start your voyage towards a __FAIR__ and __Open Data__ future and include
the [data manager](https://rdm.qbic.uni-tuebingen.de/login) platform early on in your research!

## What's new?

### Excel spreadsheets now supported for sample batch registration
<div style="font-size: smaller; color: rgba(122,122,122,1)">October 23rd, 2024 </div>

- Sample Batches can now be registered and updated
  directly [with XLSX spreadsheets](batch/sample-batch.md).
- RO-Crate Export: The project summary information can now be [downloaded](project/project_edit.md#download-project-metadata) as an
  RO-Crate to your local filesystem within the project summary.
  For more information on RO-Crates visit [here](https://www.researchobject.org/ro-crate/).
- Some smaller [bug fixes](https://github.com/qbicsoftware/data-manager-app/releases/tag/1.5.0).

## Update notes

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
