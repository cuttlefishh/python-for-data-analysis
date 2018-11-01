### Assignment 5 - Regular Expressions

Complete the tasks below. Please turn in a single Jupyter notebook named `5_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### A. Regular expressions in the command line

Setup: Download [scripps_pier_20151110.csv](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/data/scripps_pier_20151110.csv) to your directory `~/sio209/data`, if you haven't already. You will use regular expressions to get information from the file.

1. Get all the rows with data from 11/10/15 using grep. How would you keep the header line also? (Hint: to get an "or", use `\|` in grep or `|` in egrep.) 
* Get all the rows where the third column (pressure) begins with a "3" using grep. (Hint: if you want to match a period `.` and not any character, you can escape it with `\.`.)
* Change the year "15" to "2015" using sed. (Reminder: sed syntax is `'sed s/find/replace/'`. Hint: if you want to match a forward slash in sed, you can escape it with a backslash like `\/`.)
* Copy your shell code (e.g., grep, sed) to a Markdown cell in your notebook.

#### B. Regular expressions in Python

Setup: Import the `re` module.

1. Create a string variable with the value 'The quick brown fox jumps over the lazy dog'.
2. Use `re.match` or `re.search` to see if the string starts with 'The'.
3. Use `re.search` to find the first instance of a lowercase letter followed by an 'o'.
4. Use `re.findall` to find all instances of a lowercase letter followed by an 'o'.
5. Use `re.sub` to change the last word to an animal of your choice.

#### C. Numpy basics

1. Create an array of ten random floats ranging from 0 to 10. Create a second array of ten integers from 0 to 9. 
3. Use 'fancy indexing' with masks to find the values in your first array that are greater than their corresponding values in the second array (e.g., if the first element in array 1 is greater than the first element in array 2).

#### D. Pandas basics

1. Read in the csv file scripps_pier_20151110.csv as a Pandas DataFrame with the index as the Date column and the column headers from the first row of that file.
2. Print all the date/times from 11/10/15. Hint: you can get the indexes from the DataFrame, convert it to a list, then iterate over that list (using a for loop or list comprehension), and then use `re.match` or `re.search`.
3. Print all the rows from 11/10/15. Hint: you can use your answer to the exercise you just did but use `.loc` indexing.
