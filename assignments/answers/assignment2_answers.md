### Answers for Assignment 2 - Conda, IPython, and Jupyter

Work through these tasks. *How to provided your answer is specificed in italics.* Turn in a single text file of your answers. Please name your file `2_first_last.txt` or `2_first_last.md` (substitute your first and last name).

Note 1: This assignment assumes you have already installed [Miniconda 3](https://conda.io/miniconda.html) (Miniconda for Python 3) and created an environment called `python3` (we did this in Lesson 4). If you installed Miniconda 2 (Miniconda for Python 2), you should probably delete it and install Miniconda 3. Miniconda 3 will still let you create environments using Python 2 if you need to.

Note 2: This assignment assumes you have completed Lesson 4. Since we ran out of time to complete the Python Crash Course in class, please go through this on your own. You could also watch last year's YouTube videos from Lesson 4.

#### A. Working with Conda

*Copy your terminal commands and output as your answers.*

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

6. Optional: If you are familiar with R, create an environment and install the R kernel using the instructions [here](https://irkernel.github.io).
7. Optional: If you are familiar with QIIME, create an environment and install QIIME using the instructions [here](http://qiime.org/install/install.html).

#### B. Python and IPython command-line interpreter

*Write your answers to #1 and #2. Copy your terminal commands and output as your answers for #3.*

1. Launch your `python3` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?

    *No, the first command produces an error because Python 3 requires parentheses around print commands.*

2. Launch your `python2` conda environment and find out which version of Python you are using. Then try to run the commands `print 'Hello, world'` and`print('Hello, world')`. Do they both work?

    *Yes, they both work because Python 2 is forward-compatible with the Python 3 print command.*

3. Pick 3 of the 8 sections in Data Types we covered in Lesson 4: booleans, numbers, strings, lists, tuples, arrays, sets, and dictionaries. Using the IPython interpreter in your `python3` environment, type and run the commands we used in those sections of Lesson 4.

    ```
    $ ipython
    Python 3.7.0 | packaged by conda-forge | (default, Aug 27 2018, 17:24:52) 
    Type 'copyright', 'credits' or 'license' for more information
    IPython 7.0.1 -- An enhanced Interactive Python. Type '?' for help.
    
    In [1]: a = True 
       ...: b = False                                                                                   
    
    In [2]: a == True                                                                                   
    Out[2]: True
    
    In [3]: b == True                                                                                   
    Out[3]: False
    
    In [4]: a or b                                                                                      
    Out[4]: True
    
    In [5]: a and b                                                                                     
    Out[5]: False
    
    In [6]: l = [0, 1, 1, 2, 3, 5, 8]                                                                   
    
    In [7]: m = [5, 2, 'a', 'xxx', True, [0, 1]]                                                        
    
    In [8]: l[0:3]                                                                                      
    Out[8]: [0, 1, 1]
    
    In [9]: m[4]                                                                                        
    Out[9]: True
    
    In [10]: m[4] = False                                                                               
    
    In [11]: m[4:]                                                                                      
    Out[11]: [False, [0, 1]]
    
    In [12]: n = (3, 5, 6)                                                                              
    
    In [13]: n[0]                                                                                       
    Out[13]: 3
    
    In [14]: n[0] = 2                                                                                   
    ---------------------------------------------------------------------------
    TypeError                                 Traceback (most recent call last)
    <ipython-input-14-21012a8fb940> in <module>
    ----> 1 n[0] = 2
    
    TypeError: 'tuple' object does not support item assignment
    ```

#### C. Working with Jupyter notebooks and Python basics

*Write your answers to #1 and #2. No need to turn anything in for #3.*

1. Launch your `python3` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?

    *You should be able to make a Python 3 notebook, and your Python version should be Python 3.7.x.*

2. Launch your `python2` conda environment and then launch the Jupyter notebook server. Which kinds of notebooks can you create? Open a Terminal within the notebook environment; what is your Python version?

    *You should be able to make a Python 2 notebook, and your Python version should be Python 2.7.x.*

3. Pick 1 of the 4 sections in Loops and Control Structures we covered in Lesson 4: boolean and comparison operations, if tests, while loops, and for loops. Using a Jupyter notebook in your `python3` environment, type the code from that section in one or more cells, then run those cells. Put a header above the code cell using a Markdown cell. Practice creating, deleting, and moving cells using the keyboard shortcuts.

    *(Run this code in a notebook, but don't turn it in.)*
