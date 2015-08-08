## Metabolomics Analysis in AltAnalyze ##

Metabolomics experiments typically produce quantitative values associated with chemical identifiers (PubChem, KEGGcompound, HMDB, ChEBI, CAS). AltAnalyze supports import and analysis of metabolomics data assuming:
  * IDs correspond to one of the above chemical ID systems
  * Quantitative values are non-zero (ideally log2)

Input IDs do not have to correspond to one of the above, but will if annotations and enrichment analyses are desired in AltAnalyze. Supported analyses include:
  1. Differential metabolite expression statistics (e.g., moderated t-test)
  1. Metabolite annotation (e.g., name, KEGG, WikiPathways)
  1. Sample classification (LineageProfiler)
  1. Marker prediction (MarkerFinder)
  1. Quantile and batch-effects normalization
  1. Hierarchical clustering
  1. 2D and 3D PCA
  1. Basic sample QC visualization
  1. Pathway enrichment analysis and visualization

### Data Import ###

To import data, simple select the **Vendor/data-type** as **Other ID** and the appropriate ID system under the menu **Select platform**. Proceed with the default or customized options.