# Instructions for Installing Pre-requisites for Brainhacking 101

The following sections contain instructions for downloading the software needed to participate in the Brainhack courses.  If you have any difficulties installing any packages, help will be available at the Brainhack Installfests.  If the following packages are unavailable for your platform or you do not wish to install the software, you can follow the tutorials by downloading only the X2Go client (instructions in the AWS section) and logging into an Amazon cloud instance.

## GitHub

### Software to install
 * git

### Debian/Ubuntu Linux
Type the following command in a terminal:

`sudo apt-get install -y git`

### CentOS/RHEL
Type the following command in a terminal:

`sudo yum install -y git`

### Mac OS X
Download the Xcode Command Line Tools [here](https://developer.apple.com/downloads/index.action) (you will need to obtain an Apple ID if you do not have one already).  Git is included as one of the tools. (If you have trouble making a secure connection to Apple, check for any anti-virus software that might be blocking web connections, such as Sophos.)

### Windows

Download Git for Windows [here](https://git-for-windows.github.io/).

## Python

### Software to install
 * Anaconda (Python 2.7)
 * Pip
 * IPython
 * Jupyter
 * Numpy
 * Scipy

You should download a scientific Python distribution such as Anaconda, which has binaries for Linux, Mac OS X, and Windows that can be found [here](https://www.continuum.io/downloads).  Make sure that you download a binary with Python 2.7 (not Python 3.4).
Anaconda comes with a useful command for managing packages (`conda`) that complements the conventional Python package manager (`pip`) well.
Installing some packages on Mac OS X is particularly difficult without using a Python distribution such as Anaconda.
The following installation commands assume the use of Anaconda, although you may also want to try out [Enthought Canopy](https://store.enthought.com/).

After you have installed Anaconda, install the Python package manager, IPython, Jupyter, and NumPy/SciPy by typing the following command in a terminal:

`conda install pip ipython jupyter numpy scipy`

The proceeding Nibabel, Nilearn, AWS classes assume that you have installed Python.

## Nibabel

Download Python if you have not already using the instructions above.  Then type the following in a terminal:

`pip install nibabel`

## Nilearn and Plotting

Download Python and nibabel if you have not already using the instructions above.  Then type the following in a terminal:

```
pip install scikit-learn matplotlib
pip install -U --user nilearn
```

## Neurodebian

### Software to install (for VM)
 * Virtualbox

Instructions for adding the Neurodebian repositories to Debian-based Linux distributions are [here](http://neuro.debian.net/).

Downloads for Virtualbox (needed to import the Neurodebian Virtual Machine) can be found [here](https://www.virtualbox.org/wiki/Downloads).

Instructions for installing the Neurodebian Virtual Machine are [here](http://neuro.debian.net/vm.html).

## AWS

### Software to install
 * AWS Command Line Interface
 * Boto
 * Starcluster
 * X2Go Client
 * Cyberduck (or CloudExplorer for Linux users)

Download Python if you have not already using the instructions above.  Then type the following in a terminal to install the AWS Command Line Interface, boto and Starcluster:

`pip install awscli boto starcluster`

You will also need to configure the AWS CLI by following the instructions [here](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html).

X2Go will allow you to pull up a desktop session on a running instance of an Amazon Machine Image.  To install the the X2Go client for Linux, Mac OS X, or Windows, follow the instructions [here](http://wiki.x2go.org/doku.php/doc:installation:x2goclient).

**Note for OS X: We have encountered difficulties with X2Go and keyboard mappings when using older versions of Apple X11.  If you come across such issues (i.e., control keys not working), try updating to the latest version of XQuartz using [this link](http://xquartz.macosforge.org/landing/).**

Cyberduck will allow you to browse Amazon S3 buckets (storage areas for files).  You can download Cyberduck for Mac OS X and Windows [here](https://cyberduck.io/).

Linux users can use CloudExplorer.  To install Cloud Explorer, first install its dependencies:

### Debian/Ubuntu Linux

```
sudo apt-get install openjdk-8-jre openjdk-8-jdk ant
```

### CentOS/RHEL

```
sudo yum -y install git java-1.8-openjdk java-1.8.0-openjdk-devel ant
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

Then type the following commands in a terminal:

```
git clone https://github.com/rusher81572/cloudExplorer.git
cd cloudExplorer
ant
```

To start CloudExplorer, make sure that you are within the *cloudExplorer* directory and then type:

`java -jar dist/CloudExplorer.jar`
