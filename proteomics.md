## Proteomics Analysis in AltAnalyze ##

Proteomics experiments typically produce quantitative values associated with protein, peptide or gene identifiers. AltAnalyze supports import and analysis of proteomics data assuming:
  * IDs correspond to any of the many supported input ID systems
  * Quantitative values are non-zero (ideally log2)

Input IDs do not have to correspond to one of the above, but will if annotations and enrichment analyses are desired in AltAnalyze. Supported analyses include:
  1. Differential protein expression statistics (e.g., moderated t-test)
  1. Protein/gene annotation (e.g., name, Pathways, Ontologies)
  1. Sample classification (LineageProfiler)
  1. Marker prediction (MarkerFinder)
  1. Quantile and batch-effects normalization
  1. Hierarchical clustering
  1. 2D and 3D PCA
  1. Basic sample QC visualization
  1. Pathway enrichment analysis and visualization

### Data Import ###

To import data, simple select the **Vendor/data-type** as **Other ID** and the appropriate ID system under the menu **Select platform**. Proceed with the default or customized options.