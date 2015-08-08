## Introduction ##

BEDTools is a suite of open-source utilities for analyzing genomic sequence and coverage from various file types, including BED, SAM and BAM files. BEDTools can be easily compiled on Unix, Linux and Mac OS X operating systems. Directions for installation on Windows can be found [here](http://bcc.bx.psu.edu/course/install-bedtools.html).


## Details ##

See the [BEDTools website](http://code.google.com/p/bedtools/) for more information.

### Usage with AltAnalyze ###

After installation of BEDTools, AltAnalyze users will need to call the utility bamToBed (recognized on Unix systems once BEDTools has been added to the local or global .bashrc file). The file accepted\_hits.bam is produced with each TopHat run in the same output directory as the junction BED file.

In the below example, "hESC\_differentiation\_exons.bed" is produced by AltAnalyze prior to running BEDTools ([see instructions here](BAMtoBED.md)), containing all known mRNA exon region coordinates from Ensembl/UCSC and all novel exon coordinates indicated from the TopHat junction BED results. These methods should work equivalently for non-TopHat produced BAM files, however, additional sorting of the BAM file may be required (e.g., SAMTools).

_Build Exon BED file from BAM_

**For a Single BAM File**
```
bamToBed -i accepted_hits.bam -split| coverageBed -a stdin -b /home/user/BAMtoBED/Hs_cancer_exons.bed > /home/user/RNASeqStudy/Sample1/day0_s1__exons.bed
```

**For Many BAM Files (one per folder)**

```
for f in */accepted_hits.bam; do parentdir=`dirname $f`;   parentdirname=`basename $parentdir`; bamToBed -i $f -split| coverageBed -a stdin -b Hs_cancer_exons.bed > ${parentdirname}__exon.bed; done
```

This will loop through every folder in the current directory, find the accepted\_hits.bam file and name the resulting exon.bed file as "folder\_name"exon.bed. Thus, you can obtain all exon.bed files with this single command.