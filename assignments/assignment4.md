### Assignment 4 - Python Fundamentals II

Complete the tasks below. Please turn in a single Jupyter notebook named `4_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### A. Lists and loops

1. Create a list of 10 random integers in the range of -100 to 100. 
2. Loop through that list using a for loop. Put the non-negative (positive or zero) integers into a new list. If negative integers are encountered, print a message saying that the value is negative and printing that value.

#### B. Functions, lists, and loops

1. Write a function that does what you did in part A but with the following differences: 
    - The input list can be any list of numbers.
    - The function should take as a parameter a threshold for being included in the new list (e.g., if you want non-negative integers, the threshold would be 0, and the function would check if values are >= to this value).
    - The printed message for failing to be included should also report the threshold parameter.
    - The new list should be returned by the function.
2. Execute the function on your list of 10 random integers.

#### C. Dictionaries and list enumeration

1. Create a two-dimensional list with 3 'rows' and 4 'columns' and a mixture of strings and integers. 
2. Loop through each element of the list and check if each element is a string or an integer. Save the strings as a dictionary with the index (row, column) as the key and the string as the value. Save the integers as a dictionary with the index (row, column) as the key and the integer as the value.
3. Print out your dictionaries (no `print` command required).

#### D. List comprehension and saving files

1. Create a list of 5 strings that are first and last names, e.g. `'Jon Doe'`. 
2. Use a list comprehension (a single-line command) to get the first initial from each name and store each string (e.g. `'J'`) in a new list. Print this list (no `print` command required).
3. Repeat but store both the first and last initial (e.g. `'JD'`) in a new list. Print this list (no `print` command required).
4. Save this second list to a text file.

#### E. Reading files, sets, and saving files

1. Download this text file of past [World Series winners](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/data/world_series_winners.txt). 
2. Read in the lines of the file to a list, so that each line is an element of the list. 
3. Create a new list with just those list elements that contain 'New York'; print that list, making sure there's not an extra newline character between each line. Print this list (no `print` command required).
4. Use the `set` class to convert the list of all World Series winners to a list of unique values. Print this list (no `print` command required).
5. Write the output to a new file.
