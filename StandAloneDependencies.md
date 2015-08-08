## Optional AltAnalyze Dependencies to be Installed ##

The compiled versions of AltAnalyze (Windows, Mac OSX and Ubuntu) should run immediately after extraction, however, the source code implementations may require additional Python modules installed. These are:

  1. Required: Python version 2.3 or greater
  1. Graphical User Interface requirement: Tkinter
  1. WikiPathways API visualization: lxml
  1. Faster Fisher Exact Test: Scipy
  1. Visualization output files: Matplotlib, Numpy, Scipy
  1. PNG viewing in the GUI: Python Imaging Library (PIL) ImageTk
  1. Statistical libraries for Combat: Patsy and Pandas
  1. Network visualization in igraph: igraph and cairo

These libraries can be installed from source code or from installers provided by the open-source project websites.

To determine if a pre-compiled version of AltAnalyze is compatible with your operating system, download the program and double-click the executable file name "AltAnalyze". The program can also be initiated from a terminal command-line (e.g., "./AltAnalyze in Linux). Feel free to [contact us](ContactUs.md) about any problems.

### Instructions for Windows/Linux/Mac OS X ###

**Mac OS X**

By default, Mac OS X has Python installed along with Tkiner. Python version 2X should be default and used instead of python 3.

**Windows**

Install Python 2.7 from http://www.python.org. Tkinter is installed by default.

**Linux** (see Ubuntu below)

If python or tkinter is not installed, install Python 2.7 from http://www.python.org. Tkinter is installed by default. Test by typing `python` at the terminal and then `import tkinter`.

**Cross-Platform Installation Options**

Python and Tkinter are all that are needed for AltAnalyze to run, but other dependencies are required if you wish to visualize WikiPathways (suds, PIL), cluster or QC plots (Matplotlib, Numpy, Scipy) or speed up the Fisher Exact Test analysis (scipy). To install these, see the below instructions.

  1. **Install setuptools**: http://pypi.python.org/pypi/setuptools/
  1. **Install suds**: `sudo easy_install suds`
  1. **Install matplotlib**: `sudo easy_install matplotlib`
  1. **Install numpy**: `sudo easy_install numpy`
  1. **Install scipy**: `sudo easy_install scipy`
  1. **Install Imagetk**: `easy_install --find-links http://www.pythonware.com/products/pil/ Imaging`
  1. **Install patsy**: `sudo easy_install patsy`
  1. **Install pandas**: `sudo easy_install pandas`
  1. **Install fastcluster**: recommend install from source
  1. **Install igraph**: recommend installer
  1. **Install cairo**: recommend install from source (see INSTALL file or [here](http://code.google.com/p/altanalyze/wiki/PotentialIntegration#iGraph_(directed_networks_with_arrows)) for Windows users)
  1. **Install ordereddict (Python 2.6 or below) :** easy\_install ordereddict

### Instructions for Ubuntu ###

Adding support for python applications call Tk is particularly challenging on Ubuntu, since Python is installed but Tkinter is not. We recommend:

  1. _**Ensure all Ubuntu updates have been installed**_
  1. **Install Tkinter**: `apt-get install python-tk` _**(restart after)**_
  1. **Install setuptools**: `sudo apt-get install python-setuptools`
  1. **Install suds**: `sudo easy_install suds`
  1. **Install matplotlib**: `sudo apt-get install python-matplotlib`
  1. **Install numpy**: `sudo apt-get install python-numpy`
  1. **Install scipy**: `sudo apt-get install python-scipy`
  1. **Install Imagetk**: `sudo apt-get install python-imaging python-imaging-tk`
  1. **Install patsy**: `sudo easy_install patsy`
  1. **Install pandas**: `sudo easy_install pandas`
  1. **Install fastcluster**: `sudo easy_install fastcluster`

Note: Installing from source is necessary when apt-get or easy\_install does not properly obtain all dependent libraries. To install from source use these commands:
  * python setup.py build
  * sudo python setup.py install

For igraph, install as described [here](http://igraph.wikidot.com/installing-python-igraph-on-linux)
  * This will install to the default system python (default or python installed by apt-get). If installed via other means (e.g., from source to /usr/local/bin), you will need to sym link the igraph folder from the equivalent system python version to your local installed and use the command: export LD\_LIBRARY\_PATH=/usr/lib/ or export LD\_LIBRARY\_PATH=/usr/local/lib/ if igraph gives an ImportError.

_**Developers Only**_

Both PyInstaller and cx\_Freeze have been used to build AltAnalyze binary distributions. In general, PyInstaller works the best with the described patch for Ubuntu, whereas cx\_Freeze will work for some but not all Ubuntu releases and configurations (e.g., compatible with 10.04).

  * Install cx\_Freeze from source (problems with apt-get) _**(may require libssl-dev be installed)**_
  * OR download and extract PyInstaller 1.6 (requires this [patch](http://www.pyinstaller.org/ticket/339))
  * In the AltAnalyze main program directory (ensure .py files are in this root and not just Source\_code), run: python setup.py build
  * Paste the files in the 'build/exe.linux directory into the AltAnalyze main program folder.
  * Test the "AltAnalyze" executable file in a copy of the AltAnalyze directory prior to distribution.

## Creating Compilers (advanced) ##

If you wish to create your own compiled version of AltAnalyze for distribution to your users (e.g., custom versions or unsupported operating systems), install the above and be mindful of the following:

  1. Customization of the setup.py file may be required for inclusion or exclusion of OS specific libraries (dll files).
  1. See the setup.py script for run instructions on different operating systems.
  1. The suds package folder must exist in the Python site-packages folder (not just the egg - zip must be extracted).
  1. Issues with matplotlib external dependencies may occur (see existing setup.py files for details).
  1. Issues with conflicting dependencies may occur on some OSs resulting in strange errors during binary creations. These include: the python library six may need to be called as site-packages/six/six.py rather than the egg file.

## Potential Issues ##
  1. Pandas installs it's own dateutil which may cause errors to be displayed in the console and possibly other issues.
  1. Eggs are not well supported by py2exe: http://www.py2exe.org/index.cgi/ExeWithEggs