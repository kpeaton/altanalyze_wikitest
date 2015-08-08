## _What microarrays can AltAnalyze work with?_ ##

**_Answer_**: AltAnalyze can work with nearly any gene expression microarray (e.g., [Affymetrix](http://www.affymetrix.com), [Illumina](http://www.illumina.com/), [Agilent](http://agilent.com), [CodeLink](http://www.appliedmicroarrays.com/index.php?option=com_content&view=article&id=15&Itemid=23)) as well as RNASeq data. For all array and [RNASeq](RNASeq.md) platforms analyzed, AltAnalyze will perform a series of statistical analyses to assess differential gene expression and annotate these results with gene, pathway, Ontology and miRNA binding site predictions (see below). In addition, pathway and ontology over-representation can be automatically performed for differentially expressed genes (user-defined). When analyzing expression data from splicing sensitive platforms ([RNASeq](RNASeq.md), [Exon 1.0](http://www.affymetrix.com/support/technical/byproduct.affx?product=huexon-st), [Gene 1.0](http://www.affymetrix.com/support/technical/byproduct.affx?product=hugene-1_0-st-v1) or [Junction](JunctionArrays.md) arrays), several sophisticated alternative exon analyses are also available (see below). These analyses are also possible for unsupported array platforms (e.g., Affymetrix U133 array), by providing a mapped expression file for each sample ([see here](SplicingForAnyPlatform.md)).

### Supported Gene Expression Analyses ###

Several useful methods are available for analysis of both conventional and splicing-sensitive platforms in AltAnalyze. These include:
  1. Expression normalization of CEL files using the RMA algorithm through [APT](APT.md) (_Affymetrix Only_).
  1. Automated array type identification and download of associated library and annotation files (_Affymetrix Only_).
  1. Annotation of probeset-level results with gene annotations (symbol, description), Ensembl IDs, Gene Ontology, WikiPathways, genomic coordinates, microRNA binding site predictions and AltAnalyze custom cellular location (e.g., membrane/extracellular/nuclear) and function (e.g., GPCR subtype, transcript factor) annotations.
  1. Differential gene expresssion (fold, t-test p-value, f-test p-value, BH False Discovery Rate (FDR) p-values).
  1. Over-representation analysis using the [GO-Elite](GOElite.md) analysis module.

### Supported Alternative Exon Analyses ###
When analyzing several array and [RNASeq](RNASeq.md) platforms, alternative exon detection, annotation and over-representation methods are available. These include:
  1. Filtering of exon or junction features using either expression or detection p-values (DABG from [APT](APT.md) AltAnalyze output). For RNASeq, this includes specific cut-offs for exons and junctions, based on number of read-counts and exon/junction/gene-level RPKMs.
  1. Alternative exon differential expression using several optional [scoring methods](ScoringMethod.md).
  1. Splicing-event, alternative promoter and alternative polyadenylation predictions (available species only) and associated p-value calculation (t-test, f-test, permutation and FDR p-values).
  1. Comparison of exon-level versus reciprocal-junction results for independent confirmation ([RNASeq](RNASeq.md) and JunctionArray).
  1. Associated alternative isoform prediction (protein-level) and overall sequence differences (e.g., truncation, non-sense mediated decay, alternative N-terminus, alternative coding).
  1. Protein domain (InterPro) and protein feature (UniProt) composition differences (whole protein versus alternative exon overlapping).
  1. microRNA binding sites predictions overlapping with alternative-exons.
  1. Over-representation of alternative exons for: A) pathways, B) alternative domains and C) alternative microRNA binding sites.
  1. Protein/exon/transcript/domain/pathway visualization in DomainGraph.

For more information, see the full documentation at:

http://www.altanalyze.org/help_main.htm

or

http://code.google.com/p/altanalyze/w/list