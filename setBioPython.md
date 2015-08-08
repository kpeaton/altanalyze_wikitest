## Installation Instructions for BioPython ##

Although the typical AltAnalyze user will not need to install any additional python libraries, even if running python directly from the source code, users and developers wishing to customize or build databases (independent of Official releases) will need to install certain libraries:

  1. Python 2.7.1
  1. Numpy
  1. C compiler (Mac and some Linux)
  1. BioPython

Numpy and a C compiler are required for BioPython installation and not for other AltAnalyze functionality. With installation of Numpy, additional installation of a C compiler is not needed for Windows. BioPython itself is required for sequence analysis modules for protein prediction from mRNAs with no annotated protein sequence.

### Installation on Mac OS X ###
  1. Install Python: Although python is installed by default on the Mac, this version has certain compatibility issues that will require you to install a new version from Python. We recommend Python 2.7.1 (32 bit or 64 bit) http://www.python.org/download/releases/2.7.1/
  1. Install setuptools for your OS and processor architecture from: http://pypi.python.org/pypi/setuptools. Follow the instructions to install by Terminal. This will allow you to run easy\_install by command line.
  1. Install Numpy: Select the appropriate download from Source Forge http://sourceforge.net/projects/numpy/files/NumPy/ or through [easy\_install](http://pypi.python.org/pypi/setuptools)
  1. Install C compiler: It is recommended to install xCode from Apple. xCode is a large installation (3.6GB download - 10GB installed).
  1. Install BioPython: In a terminal window type "easy\_install biopython". If you receive a warning, repeat the command, as intermittent issues can cause transient errors.


### Installation on Windows ###
  1. Install Python: We recommend Python 2.7.1 (32 bit or 64 bit) http://www.python.org/download/releases/2.7.1/
  1. Set Python path: See the [following link](SetPythonPATH.md).
  1. Install Numpy: Select the appropriate download from http://www.lfd.uci.edu/~gohlke/pythonlibs/
  1. Install BioPython: Select the appropriate download from http://www.lfd.uci.edu/~gohlke/pythonlibs/

Once complete, you will be ready to perform database installations. For further details, [proceed here](BuildingDatabases.md).