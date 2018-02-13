### Assignment 3 - Python Fundamentals I

Complete the tasks below. You should turn in a single Jupyter notebook named `3_first_last.ipynb` (substitute your first and last name); also turn in the input .csv file used in question B3. For questions where Python scripts are used instead of the Jupyter notebook (questions A1, B1, B2), instructions are provided about pasting output/scripts into Markdown cells in your notebook.

#### A. Python basics, strings, printing (Shaw Exercises 1–10)

1. Take the file of Python code you generated in Exercise 1, called `ex1.py`, and run it on the command line. Copy the command and output from your terminal and paste it in a Markdown cell in your Jupyter notebook. (Ex1)
2. Print a sentence that contains a phrase in double quotes; print a sentence that contains an apostrophe. (Ex1)
3. Deliberately enter five incorrect commands (in separate cells) and interpret the error messages (in Markdown cells). (Ex1)
4. Add comments to your code in \#2 and \#3 explaining what is happening. (Ex2)
5. Write and evaluate five mathematical expressions. (Ex3)
6. Assign values to three numeric and three string variables. (Ex4)
7. Print values of the six variables you assigned in \#6. (Ex4–5)
8. Print two strings in raw format (%r formatter) and two strings in general/string format (%s formatter) with formatting characters. (Ch6)
9. Concatenate two strings into a third string, then find the length of all three strings.
10. Print the three strings from \#9 with a tab between the first and second and a newline between the second and third.
11. Print the three strings from \#9 with a stored formatter. (Ch7–8)
12. Print a piece of text with five lines using both newline characters and a text block. (Ex9)
13. Print a string containing a backslash, single-quote, double-qoute, newline, and tab. (Ex10)

#### B. Taking input, reading and writing files, functions (Shaw Exercises 11-26) 

**1.** Write some code, without using functions, that calculates the average of 5 numbers. Do it three different ways:

* Write a .py file that takes input from the command line using `raw_input()` (Python 2) or `input()` (Python 3). After the script works, paste the text of the file into your Jupyter notebook.
* Write a .py file that takes input from the command line using `argv`. After the script works, paste the text of the file into your Jupyter notebook.
* Enter code into two Jupyter notebooks cells: the first stores value as variables, and the second computes the average.

**2.** Using functions, write some code that takes two strings, prints them with the first letter capitalized, prints them with all letters capitalized, prints the first and last letter of each, prints the length of each, and then prints the concatenation of the two strings. Do it two different ways:

* Write a .py file that uses `argv`. After the script works, paste the text of the file into your Jupyter notebook.
* In your Jupyter notebook, comment out the `argv` portions and hard code in the values of your strings. Then make sure the code runs the same.

**3.** Using a text editor, create a comma-separated values file with 5 columns and 5 rows. Save it in the same directory as your Jupyter notebook. In the Jupyter notebook, read and print the file in different ways, and write new files, as follows:

* Read your .csv file using `read()`, `readline()`, or `readlines()`, and print the output to the screen (`print()` command is optional in notebooks!).
* Do the same but use a `with` block and a different one of `read()`, `readline()`, or `readlines()`.
* Using either of the two above methods, then change one row of data, and write your csv data to a new file.
* Read your .csv file using Pandas and display the resulting DataFrame.
* Save your DataFrame to a new file using Pandas.
