# Instructions for Installing Pre-requisites for Brainhacking 101

## GitHub

### Software to install
 * git

### Ubuntu Linux
Type the following command at the terminal:

`sudo apt-get install -y git`

### CentOS/RHEL
Type the following command at the terminal:

`sudo yum install -y git`

### Mac OS X
Download the Xcode Command Line Tools [here](https://developer.apple.com/downloads/index.action) (you will need to obtain an Apple ID if you do not have one already).  Git is included as one of the tools.

## Python

### Software to install
 * Anaconda
 * Pip
 * IPython
 * Jupyter
 * Numpy
 * Scipy

You should download a scientific Python distribution such as Anaconda, which can be downloaded [here](https://www.continuum.io/downloads).
Anaconda comes with a useful command for managing packages (`conda`) that complements the conventional Python package manager (`pip`) well.
Installing some packages on Mac OS X is particularly difficult without using a Python distribution such as Anaconda.
The following installation commands assume the use of Anaconda, although you may also want to try out [Enthought Canopy](https://store.enthought.com/).

After you have installed Anaconda, install the Python package manager, IPython, Jupyter, and NumPy/SciPy by typing the following command at the terminal:

`conda install pip ipython jupyter numpy scipy`

The proceeding Nibabel, Nilearn, AWS classes assume that you have installed Python.

## Nibabel

Download Python if you have not already using the instructions above.  Then type the following at the terminal:

`pip install nibabel`

## Nilearn and Plotting

Download Python if you have not already using the instructions above.  Then type the following at the terminal:

`pip install -U --user nilearn`

## Neurodebian

Instructions for adding the Neurodebian repositories to Debian-based Linux distributions are [here](http://neuro.debian.net/).

Instructions for installing the Neurodebian Virtual Machine are [here](http://neuro.debian.net/vm.html).

## AWS

Download Python if you have not already using the instructions above.  Then type the following at the terminal:

`pip install boto starcluster awscli`
