---
date: 2020-07-01 
layout: post
title:  Start Here
subtitle: Learn Python For Free
description: Install Python
image: /assets/img/startHere.png
optimized_image: /assets/img/startHere.png
category: tutorial
author: henry
---

This post is to answer the biggest question in Data Science.....Where do I Start???


**Step 0** 
The IPython notebook runs in the browser, and works best in Google Chrome. You probably want to use Chrome for this

## Recommended Method: Anaconda
![image]({{ site.baseurl }}/assets/img/ana.PNG)

The Anaconda Python distribution is an easily-installable bundle of Python and many of the libraries used throughout this site. Unless you have a good reason not to, we recommend that you use Anaconda.

### Mac/Linux users
1. Download the [appropriate version](https://docs.anaconda.com/anaconda/install/) of Anaconda
1. Follow the instructions on that page to run the installer
1. Test it out: open a terminal window, and type ``python``, you should see something like
```
Python 2.7.5 |Anaconda 1.6.1 (x86_64)| (default, Jun 28 2013, 22:20:13) 
```
If `Anaconda` doesn't appear on the first line, you are using a different version of Python. See the troubleshooting section below.

1. Test out the IPython notebook: open a Terminal window, and type `ipython notebook`. A new browser window should pop up. 
1. Click `New Notebook` to create a new notebook file
1. Update IPython to the newest version by typing `conda update ipython` at the command line

### Windows Users
1. Download the [appropriate version](https://docs.anaconda.com/anaconda/install/) of Anaconda
1. Follow the instructions on that page to run the installer. This will create a directory at `C:\Anaconda`
1. Test it out: start the Anaconda launcher, in the Start menu. Start the IPython notebook. A new browser window should open. 
1. Click `New Notebook`, which should open a new page.
1. Update IPython to the newest version by opening a command prompt, and typing `conda update ipython`

If you did not add Anaconda to your path, be sure to use the full path to the python and ipython executables, such as `/anaconda/bin/python`.

## Installing additional libraries
Anaconda includes most of the libraries we will use in this course, but you will need to install a few extra ones:

1. [BeautifulSoup](http://www.crummy.com/software/BeautifulSoup/)
1. [Pandas](https://pandas.pydata.org/)
1. [Scipy](https://www.scipy.org/getting-started.html)
1. [SStatsmodels](https://www.statsmodels.org/stable/index.html)
1. [Matplotlib](https://matplotlib.org/)
1. [Scikit Learn](https://scikit-learn.org/stable/)
1. [TensorFlow](https://www.tensorflow.org/)
1. [Seaborn](http://web.stanford.edu/~mwaskom/software/seaborn/)
1. [NumPy](https://numpy.org/)
1. [Keras](https://keras.io/)
1. [Plotly](https://plotly.com/)
1. [PyQuery](https://pythonhosted.org/pyquery/)

The recommended way to install these packages is to run `pip install BeautifulSoup` on the command line. If this doesn't work, you can download the source code, and run `python setup.py install` from the source code directory. On Unix machines, either of these commands may require `sudo` (i.e. `sudo pip install...` or `sudo python`)

## Opening IPython Notebooks
To view an IPython notebook, you must first start the IPython notebook server in the directory where the file lives. Simply navigate to this directory at the command prompt, and type `ipython notebook`. This will open a browser window, listing all the `ipynb` files in that directory.

## Updating from older Anaconda versions
You can easily update to the latest Anaconda version by updating conda, then Anaconda as follows:

```
conda update conda
conda update anaconda
```

## Troubleshooting

**Problem**
When you start python, you don't see a line like `Python 2.7.5 |Anaconda 1.6.1 (x86_64)|`. You are using a Mac or Linux computer

**Reason**
You are most likely running a different version of Python, and need to modify your Path (the list of directories your computer looks through to find programs). 

**Solution**
Find a file like `.bash_profile`, `.bashrc`, or `.profile`. Open the file in a text editor, and add a line at this line at the end: `export PATH="$HOME/anaconda/bin:$PATH"`. Close the file, open a new terminal window, type `source ~/.profile` (or whatever file you just edited). Type `which python` -- you should see a path that points to the anaconda directory. If so, running `python` should load the proper version

If this doesn't work (typing `which python` doesn't point to anaconda), you might be using a different shell. Type `echo $SHELL`. If this isn't `bash`, you need to edit a different startup file (for example, if if `echo $SHELL` gives `$csh`, you need to edit your `.cshrc` file. The syntax for this file is slightly different: `set PATH = ($HOME/anaconda/bin $PATH)`
***

**Problem**
You are running the right version of python (see above item), but are unable to import numpy. 

**Reason**
You are probably loading a different copy of numpy that is incompatible with Anaconda

**Solution**
See the above item to find your `.bash_profile`, `.profile`, or `.bashrc` file. Open it, and add the line `unset PYTHONPATH` at the end. Close the file, open a new terminal window, type `source ~/.profile` (or whatever file you just edited), and try again.
***

**Problem**
Under Windows, you receive an error message similar to the following: "'pip' is not recognized as an internal or external command, operable program or batch file."

**Reason**
The correct Anaconda paths might not be present in your PATH variable, or Anaconda might not have installed correctly.

**Solution**
Ensure the Anaconda directories to your path environment variable ("\Anaconda" and "\Anaconda\Scripts").  See [this page](http://superuser.com/questions/284342/what-are-path-and-other-environment-variables-and-how-can-i-set-or-use-them) for details.

If this does not correct the problem, reinstall Anaconda.

**Problem**
'pip' is not recognized as an internal or external command,operable program or batch file.

**Solution**
![image]({{ site.baseurl }}/assets/img/piperror.PNG)

**Problem**
ERROR: Could not install packages due to an EnvironmentError: [Errno 13] Permission denied:

**Solution**
![image]({{ site.baseurl }}/assets/img/pipdenied.PNG)



