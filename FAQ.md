# AltAnalyze Frequently Asked Questions #

### Main Analysis Options ###

  * [What operating systems is AltAnalyze compatible with?](CompatibleOS.md)
  * [Can I run AltAnalyze on a remote machine without using the graphical user interface?](CommandLineMode.md)
  * [How can I visualize splicing and domain level changes from AltAnalyze?](SpliceVisualization.md)
  * [What microarrays can AltAnalyze work with?](CompatibleArrays.md)
  * [Can AltAnalyze work with exon/junction data for an unsupported platform (e.g., custom array)?](SplicingForAnyPlatform.md)
  * [What is the difference between the splicing-index, FIRMA, MiDAS, Linear Regression and ASPIRE methods?](ScoringMethod.md)
  * [How can I annotate my splicing results from another program in AltAnalyze?](AnnotateExternal.md)

### Installing AltAnalyze ###

  * [Why Does AltAnalyze crash when trying to download the database when first run?](DBaseInstallationError.md)

### Data Analysis and Import ###
  * [What files do I need when analyzing Affymetrix arrays?](RequiredFiles.md)
  * [When I have dozens of samples in my study, how can I more easily assign the samples to groups than one by one?](ManualGroupsCompsCreation.md)
  * [What is the recommended cutoff for expressed genes with RNA-Seq?](RNASeqExpressionCutoffs.md)
  * [Why does AltAnalyze need to filter my data?](FilteringData.md)
  * [Should I calculate gene expression using constitutive or all mRNA aligning probests?](Constitutive_vs_all.md)
  * [How does a pair-wise alternative exon analysis differ from multiple group comparisons?](MultipleComparisons.md)
  * [Why do I need to define groups and comparisons?](GroupsAndComps.md)
  * [Why doesn't AltAnalyze run GO-Elite by default?](GOEliteDefault.md)
  * [Why does AltAnalyze download the Gene 1.0 transcript annotation file for Exon 1.0 array analyses?](GeneArrayCSVForExon.md)
  * [How can I remove probesets with sequence that aligns to multiple genomic loci from my analysis?](CrossHybProbesets.md)
  * [Can AltAnalyze return transcript cluster results instead of Ensembl for the Gene 1.0 array?](TranscriptClusterCenteredResults.md)
### Probeset Alignments and DomainGraph ###

  * [How do AltAnalyze probeset-to-gene and probeset-to-exon mappings differ from those in the Affymetrix annotation files?](ExonMappings.md)
  * [In AltAnalyze a probeset associated with an intron is predicted to alter protein domain composition of the protein, but in DomainGraph why don't I see the probeset?](DGIntronMapping.md)
  * [How do I start DomainGraph and what can I do in DomainGraph?](StartingDG.md)

### Interpreting Alternative Exon Results ###
  * [Why don't the folds and expression values from my RNA-seq experiment don't seem to match correctly?](RNASeqFoldsAndExpression.md)
  * [What is a constitutive exon/junction?](GeneExpCalculation.md)
  * [Which results should I validate?](ResultsVerification.md)
  * [If two probesets align to one exon and have opposite splicing changes, what does this mean?](OppositeMappings.md)
  * [What does the (+) and (-) mean proceeding a protein domain, miRNA binding site or protein identifier?](ProteinDirectionIndicator.md)
  * [What does the identifier E2-3 indicate and where does this annotation come from?](ExonRegionIDs.md)
  * [Where do the alternative splicing annotations provided in the column "exon annotations" come from?](ASAnnotations.md)
  * [What does the column "distal exon-region-ID" indicate?](DistalExonRegion.md)
  * [What is the adjusted fold versus the non-adjusted fold change?](AdjFoldChange.md)
  * [Why do all alternative exons have the indicator "exon-inclusion" in the column "event\_call"?](EventCall.md)
  * [How can I graph my splicing scores for all exons in a gene?](GraphingExonData.md)
  * [What is the difference between exon-level and gene-level alternative exon results?](ExonVsGene.md)
  * [When viewing AltAnalyze results in DomainGraph, why don't the identifiers match to my array/RNA-seq platform?](DomainGraphNonExon.md)

### Other ###
  * [Who are you and what's your deal?](AboutUs.md)