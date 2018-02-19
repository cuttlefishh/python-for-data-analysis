### Assignment 6 - Pandas Fundamentals

Complete the tasks below. Please turn in a single Jupyter notebook named `6_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### The Earth Microbiome Project

For this assignment, we will use Pandas to examine metadata from the [Earth Microbiome Project](http://earthmicrobiome.org/).

First, download the metadata file for a 2,000-sample subset of the >27,000 samples in the Release 1 16S rRNA dataset.

```
curl -O "ftp://ftp.microbio.me/emp/release1/mapping_files/emp_qiime_mapping_subset_2k.tsv"
```

**1.** Reading and summarizing.

* Import the tab-separated values file `emp_qiime_mapping_subset_2k.tsv` as a DataFrame called `df` with default data types, with the first row as column labels (columns) and the first column as row labels (indexes).
* The indexes should be the sample IDs. How many samples are in this DataFrame? How many metadata columns?
* What are the minimum and maximum pH values in the dataset?
* What are the average and standard deviation temperature values in the dataset?

**2.** Indexing, slicing, and writing.

* Make a new Series called `temp` with the temperature column as its own Series object. Remove NaN values (np.nan) from this Series. How many values are left?
* Make a new DataFrame called `df_seqs` from columns sequences_split_libraries through observations_deblur_150bp (column positions 17-23) of the existing DataFrame. What is the mean value of column observations_deblur_90bp?
* Save `df_seqs` as a csv file.

**3.** Merging, joining, and concatenating.

* Store the first 5 rows of `df_seqs` as a new dataframe called `df_seqs_head`. Store the last 5 rows of `df_seqs` as a new dataframe called `df_seqs_tail`.
* Concatenate `df_seqs_head` and `df_seqs_tail` using the concat() function.
* Append `df_seqs_tail` to `df_seqs_head` using the append() function.
* Make a new DataFrame called `df_phys` with the pH, temperature, and salinity columns (hint: you will need to know the exact column names; these are some of the last few columns). Make another new DataFrame called `df_empo` with the column empo_3 (note: this will actually be a Series because it has only one column, but you can treat it like a DataFrame).
* Merge `df_phys` with `df_seqs` using the merge() function with the indexes of both DataFrames to make a new DataFrame called `df_merged`.
* Join `df_merged` with `df_empo` using the join() function and store the result as `df_merged`.

**4.** Applying functions.

* Use a list comprehension to add a new column to `df_merged` called `temperature_deg_f` which takes the values in `temperature_deg_c` and converts them to degrees Fahrenheit. 
* Create a function that changes a single numerical value from Celsius to Fahrenheit. Apply this function to the values in `temperature_deg_c` using apply() to create a new column called `temperature_deg_f_2`.

**5.** Sorting.

* Sort the rows in `df_merged` by sequences_split_libraries values from high to low and store the result as `df_merged`.
* Sort the columns in `df_merged` by column name from A to Z and store the result as `df_merged`.
