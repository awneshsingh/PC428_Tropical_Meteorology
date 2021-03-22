# Python for PC428: Tropical Meteorology

Contact: [Dr. Awnesh Singh](mailto:awnesh.singh@usp.ac.fj)

[Pacific Centre for Environment and Sustainable Development (PaCE-SD)](http://pace.usp.ac.fj/), [The University of the South Pacific](http://www.usp.ac.fj), Suva, Fiji


## Table of Contents

- [Python](#python)
- [The Anaconda Python Distribution](#the-anaconda-python-distribution)
- [Installing the Anaconda Python Distribution](#installing-the-anaconda-Ppython-distribution)
- [Installation of Additional Libraries](#installation-of-additional-libraries)
- [Some Exercises](#some-exercises)
- [Remember...](#remember)


## Python

What is Python? Python is an open-source high-level programming language that lets you work more quickly and integrate your systems more effectively, and let you do sophisticated data analysis. Python is realesed in two versions: Python 2 and Python 3 and is available from [https://www.python.org/](https://www.python.org/). We shall use Python 3 version for this training. Python uses [several libraries](https://docs.python.org/3/library/) to perform a range of tasks, which needs to be installed seperately.

## The Anaconda Python Distribution

Anaconda is a Python-based data processing and scientific computing platform. It has built in many very useful third-party libraries. Installing Anaconda is equivalent to automatically installing Python and some commonly used libraries so it makes the installation so much easier than regular Python installation. If you don't install Anaconda, but instead only install Python from [https://www.python.org/](https://www.python.org/), you also need to use pip to install various libraries one by one. It is painful and you need to consider compatibility, thus it is highly recommended to directly install Anaconda.

## Installing the Anaconda Python Distribution
You will first need to to download (~662MB) and install the **Anaconda Python Distribution**. It is a completely free enterprise-ready Python distribution for large-scale data processing, predictive analytics, and scientific computing. It includes the python interpreter itself, the python standard library as well as a set of packages exposing data structures and methods for data manipulation and scientific computing and visualization. In particular, it provides [Numpy](http://www.numpy.org/), [Scipy](http://www.scipy.org/), [Pandas](http://pandas.pydata.org/), [Matplotlib](http://matplotlib.org/), [scikit-learn](http://scikit-learn.org/stable/), etc., i.e., all the main packages we will be using during the semester. The Anaconda Python distribution (select the version shipping with Python 3.7) should be downloaded for your platform (either 32-bit or 64-bit operating system) for the respective operating system (e.g., Windows) from [https://www.anaconda.com/distribution/](https://www.anaconda.com/distribution/). 

Execute the downloaded file and follow the instructions to install Anaconda **For me**. Once installed, the **Anaconda Documentation** webpage will open in your internet browser with instructions on **Getting started with Anaconda**. You will follow the instructions after you perform the tasks below. You can close the **Anaconda Cloud** webpage on the internet browser.

From the *Start* menu, right click on the **Anaconda Prompt** under **Anaconda (64-bit)** select *More* and click on *Run as administrator* (you may need administrator privileges).

Type the following at the terminal to update to the latest version of all pre-installed packages (the **$** sign represents the prompt, e.g., **(base) C:\Windows\system32>**) and press *Enter*:

```
$ conda update conda
```

Then type the following:

```
$ conda update anaconda
```

You also might want to install [pip](https://github.com/pypa/pip) to install packages from the [Python Package Index](http://pypi.python.org/pypi) by typing:

```
$ conda install pip
```

Now that you have installed these updates, return to the **Anaconda Documentation** webpage in your internet browser and follow the instructions on **Getting started with Anaconda**. You can use Python using several applications. We will be focussing on one application for the training: [Jupyter Notebook](https://jupyter.org/).

## Installation of Additional Libraries

Python uses libraries to perform specific tasks. Some of these librarires are alreay installed when you intall Anaconda using the procedure above. Type the following to see the list of libraries already installed:

```
$ conda list
```

When installing additional libraries below, select *y* when prompted by **Proceed ([y]/n)?**. Note that you may get a message that nothing needs to be installed **# All requested packages already installed.**

### netcdf4

[netcdf4](https://github.com/Unidata/netcdf4-python) allows you to read and write netcdf files (version 3 and 4 supported), install it by typing:

```
$ conda install netcdf4
```

<!---
### libjpeg
[libjpeg](https://pypi.python.org/pypi/jpeg4py/0.1.1) is a free library with functions for handling the JPEG image data format and be installed by typing:
```
$ brew install libjpeg
```
--->

### Basemap

**Basemap** is a graphic library for plotting (static, publication quality) geographical maps (see [http://matplotlib.org/basemap/](http://matplotlib.org/basemap/)). **Basemap** is available directly in **Anaconda** using the conda package manager, install by typing:

```
$ conda install basemap
```

### Seaborn

[seaborn](http://web.stanford.edu/~mwaskom/software/seaborn/) is a Python visualization library based on matplotlib. It provides a high-level interface for drawing attractive statistical graphics. You should be able to install it with ```conda``` as well:

```
$ conda install seaborn
```

### xarray

[xarray](https://github.com/xarray/xarray) is a library aimed at bringing the power of Pandas to multidimensional labelled arrays, such as the ones usually associated with geophysical quantities varying along time and space dimensions (e.g., [time, latitudes, longitudes], [time, level, latitudes, longitudes], etc.) and supports reading and writing netcdf files. It can be installed via `conda` by typing:

```
$ conda install xarray
```

<!---
### wget

GNU Wget (or just Wget, formerly Geturl, also written as its package name, wget) is a computer program that retrieves content from web servers. It is part of the GNU Project. Its name derives from World Wide Web and get. It supports downloading via the HTTP, HTTPS, and FTP protocols.

```
$ conda install -c anaconda wget=2.2
```
--->

### openpyxl

Excel is a popular and powerful spreadsheet application for Windows. The `openpyxl` module allows your Python programs to read and modify Excel spreadsheet files. It can be installed via `conda` by typing:

```
$ conda install openpyxl
```

### cartopy

Cartopy is a Python package designed for geospatial data processing in order to produce maps and other geospatial data analyses. Cartopy makes use of the powerful PROJ.4, NumPy and Shapely libraries and includes a programmatic interface built on top of Matplotlib for the creation of publication quality maps. Key features of cartopy are its object oriented projection definitions, and its ability to transform points, lines, vectors, polygons and images between those projections. You will find cartopy especially useful for large area / small scale data, where Cartesian assumptions of spherical data traditionally break down. If you’ve ever experienced a singularity at the pole or a cut-off at the dateline, it is likely you will appreciate cartopy’s unique features! The module can be installed via `conda` by typing:

```
$ conda install -c conda-forge cartopy
```

### eofs

eofs is a Python package for EOF analysis of spatial-temporal data. Using EOFs (empirical orthogonal functions) is a common technique to decompose a signal varying in time and space into a form that is easier to interpret in terms of spatial and temporal variance. eofs can be installed via `conda` by typing:

```
$ conda install -c conda-forge eofs
```

### And just to be sure ...

that you have all the necessary packages, type:

```
$ conda update --all
```

### To exit...
type

```
$ exit
```

## Jupyter Notebook

The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Uses include: data cleaning and transformation, numerical simulation, statistical modeling, data visualization, machine learning, and much more. 

You can open Jupyter Notebook using either of the following:
1. From the *Start* menu, click on **Anaconda3 (64-bit)** and select **Jupyter Notebook (Anaconda3)**. Jupyter Notebook will open in your default Internet Browser.
2. From the *Start* menu, click on **Anaconda Navigator (Anaconda3)**. A new window of Anaconda Navigator will open. Search for Jupyter Notebook and click on **Launch**. Jupyter Notebook will open in your default Internet Browser.


## Some Exercises

There are numerous Python exercises to try out fron the internet. Some of the good ones are listed below:


- [https://www.w3schools.com/python/default.asp](https://www.w3schools.com/python/default.asp) [preferred]
- [https://www.tutorialspoint.com/python3/index.htm](https://www.tutorialspoint.com/python3/index.htm)


## Remember...
 
Learning Python can be fun. But it is important to learn the very basics first before moving into more complex problems. The exercises above should help you learn the basics of Python and should prepare you well for data analysis later on. There are many Python forums that are helpful if you get stuck. And I am just an email away. Lets start coding! 
