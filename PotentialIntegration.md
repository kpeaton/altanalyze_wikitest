# Useful Extensions to Consider #

### Visualization ###
  * RNA-Seq analysis: https://rnaseqlib.readthedocs.org/en/latest/
  * Network visualization: http://code.google.com/p/python-graph/w/list
  * Python graph-tool: http://projects.skewed.de/graph-tool/
  * RNA-Seq isoform visualization (requires Matplotlib and PyML) : http://splicegrapher.sourceforge.net/
  * Other: http://vermeulen.ca/python-graphics.html
  * Advanced table viewer: http://www.nemethi.de/tablelist/tablelist.html
  * Interactive heatmap, network and other in Orange: http://www.biolab.si/supp/bi-visprog/dicty/Heat%20Map.htm
  * Methylation-sequencing visualization: https://github.com/simonvh/fluff/blob/master/README.md
  * Interactive visualization: http://bokeh.pydata.org/
  * Biclustering: http://scikit-learn.org/stable/auto_examples/bicluster/plot_spectral_biclustering.html
  * Sircah: http://www.bork.embl.de/Sircah/gallery.html
  * Sub-pathway based python GSEA DiffPath: https://github.com/aditi9783/DiffPath

### Data Analysis ###
  * HTSeq: http://www-huber.embl.de/users/anders/HTSeq/doc/overview.html
  * Exon expression extraction: http://code.google.com/p/bedtools/
  * PCA and clustering: http://pyrorobotics.org/?page=PyroModuleAnalysis
  * RNA-Seq QC and visualization: http://code.google.com/p/rseqc/
  * RNA-Seq QC and visualization: https://confluence.broadinstitute.org/display/CGATools/RNA-SeQC/
  * Evaluate [ICA](http://en.m.wikipedia.org/wiki/Independent_component_analysis#section_2) for LineageProfiler
  * Genomic evaluation of qPCR primers: http://quwubin.cn/MFEprimer/
  * Databases for probe-level splicing anlayses: http://affymetrix2.bioinf.fbb.msu.ru/files.html
  * GEO data import: http://bcbio.wordpress.com/2010/01/02/automated-retrieval-of-expression-data-with-python-and-r/
  * Sweave for python: http://stackoverflow.com/questions/2161152/sweave-for-python
  * SplicingCompass in R: http://www.ichip.de/software/SplicingCompass.html
  * Pycogent for probabilist genomics: http://pycogent.org

note: Win32 and Win64 unofficial installers can be found here: http://www.lfd.uci.edu/~gohlke/pythonlibs/

# Visualization Software Installation Notes #

### python-graph (build Cytoscape like networks) ###
<ol>
<blockquote><li> easy_install python-graph-core </li>
<li> easy_install python-graph-dot (possible dependency) </li>
<li> install graphviz (dependency for dot and graphviz) </li>
<ul>
<li> install MacPorts (easy install for mac apps – from dmg) </li>
<li> sudo install graphviz </li>
</ul>
<li> ran example python-graph file and received a warning about trying to import the module gv. The module gv appears to be local to python graph and is called when graphviz is found in the indicated path (path is manually specified in the test code.) No graphviz folder containing a folder named python found. No solution on the Wiki for mac. </li>
<li> Tried to install pygraphviz (not sure if this is related) using easy_install, does not appear to be related. </li>
<li> stopped here… failed </li>
</ol></blockquote>

### pyGraphViz ###
<ol>
<blockquote><li> Saw at <a href='http://stackoverflow.com/questions/5639049/setting-graph-attributes-in-pygraph'>http://stackoverflow.com/questions/5639049/setting-graph-attributes-in-pygraph</a> that pyGraphViz can run virtually the same example and work without using the above python-graph… this worked! Use this instead (only dependency is graphviz and possibly dot – not sure). Need to test on PC and Linux. </li>
</ol></blockquote>

### MatPlotLib (make charts) ###
<ol>
<blockquote><li> Depends on numpy (already installed) </li>
<li> easy_install matplotlib… encountered several errors, but installed. As an alternative can install from: <a href='http://matplotlib.sourceforge.net'>http://matplotlib.sourceforge.net</a> (installs numpy) </li>
<li> Tried - <a href='http://www.thetechrepo.com/main-articles/465-how-to-create-a-graph-in-python'>http://www.thetechrepo.com/main-articles/465-how-to-create-a-graph-in-python</a> - worked great! </li>
<li> Tried the animation examples on the website and encountered a common error: </li>
<ul>
<li> File "/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/site-packages/matplotlib-1.1.0-py2.7-macosx-10.6-intel.egg/matplotlib/animation.py", line 248, in <i>blit_clear </li></i><li> a.figure.canvas.restore_region(bg_cache<a href='a.md'>a</a>) </li>
<li> AttributeError: 'FigureCanvasMac' object has no attribute 'restore_region' </li>
<li> No function restore_region in the class FigureCanvasMac in the module “backend_macosx.py” (only one that contains FigureCanvasMac). </li>
<li> After contacting the MatPlotLib community, discovered that setting blit=False will fix this problem.</li>
</ul>
</ol>
<h3>iGraph (directed networks with arrows)</h3>
<ol>
<li> Depends on Cairo for non-SVG based visualization (PNG, PDF) </li>
<li> amd64bit installer from: <a href='http://www.lfd.uci.edu/~gohlke/pythonlibs/'>http://www.lfd.uci.edu/~gohlke/pythonlibs/</a> </li>
<li> cairo dependencies from <a href='http://ftp.gnome.org/pub/gnome/binaries/win64/dependencies/'>http://ftp.gnome.org/pub/gnome/binaries/win64/dependencies/</a> as described here: <a href='http://www.cs.rhul.ac.uk/home/tamas/development/igraph/tutorial/install.html#installing-igraph'>http://www.cs.rhul.ac.uk/home/tamas/development/igraph/tutorial/install.html#installing-igraph</a> </li>
</ol>