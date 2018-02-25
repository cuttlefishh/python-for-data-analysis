### Answers for Assignment 2 - Bash, Conda, IPython, and Jupyter

Work through these tasks. For section A, copy your history containing the commands you executed for this section. For sections B and C, you don't need to turn in any commands or code; just provide your answers to the questions. Turn in a single text file of your answers. Please name your file `2_first_last.txt` or `2_first_last.md` (substitute your first and last name).

Note: This assignment assumes you have already installed [Miniconda 3](https://conda.io/miniconda.html) (Miniconda for Python 3) and created an environment called `python3` (we did this in Lesson 4). If you installed Miniconda 2 (Miniconda for Python 2), you should probably delete it and install Miniconda 3. Miniconda 3 will still let you create environments using Python 2 if you need to.

#### A. Working with Conda

1. Make a conda environment called `python2` that's identical to your `python3` environment except it uses Python 2.

        $ conda create -n python2 python=2 jupyter

2. Practice activating and deactivating conda environments.

        $ source activate python2
        
3. Use `conda install` and `pip install` to install additional packages to your environment.

        $ conda install pandas
        $ pip install tabview

4. List your conda environments.

        $ conda env list
        $ conda info --envs

5. List the packages installed in one of your environments.

        $ conda list

6. Optional: If you are familiar with R, create an environment and install the R kernel using the instructions [here](https://www.continuum.io/blog/developer/jupyter-and-conda-r).
7. Optional: If you are familiar with QIIME, create an environment and install QIIME using the instructions [here](http://qiime.org/install/install.html).

#### B. Python and IPython command-line interpreter

1. Launch your `python3` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?

    *No, the first command produces an error because Python 3 requires parentheses around print commands.*

2. Launch your `python2` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?

    *Yes, they both work because Python 2 is forward-compatible with the Python 3 print command.*

#### C. Working with Jupyter notebooks and Python basics

1. Launch your `python3` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?

    *You should be able to make a Python 3 notebook, and your Python version should be Python 3.6.x.*

2. Launch your `python2` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?

    *You should be able to make a Python 2 notebook, and your Python version should be Python 2.7.x.*
