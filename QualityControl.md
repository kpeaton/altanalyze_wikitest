## Quality Control Analyses in AltAnalyze ##

Several quality control metrics are applied in AltAnalyze to identify putative outlier samples. The main output of all of these analyses are PDF and PNG image files output to the results directory under the folder **` DataPlots `**. A detailed description of these methods is provided [here](http://www.altanalyze.org/help.htm#QC).

### Affymetrix ###

  1. Distribution of normalized log2 probeset intensity values
  1. Mean raw signal intensities of each array
  1. Mean absolute deviation (MAD) of the RMA residuals for each array

### RNA-Seq ###

  1. Distribution of log2 read-counts (exon and junction)
  1. Feature-level box-plots for the distribution of exon, junction and intron read-counts
  1. Total number of reads for each sample, broken down by exon, junction and intron aligning

### All Platforms ###

  1. [Hierarchical clustering](Heatmaps.md) of significant genes and outliers
  1. Principal Component Analysis of samples (significant genes)
  1. Cell/tissue characterization of each sample (LineageProfiler)