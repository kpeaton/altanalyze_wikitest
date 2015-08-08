## AltAnalyze Software Update History ##

_note:_ For further details and explanation, see the associated sections in the full [online AltAnalyze documentation](http://www.altanalyze.org/help_main.htm).

### Version 2.0.9 Updates ###
In this version, we have added a number of new analysis methods to support comprehensive automated gene-expression, splicing, network and single-cell analyses. See the latest included software documentation for more details. Changes include:
  1. Multiple independent tools and workflows for single-cell gene expression and splicing analyses (Iterative Clustering and Driver Selection or ICDS).
  1. Support for junction count expression files provided by the Cancer Genome Atlas (TCGA).
  1. Support for the Affymetrix Human Transcriptome 2.0 (HTA2.0) array (gene expression and splicing analyses).
  1. [Heatmap](http://code.google.com/p/altanalyze/wiki/Heatmaps) pathway enrichment analysis and linkouts to gene annotations, TreeView, associated pathway gene-sets and networks.
  1. PCA on all genes not just differentially expressed produced (fast with implementation of SVD).
  1. Heatmap viewer allows for amplification of GeneSets or Ontology terms associated genes, via correlation analyses or restricted intra-correlation filtering or automated driver gene selection. Support for pasting lists of genes from Excel into this and other menus.
  1. Handling of zero non-log values in the input file (e.g., FPKMs).
  1. Gene Biotypes (e.g., TFs, kinases) added to go-elite, heatmap enrichment and other places.
  1. GO-Elite can be run by just pasting in genes.
  1. TreeView is downloaded with AltAnalyze and can be called from any heatmap with a button click for your results.
  1. Top represented genes from GO-Elite listed on the left of the heatmap.
  1. Annotation of the amount of variance explained by each PCA component and associated top PCA component genes (correlated and anti-correlated) identified.
  1. Optionally store gene signatures from PCA or heatmap analyses for later application elsewhere.
  1. If few hopach clusters are produced it actually will use the second level hopach results (e.g., for label 1000 and 1100, they will be considered 10 and 11 rather than 1).
  1. Novel reciprocal isoform percent spliced in (Ri-PSI) algorithm for getting high confidence alternative splicing events.
  1. Interactive Venn Diagram gene-set selection.
  1. Automatic visualization of the top 50 alternatively spliced genes with the AltExon viewer.
  1. Automatic gene interaction network visualization for all differentially expressed genes.
  1. Directory descriptor files added to all major result directories.
  1. Improved results viewer with additional graphs.
  1. Combination of all compendium LineageProfiler results with top term summaries.
  1. Online video [tutorials](Tutorials.md) and individual tutorials for each Additional Analyses features.

Bug fixes include:
  1. Various issues with the heatmap viewer and pathway enrichment and gene visualization fixed.
  1. Error with Venn Diagram maker and other visualization methods crashing after trying to use a second time.
  1. Ontology analysis (issue with GO-Slim corrected).
  1. Combat included libraries (fixed by the patsy developers)
  1. Issue with batch effects menu corrected (stuck in a loop)
  1. LineageProfiler should work better
  1. AltExon viewer bugs fixed
  1. Pasting in genes should remove carriage returns (network visualization and clustering).
  1. Errors with TFTarget import are fixed.
  1. MarkerFinder errors with non-workflow generated input datasets.

### Version 2.0.7 Updates ###
In this version, we have added a number of new analysis methods to support comprehensive automated gene-expression analysis as well as improved RNA-Seq analysis and filtering. Changes include:
  1. [Heatmap](http://code.google.com/p/altanalyze/wiki/Heatmaps) visualization of hierarchically clustered genes (significant and outlier).
  1. Principal Component Analysis and visualization.
  1. Independent Affymetrix RMA and RNA-Seq feature-level quality control plot visualization.
  1. LineageProfiler cell and tissue correlation analysis arrays and RNA-Seq expression detection platforms.
  1. WikiPathways visualization for selected or enriched GO-Elite pathways.
  1. Support for GO-Elite version 1.2.5 additional resources (e.g., transcription factor targets, microRNA targets, disease ontology, biomarkers, domains, KEGG, Pathway Commons). [Details here](http://genmapp.org/go_elite/help.htm#resources).
  1. Ability to perform clustering, LineageProfiler, pathway enrichment or pathway visualization independent from other functions.
  1. Moderated t-tests based on R's limma algorithm.
  1. Included support of RNA-Seq BED file annotations missing the 'chr' chromosome annotation.
  1. Added separate RNA-Seq filtering options for exons, junctions and genes.
  1. Fixed Gene Ontology annotation bug for gene-expression results.

### Version 2.0.6 Updates ###
In this version, we improve upon changes made in the previous release and supply several new methods and analysis support. Changes include:
  1. Improved gene expression detection and filtering for RNA-Seq (separate RPKM and read-count filtering for exons and junctions).
  1. Improved constitutive exon-detection methods (introduced in database version Ensembl 64).
  1. Support added for the Affymetrix [hGlue](hGlue.md) junction array
  1. New summary export result files (e.g., splicing-statistics for all analyzed features).
  1. New fully automated methods for AltAnalyze database creation (automated download of all necessary files - command-line only).
  1. Fixed several identified bugs from version 2.0.5 (e.g., problems with 3'array processing, Gene Ontology annotations, RNA-Seq import).

### Version 2.0.5 Updates ###
New program features, improved methods and critical fixes to RNA-seq exon bed building bug for Windows:
  1. Selection of multiple statistical p-value methods added (e.g., paired t-test, Mann Whitney) for all analyses (Section 2.4)
  1. New summary gene expression statistics file included (Section 2.5)
  1. Updated RNA-Seq gene-level RPKM calculations to provide more accurate gene expression estimates (Section 3.2)
  1. Gene expression estimates for RNA-Seq are now derived only from exon and not junction and exon expression (when applicable)
  1. Support of Affymetrix microRNA array annotation files added
  1. Protein coding potential and microRNA binding site annotations support added for conventional array data
  1. GO-Elite update, optimization and updated Ontology support
  1. Fixed import error on Windows machines for exon BED import from BEDTools

### Version 2.0.4 Updates ###
Critical fixes to bugs, resulting in program errors, introduced in version 2.03:
  1. Running source-code on a remote machine now working
  1. Independent analysis of exon only files (no junctions) now working
  1. All species RNA-Seq databases will now load properly
  1. More consistent results between exon only and exon with junction results (some novel exons missing or duplicated).
  1. RNA-Seq and junction array splicing-index results for GO-Elite analysis will be properly written (no resulting GO-Elite error).

### Version 2.0.3 Updates ###
New to version 2.03 AltAnalyze is support for both exon and junction RNASeq analysis, new functional annotations and normalization methods:
  1. Support for RNASeq exon expression import from TopHat & BioScope (Section 1.5)
  1. Support for platform independent exon/junction data in BED format (Section 1.5)
  1. New independently confirmed exon and junction event report file (Section 2.5)
  1. Updated species database support for RNASeq exon analyses (EnsMart62)
  1. Optional quantile or RPKM normalization for exons and junctions (Section 3.2)
  1. Addition of adjusted p-values for exon analyses (Section 3.2)
  1. Addition of non-coding and nonsense mediated decay annotations (Section 3.6)
  1. Identification of alternative poly-adenylation predictions (Section 3.5)
  1. Addition of UniProt domain/motif exon-overlap annotations (Section 3.6)
  1. Improved Ensembl gene function annotations (Section 3.7)
  1. Fixed Cytoscape installation and extraction problems for Windows.
  1. Automatic array recognition for version 4 format Affymetrix CEL files.
  1. Memory optimization for import and analysis.

### Version 2.02 Updates ###
  1. Improved data import
  1. Increased efficiency for datasets with many novel junction predictions (100k plus)
  1. Options for removing junctions with both ends mapping to introns.

### Version 2.01 Updates ###
New to version 2.01 AltAnalyze is support for junction aligned RNASeq data:
  1. Support of Junction .BED file analysis (Sections 1.5, 2.4, 3.2 and 6.2)
  1. Reciprocal junction analysis of RNASeq data (Section 2.4)
  1. Over 50 species now supported for RNASeq reciprocal junction analysis (http://code.google.com/p/altanalyze/wiki/SupportedSpecies)
  1. New miRNA target annotation databases added (Section 6.5)
  1. Allows analysis of genes without constitutive evidence (Section 3.4)
  1. Automatic analysis of up- and down-regulated genes by GO-Elite.
  1. New automated tools for developers to create & update databases (Section 6.7)
  1. New online RNASeq documentation (http://code.google.com/p/altanalyze)

### Version 1.1.6 Updates ###
New to version 1.16 AltAnalyze is support for alternative splicing array types and decreased memory requirements:
  1. Support of Affymetrix HJAY and MJAY arrays (Section 6.2)
  1. Combined reciprocal junction and exon analysis for junction arrays  (Section 2.3)
  1. Better memory handling for FIRMA and protein domain analysis
  1. Improved online support (http://code.google.com/p/altanalyze)

### Version 1.1.5 Updates ###
New to version 1.15 AltAnalyze are new splicing algorithm options, new array support and improved DomainGraph connectivity. The main new features are:
  1. Addition of FIRMA alternative exon analysis (Section 3.2)
  1. Alternative exon analysis support for the Affymetrix Gene 1.0 array  (Section 2.3)
  1. Universal import of 3rd party alternative exon results for analysis (Section 3.2)
  1. Restricted analysis of a pre-determined set of probe sets (Section 3.2)
  1. Bundled integration of Cytoscape and DomainGraph (Sections 2.2 and 8)
  1. Improved command-line options (Section 2.3)

### Version 1.1.4 Updates ###
Several features have been added to AltAnalyze version 1.14. Please review these if you have used previous versions of AltAnalyze, since the method in which gene expression is evaluated for both gene expression and alternative exon analyses has been updated and will affect your results. The main new features are:
  1. Updated Ensembl version 54 exon array annotations for constitutive gene probe sets (Section 3.4 and Section 6.2).
  1. Support for core probe set only gene expression calculation (Section 3.4)
  1. Improved filtering methods for gene expression data (Section 3.4).
  1. Addition of advanced gene expression analysis statistics (Section 3.2).
  1. Support for multi-group (>2) alternative exon analyses (Section 2.5).
  1. GO-Elite support for adjusted p-value filtering optional settings (Section 3.2).
  1. Improved automatic array type identification.
  1. More streamlined graphical user interface options.