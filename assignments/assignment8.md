### Assignment 8 - Time Series and Group Operations

Complete the tasks below. Please turn in a single Jupyter notebook named `8_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### Precipitation in La Jolla

For this assignment, we will use a file containing daily precipitation data in La Jolla from February 2009 to February 2018, which were downloaded from [NOAA](https://www.ncdc.noaa.gov/cdo-web/datasets/GHCND/stations/GHCND:US1CASD0030/detail) using "standard" (imperial) units (inches for precipitation, feet for elevation). Download the file from [GitHub](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/data/la_jolla_precip_daily.csv).

**1.** Set up the file.

* Import the csv file as a Pandas DataFrame with default header and index.
* Change the 'DATE' column to a timestamps using `pd.datetime()`.
* What was the maximum daily precipitation (in inches) during this time period and when was it?

**2.** Explore the dataset.

* We don't need the columns 'SNOW' and 'SNOW_ATTRIBUTES' because there was no recorded snow in the dataset. Delete those columns "in place".
* Find out about the sampling stations. Notice that the column values are similar between rows except 'DATE' and 'PRCP'. Explore these other columns using three different commands (we haven't covered them yet, but they are easy to use and you can always google them): 
    * Use the `value_counts()` method for each of these columns: 'STATION', 'NAME', 'LATITUDE', 'LONGITUDE', and 'ELEVATION'. There should only be one cateogory for each calculation because all the data come from the same station. To see what output looks like for a more diverse series, use the `value_counts()` method on 'PRCP' and 'PRCP_ATTRIBUTES'.
    * Make a DataFrame with just the columns 'STATION', 'NAME', 'LATITUDE', 'LONGITUDE', and 'ELEVATION' and use the method `drop_duplicates()` to see all the unique combinations of values in those five columns. 
    * Create a groupby object using `groupby('STATION')`, then use the `count()` method on that groupby object to count the number of values for each station.

**3.** Plot precipitation versus time.

* Use the Matplotlib function `plot()` to plot 'PRCP' versus 'DATE' as a line.
* Plot 'PRCP' versus 'DATE' each year separately as a different colored line, with a legend indicating the year. Hint: You will have to extract the year from the date somehow, for example with the `.year` attribute or a regular expression, optionally creating a new column for the year.
* Go back and recolor the two plots above: pick two colors from ColorBrewer or xkcd and draw your subplots again.
* Replot the plots in a subplot with the two sets of axes in a 1x2 formation.

**4.** Plot distributions of the precipitation data.

* Plot a histogram of precipitation values using the Matplotlib function `hist()` or `violinplot()`.
* Plot a histogram with kernel density and rugplot with the Seaborn function `distplot()`. Play around with the settings to make a histogram that represents the data well.
* Add columns to the DataFrame for month and year. Hint: You can do this with list comprehension and the datetime attributes `month` and `year`.
* Use groupby to group the data by `year` or by `month`. Which year was the rainiest? Which month was the rainiest?
* Make boxplots by year and by month using the Seaborn function `boxplot()`. 

**5.** Pivoting, stacking and unstacking.

* Use pivot_table to produce a new DataFrame, where rows=years and columns=months, containing the mean precipitation of each month.
* Draw a heatmap of years x months where each square is a month colored by mean precipitation. Adjust the colormap to highlight months with heavy precipitation. Hint: Seaborn's `heatmap()` function makes this very easy.
* Stack the monthly precipitation table using `stack()`. View the values for 2017. Which month had the most precipitation in 2017? Describe the distribution statistics for all months using `describe()`. How many months are included in this dataset? What was the median month (daily average) value in this time period?
* Use `unstack()` to stack precipitation pivot table by month and then year. View the values for December. Which year had the wettest December?
