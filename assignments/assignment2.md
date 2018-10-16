### Assignment 2 - Conda, IPython, and Jupyter

Work through these tasks. *How to provided your answer is specificed in italics.* Turn in a single text file of your answers. Please name your file `2_first_last.txt` or `2_first_last.md` (substitute your first and last name).

Note 1: This assignment assumes you have already installed [Miniconda 3](https://conda.io/miniconda.html) (Miniconda for Python 3) and created an environment called `python3` (we did this in Lesson 4). If you installed Miniconda 2 (Miniconda for Python 2), you should probably delete it and install Miniconda 3. Miniconda 3 will still let you create environments using Python 2 if you need to.

Note 2: This assignment assumes you have completed Lesson 4. Since we ran out of time to complete the Python Crash Course in class, please go through this on your own. You could also watch last year's YouTube videos from Lesson 4.

#### A. Working with Conda

*Copy your terminal commands and output as your answers.*

1. Make a conda environment called `python2` that's identical to your `python3` environment except it uses Python 2.
2. Practice activating and deactivating conda environments.
3. Use `conda install` and `pip install` to install additional packages to your environment.
4. List your conda environments.
5. List the packages installed in one of your environments.
6. Optional: If you are familiar with R, create an environment and install the R kernel using the instructions [here](https://irkernel.github.io).
7. Optional: If you are familiar with QIIME, create an environment and install QIIME using the instructions [here](http://qiime.org/install/install.html).

#### B. IPython command-line interpreter and Python basics

*Write your answers to #1 and #2. Copy your terminal commands and output as your answers for #3.*

1. Activate your `python2` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?
2. Activate your `python3` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?
3. Pick 3 of the 8 sections in Data Types we covered in Lesson 4: booleans, numbers, strings, lists, tuples, arrays, sets, and dictionaries. Using the IPython interpreter in your `python3` environment, type and run the commands we used in those sections of Lesson 4.

#### C. Working with Jupyter notebooks

*Write your answers to #1 and #2. No need to turn anything in for #3.*

1. Activate your `python2` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?
2. Activate your `python3` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?
3. Pick 1 of the 4 sections in Loops and Control Structures we covered in Lesson 4: boolean and comparison operations, if tests, while loops, and for loops. Using a Jupyter notebook in your `python3` environment, type the code from that section in one or more cells, then run those cells. Put a header above the code cell using a Markdown cell. Practice creating, deleting, and moving cells using the keyboard shortcuts.
