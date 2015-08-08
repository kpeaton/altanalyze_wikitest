# Sample Junction BED files #

Junction.bed and exon.bed files produced from RNA-seq alignment of Illumina sequence reads for four biological samples are provided below using TopHat with known and novel discovery allowed (version 1.2.0). These samples correspond to:
  1. Human embryonic stem cells
  1. Derived neural precursors

These files are available in a zip compressed archive [here](http://altanalyze.org/hESC_differentiation_RNASeq.zip).

### Details ###
Sample data was obtained from NCBI's now discontinued Sequence Read Archive (http://www.ncbi.nlm.nih.gov/sra) for the entries [SRS011896](http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?sample=SRS011896), [SRS011898](http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?sample=SRS011898), [SRS011900](http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?sample=SRS011900) and [SRS011902](http://trace.ncbi.nlm.nih.gov/Traces/sra/sra.cgi?sample=SRS011902). _**Note: SRA is in the process of being discontinued, hence, FASTQ files may be unavailable.**_

For each of these samples, multiple sequence read files were downloaded and concatenated in FASTQ format. TopHat was run allowing for novel junction discovery and default settings as described [here](TopHat.md). Junction results were obtained directly from TopHat, while exon read counts were obtained using BEDTools as described [here](BEDTools.md). An overview of how to build AltAnalyze RNA-seq input files can be found [here](ObtainingRNASeqInputs.md).

To load in AltAnalyze, download [version 2.0](http://code.google.com/p/altanalyze/downloads/list?can=2&q=version+2.02), extract and start the software, select the species database for "Homo sapiens" and proceed to "Process Junction Files".