### _How can I remove probesets with sequence that aligns to multiple genomic loci from my analysis?_ ###


_**Answer**_: Whether you are using the graphical user interface or [command-line mode](CommandLineMode.md), you can choose to remove genomic cross-hybridizing probesets.

If you are working in the graphical user interface, you can eliminate these by selecting "Remove probesets with a large cross-hybridization score" option when selecting CEL files to analyze:

![http://www.genmapp.org/AltAnalyze/image/SelectCELfiles.jpg](http://www.genmapp.org/AltAnalyze/image/SelectCELfiles.jpg)

You can also do this in the [command-line](CommandLineMode.md) by adding the flag "--noxhyb yes" which instructs AltAnalyze to exclude cross-hybridizing probesets. These annotations are obtained from annotation files produced for the [MADS software](http://biogibbs.stanford.edu/~yxing/MADS/Annotation.html).

You can also do this yourself by downloading the Affymetrix probeset annotation file for your exon array (e.g., [HuEx-1\_0-st-v1.na31.mm9.probeset.csv](http://www.affymetrix.com/support/technical/byproduct.affx?product=huexon-st)) from the [Affymetrix website](http://www.affymetrix.com/support/technical/byproduct.affx?) and identifying probesets with several probes that cross-hybridize according to the column "number\_cross\_hyb\_probes".