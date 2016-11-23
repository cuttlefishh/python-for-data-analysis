## Lesson 2 - Conda, IPython, and Jupyter Notebooks

### Installing Miniconda and working with Conda

_Conda is an open source package management system and environment management system for installing multiple versions of software packages and their dependencies and switching easily between them. It works on Linux, OS X and Windows, and was created for Python programs but can package and distribute any software._ -- <http://conda.pydata.org/docs/>

First, install miniconda3: <http://conda.pydata.org/miniconda.html>. By default, environments you create will use Python 3, but you can specify Python 2 if required.

Then, create a conda environment. Let's make an environment called `python3` for this class that includes Python 3 and Jupyter. 

```
conda create -n python3 python=3 jupyter
```

To activate the environment:

```
source activate python3
```

To deactivate the environment:

```
source deactivate
```

To delete an environment:

```
conda env remove -n myenv
```

After you activate your environment, you can install additional packages to that environment using `conda install`:

```
conda install pandas
```

If the package isn't available from conda, try `pip install`:

```
pip install tabview
```

List the environments on your system:

```
conda env list
```

List the packages in your current environment:

```
conda list
```

### Python and IPython command-line interpreter

Demonstration.

### Working with Jupyter notebooks and Python basics

lesson2.ipynb

### Assignment for Lesson 2

**Installing Miniconda and working with Conda**

1. Make an environment called `python2` that's identical to your `python3` environment but using Python 2.
2. Practice activating and deactivating conda environments.
3. Use `conda install` and `pip install` to install additional packages to your environment.
4. List your conda environments.
5. List the packages installed in one of your environments.
6. Optional: If you are familiar with R, create an environment and install the R kernel using the instructions [here](https://www.continuum.io/blog/developer/jupyter-and-conda-r).
7. Optional: If you are familiar with QIIME, create an environment and install QIIME using the instructions [here](http://qiime.org/install/install.html).

**Python and IPython command-line interpreter**

1. Launch your `python3` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?
2. Launch your `python2` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?

**Working with Jupyter notebooks and Python basics**

1. Launch your `python3` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment and determine your Python version.
2. Launch your `python2` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment and determine your Python version.
