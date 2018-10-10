# Python for Data Analysis

Course in data science. Learn to analyze data of all types using the Python programming language. No programming experience is necessary.

Quick links: [📁 lessons](https://github.com/cuttlefishh/python-for-data-analysis/tree/master/lessons)  [⏬ Lesson Schedule](https://github.com/cuttlefishh/python-for-data-analysis#lesson-schedule)

Software covered:

* Python 3
* IPython environment and Jupyter notebooks
* Conda for package management and virtual environments

Course topics include:

* The UNIX command line
* Fundamentals of Python and its data types
* Data analysis packages Numpy and Pandas
* Plotting packages Matplotlib and Seaborn
* Statistics
* Regular expressions
* Interactive visualization
* Modules and classes
* Git and GitHub

## Instructor

* Luke Thompson, Ph.D.
* Lecturer at Scripps Institution of Oceanography, Assistant Professor at NOAA Northern Gulf Institute
* Email: luke@ucsd.edu
* Office hours by appointment
* Pages: [GitHub](https://github.com/cuttlefishh), [Google Scholar](https://scholar.google.com/citations?user=kggNWsMAAAAJ), [NOAA profile](https://swfsc.noaa.gov/staff.aspx?id=22360)

## Meetings

* Course number: SIOC 209
* Quarter: Fall 2018-19
* Meeting time: M/W 11:00-12:20
* First and last day of class: October 1-December 5 (20 lessons)
* Location and door code: ask instructor

## Online Content

* GitHub repository: <https://github.com/cuttlefishh/python-for-data-analysis>
* YouTube channel: <https://www.youtube.com/channel/UCVZrIrWtcvTzYlrNx7RcDyg>

## Textbooks

* [_Learn Python 3 the Hard Way_](https://learnpythonthehardway.org/python3/) by Zed Shaw (Addison-Wesley) -- Step-by-step introduction to Python with no prior knowledge assumed; includes appendix Command Line Crash Course.
* [_Learning Python_](http://proquest.safaribooksonline.com/book/programming/python/9781449355722) 3rd Edition by Mark Lutz (O'Reilly) --  Optional; more traditional introduction to Python as a computer language.
* [_Python for Data Analysis_](http://proquest.safaribooksonline.com/book/programming/python/9781491957653) 2nd Edition by Wes McKinney (O'Reilly) -- Manual focused on Pandas, the popular Python package for data analysis, by its creator. GitHub page: <https://github.com/wesm/pydata-book>.

*O'Reilly Media titles are free to UCSD affiliates with [Safari Books Online](http://proquest.safaribooksonline.com/?uicode=ucsd).*

## Additional Materials

### Command Line Resources

* [Git for Windows](https://git-for-windows.github.io) -- BASH emulator and Git software for Windows
* [Learning the Shell](http://www.linuxcommand.org/learning_the_shell.php) -- Great intro to the Unix shell
* [Unix Tutorial](http://evomics.org/unix-tutorial-2015/) by Julian Catchen -- From [Evomics 2015](http://evomics.org/workshops/workshop-on-genomics/2015-workshop-on-genomics-cesky-krumlov/) workshop in Czech Republic
* [Learn the Command Line](https://www.codecademy.com/courses/learn-the-command-line) -- Code Academy
* [_Learn Unix The Hard Way_](http://cli.learncodethehardway.org/book/) by Zed Shaw -- More detail than you will get from Appendix A of Shaw's _LPTHW_

### Python Resources

* [MIT OpenCourseWare](http://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-00sc-introduction-to-computer-science-and-programming-spring-2011/Syllabus/)
* [SciPy Lectures](https://scipy-lectures.github.io)
* [MatPlotLib Cheatsheet](https://github.com/juliangaal/python-cheat-sheet/blob/master/Matplotlib/Matplotlib.md)

### IPython Resources from Cyrille Rossant

* [IPython Interactive Computing and Visualization Cookbook](http://www.amazon.com/IPython-Interactive-Computing-Visualization-Cookbook/dp/1783284811)
* [Learning IPython for Interactive Computing and Data Visualization](https://www.packtpub.com/big-data-and-business-intelligence/learning-ipython-interactive-computing-and-data-visualization) -- [GitHub repo](https://github.com/rossant/ipython-minibook)

### Data Analysis Resources

* [10-minute Tour of Pandas](https://vimeo.com/59324550) by Wes McKinney -- Basic video tour
* [R vs. Python for Data Analysis](http://www.r-bloggers.com/choosing-r-or-python-for-data-analysis-an-infographic/) -- Fun cartoon to abate or fuel your biases
* [_Python Scripting for Computational Science_](http://www.springer.com/us/book/9783540739159) by H. P. Langtangen -- Deeper and more mathematical treatment
* [An Introduction To Applied Bioinformatics](http://caporasolab.us/An-Introduction-To-Applied-Bioinformatics/) by Greg Caporaso
* [A Dramatic Tour through Python's Data Visualization Landscape](https://dansaber.wordpress.com/2016/10/02/a-dramatic-tour-through-pythons-data-visualization-landscape-including-ggplot-and-altair/)

## Course Philosophy

1. You learn Python by doing, just like anything else. With a few exceptions, you're not going to break your computer by trying new commands. So just try it and see what happens. Print output of commands. Print values of variables. Kick the thing until it works.
2. Resist the urge to get frustrated and blame the computer when your code doesn't run. Computers are deterministic machines; it's almost always your fault. But that's OK! Your computer will give you error messages that describe what went wrong. Read them and try to understand them.
3. When you don't know how to do something, google it. You'll be amazed by the solutions you'll find to do _thing x_ if you google "python thing x".
4. Learn keyboard shortcuts, as many as you can. Tab-complete in the shell and IPython/Jupyter!
5. Remember Zed's sage wisdom:
	* Practice every day.
	* Don't over-do it. Slow and steady wins the race.
	* It's alright to be totally lost at first.
	* When you get stuck, get more information.
	* Try to solve it yourself first.

## Assignments and Grading

### Weekly Assignments

Weekly take-home assignments will follow the course schedule, reinforcing skills with exercises to analyze and visualize scientific data. Assignments will given out on Wednesdays and will be due the following Wednesday, using TritonEd. Assignments are worth 8 points each and will be graded on effort, completeness, and accuracy.

### Final Project

You will choose a data set of your own or provided in one of the texts and write a Python program (or set of Python programs or mixture of .ipynb and .py/.sh scripts) to carry out a revealing data analysis. Have a look at Shaw Ex43-52 and McKinney Ch10-12 for more ideas. The final project is worth 20 points and will be graded on effort, creativity, and fulfillment of the requirements below.

Requirements:

* Submit your project as either: a Jupyter notebook (or collection of notebooks), a Python script (or collection of scripts), or a combination of the two.
* Use `pandas` and at least three (3) additional libraries/packages, such as:
	- Plotting: `matplotlib`, `seaborn`
	- Statistics and modeling: `statsmodels`, `scikit-learn`
	- Bioinformatics: `scikit-bio`, `biopython`
	- Climate science: `cdms`, `iris`
	- Other domain-specific libraries/packages
* Use at least three (3) user-defined functions.
* Optional: Create user-defined modules and classes for use in your code.
* Optional: Share your code on GitHub.

### Grading

There are 100 points total possible for the course:

* Assignments: 72 points (9 assignments x 8 points each)
* Final project: 20 points
* Participation: 8 points

Participation is based on completing the pre-course survey, showing up to class (when you are able), and completing the course evaluation (this is on the honor system as I won't know who completes it). There are no midterm or final exams.

## Schedule Overview

The course consists of 20 lessons. As a class, it is taught as two lessons per week for 10 weeks, but the material can be covered at any pace.

Lessons 1-3 will be an introduction to the command line. By the end of this tutorial, everyone will be familiar with basic Unix commands.

Lessons 4-9 will be an introduction to programming using Python. The main text will be Shaw's _Learn Python 3 the Hard Way_. For those with experience in a programming language other than Python, Lutz's _Learning Python_ will provide a more thorough introduction to programming Python. We will learn to use IPython and IPython Notebooks (also called Jupyter Notebooks), a much richer Python experience than the Unix command line or Python interpreter.

Lessons 10-18 will focus on Python packages for data analysis. We will work through McKinney's _Python for Data Analysis_, which is all about analyzing data, doing statistics, and making pretty plots. You may find that Python can emulate or exceed much of the functionality of R and MATLAB.

Lessons 19-20 conclude the course with two skills useful in developing code: writing your own classes and modules, and sharing your code on GitHub.

## Lesson Schedule

Lessons are available as .md or .ipynb files by clicking on the lesson numbers below. Readings should be completed while typing out the code (this is integral to the Shaw readings) and doing any Study Drills (Shaw) and Chapter Quizzes (Lutz).

Lesson	|	Title	|	Readings	|	Topics	|	Assignment
-----	|	-----	|	-----	|	-----	|	-----
[1](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson01.md)	|	Overview	|	--	|	Introductions and overview of course	|	Pre-course survey; Acquire texts
[2](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson02.md)	|	Command Line Part I	|	Shaw: [Introduction](https://learnpythonthehardway.org/python3/intro.html),<br>[Ex0](https://learnpythonthehardway.org/python3/ex0.html), [Appendix A](https://learnpythonthehardway.org/python3/appendixa.html)	|	Command line crash course; Text editors	|	Assignment 1: Basic Shell Commands
[3](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson03.md)	|	Command Line Part II	|	Yale: [The 10 Most Important Linux Commands](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/data/the_10_most_important_linux_commands.md)	|	Advanced commands in the bash shell	|	--
[4](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson04.ipynb)	|	Conda, IPython, and Jupyter Notebooks	|	Geohackweek: [Introduction to Conda](https://geohackweek.github.io/Introductory/01-conda-tutorial/)	|	Conda tutorial including Conda environments, Python packages, and PIP, Python and IPython in the command line, Jupyter notebook tutorial and Python crash course	|	Assignment 2: Bash, Conda, IPython, and Jupyter
[5](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson05.ipynb)	|	Python Basics, Strings, Printing	|	Shaw: [Ex1-10](https://learnpythonthehardway.org/python3/ex1.html); Lutz: Ch1-7	|	Python scripts, error messages, printing strings and variables, strings and string operations, numbers and mathematical expressions, getting help with commands and Ipython	|	--
[6](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson06.ipynb)	|	Taking Input, Reading and Writing Files, Functions	|	Shaw: [Ex11-26](https://learnpythonthehardway.org/python3/ex11.html); Lutz: Ch9,14-17	|	Taking input, reading files, writing files, functions	|	Assignment 3: Python Fundamentals I
[7](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson07.ipynb)	|	Logic, Loops, Lists, Dictionaries, and Tuples	|	Shaw: [Ex27-39](https://learnpythonthehardway.org/python3/ex27.html); Lutz: Ch8-13	|	Logic and loops, lists and list comprehension, tuples, dictionaries, other types	|	--
[8](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson08.ipynb)	|	Python and IPython Review	|	McKinney: [Ch1](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/preliminaries/intro_html), [Ch2](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/python-language-basics-ipython-and-jupyter-notebooks/intro_python_environment_html), [Ch3](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/built-in-data-structures-functions-and-files/intro_python_stdlib_html)	|	Review of Python commands, IPython review	|	Assignment 4: Python Fundamentals II
[9](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson09.ipynb)	|	Regular Expressions	|	Kuchling: [Regular Expression HOWTO](https://docs.python.org/3/howto/regex.html)	|	Regular expression syntax, Command-line tools: `grep`, `sed`, `awk`, `perl -e`, Python examples: built-in and `re` module	|	--
[10](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson10.ipynb)	|	Numpy, Pandas and Matplotlib Crashcourse	|	Pratik: [Introduction to Numpy and Pandas](https://cloudxlab.com/blog/numpy-pandas-introduction/)	|	Numpy, Pandas, and Matplotlib overview	|	Assignment 5: Regular Expressions
[11](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson11.ipynb)	|	Pandas Part I	|	McKinney: [Ch4](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/numpy-basics-arrays-and-vectorized-computation/numpy_html), [Ch5](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/getting-started-with-pandas/pandas_html)	|	Introduction to NumPy and Pandas: `ndarray`, `Series`, `DataFrame`, `index`, `columns`, `dtypes`, `info`, `describe`, `read_csv`, `head`, `tail`, `loc`, `iloc`, `ix`, `to_datetime`	|	--
[12](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson12.ipynb)	|	Pandas Part II	|	McKinney: [Ch6](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/data-loading-storage-and-file-formats/io_html), [Ch7](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/data-cleaning-and-preparation/data_preparation_html), [Ch8](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/data-wrangling-join-combine-and-reshape/wrangling_html)	|	Data Analysis with Pandas: `concat`, `append`, `merge`, `join`, `set_option`, `stack`, `unstack`, `transpose`, dot-notation, `values`, `apply`, `lambda`, `sort_index`, `sort_values`, `to_csv`, `read_csv`, `isnull`	|	Assignment 6: Pandas Fundamentals
[13](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson13.ipynb)	|	Plotting with Matplotlib	|	McKinney: [Ch9](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/plotting-and-visualization/vis_html); Johansson: [Matplotlib 2D and 3D plotting in Python](http://github.com/jrjohansson/scientific-python-lectures)	|	Matplotlib tutorial from J.R. Johansson	|	--
[14](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson14.ipynb)	|	Plotting with Seaborn	|	[Seaborn Tutorial](http://seaborn.pydata.org/tutorial.html)	|	Seaborn tutorial from Michael Waskom	|	Assignment 7: Plotting
[15](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson15.ipynb)	|	Pandas Time Series	|	McKinney: [Ch11](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/time-series/timeseries_html)	|	Time series data in Pandas	|	--
[16](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson16.ipynb)	|	Pandas Group Operations	|	McKinney: [Ch10](http://proquest.safaribooksonline.com/book/programming/python/9781491957653/data-aggregation-and-group-operations/groupby_html)	|	`groupby`, `melt`, `pivot`, `inplace=True`, `reindex`	|	Assignment 8: Time Series and Group Operations
[17](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson17.ipynb)	|	Statistics Packages	|	[Handbook of Biological Statistics](http://www.biostathandbook.com)	|	Statistics capabilities of Pandas, Numpy, Scipy, and Scikit-bio	|	--
[18](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson18.ipynb)	|	Interactive Visualization with Bokeh	|	[Bokeh User Guide](http://bokeh.pydata.org/en/latest/docs/user_guide.html)	|	Quickstart guide to making interactive HTML and notebook plots with Bokeh	|	Assignment 9: Statistics and Interactive Visualization
[19](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson19.ipynb)	|	Modules and Classes	|	Shaw: [Ex40-52](https://learnpythonthehardway.org/python3/ex40.html)	|	Packaging your code so you and others can use it again	|	--
[20](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/lessons/lesson20.md)	|	Git and GitHub	|	[GitHub Guides](https://guides.github.com)	|	Sharing your code in a public GitHub repository	|	Final Project

