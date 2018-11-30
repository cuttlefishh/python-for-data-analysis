### Assignment 9 - Statistics and Interactive Visualization

Complete the tasks below. Please turn in a single Jupyter notebook named `9_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### A. Student survey data wrangling

1. Download the student survey data from [2015](https://raw.githubusercontent.com/cuttlefishh/python-for-data-analysis/master/data/survey_scores_2015_T.csv) and [2018](https://raw.githubusercontent.com/cuttlefishh/python-for-data-analysis/master/data/survey_scores_2018.csv) if you don't have them already.
2. Import the csv files as DataFrames and inspect the files. Notice that the data are formatted differently. Next you will modify them so they are compatible.
3. The 2015 data is mostly ready to go. Just convert the Y/N values to True/False (boolean).
4. The 2018 data needs a lot of work. Delete the 'Timestamp' and 'Graduate program and advisor' columns. Rename the remaining columns to match those in 2015. Convert the Yes/No values to True/False (boolean). Convert the None/Some/Moderate/Experienced values to 0/1/2/3 (integers). 

#### B. Statistical analysis

1. In both years, some students have Macs and some have Windows computers. Test the hypothesis that the proportions of Mac and Windows users are the same in 2015 and 2018. Note that in 2018, the question was asked differently and some people listed multiple operating systems; for the purposes of this question, assume that SDNT6 and SDNT10 have Windows computers and SDNT7 has a Mac.
2. For each of the 'score' columns shared by both datasets (there are five), use a two-sample *t*-test to determine if the two samples have equal means. Note: To use `scipy.stats`, you may have to import it directly like so: `from scipy import stats`.

#### C. Stock data

1. Download historical stock data from the past three years for a stock of your choice (eligible symbols: [here](https://iextrading.com/trading/eligible-symbols/)) and the S&P 500 index (symbol: 'SPY'). Use Panads timeseries operations to calculate the start and end dates. IEX is currently a reliable source of data that does not require registration (see [pandas-datareader docs](https://pydata.github.io/pandas-datareader/stable/remote_data.html)). Note that using IEX will return a hierarchical column index, where the first column index is the price type ('open', 'high', 'low', 'close', 'volume') and the second column index is the symbol. You may also want to convert the index from string/object type to datetime type. For example, to download stock data for Qualcomm and Illumina and see the close data for Qualcomm, use these commands, where `start` and `end` are Pandas datatime objects: 

        import pandas_datareader as pdr
        quotes = pdr.data.DataReader(['QCOM', 'ILMN'], 'iex', start, end)
        quotes.set_index(pd.to_datetime(quotes.index), inplace=True)
        quotes['close']['QCOM']

2. Calculate the 52-week high and low for the past year for your stock and for the S&P 500.
3. Plot the price at close over the past three years of your stock and the S&P 500. Use a dual y-axis (using `twinx` like we learned in the Matplotlib lesson) to display the two prices side by side on separate scales.
4. Calculate the percent change from three years ago for both prices. How did your stock perform relative to the S&P 500?

#### D. Bokeh visualization

1. Use Bokeh to create an interactive visualization of the stock data you downloaded in Question 3. The HTML file that is generated should use the default content delivery network; i.e., it requires an internet connection to render properly.
2. Use Bokeh to create an interactive visualization from a dataset of your choice. You can choose one of the datasets from a previous assignment (e.g., precipitation in La Jolla, moons of the Solar System, or the Earth Microbiome Project) or your own dataset. The HTML file that is generated should be a stand-alone file (`mode=inline`) that does not require an internet connection to render properly.

#### E. Final project proposal

The final project description is [here](https://github.com/cuttlefishh/python-for-data-analysis/blob/master/assignments/final_project.md). Write a short paragraph describing your proposed idea for the final project. If you are doing an analysis, describe the dataset you plan to use, what analysis you want to do, and how the Python packages you plan to use will help you do this analysis. If you are creating a software tool, describe the purpose of your tool and how you will use Python packages to accomplish it. I will provide feedback when I grade your assignment. If you would like feedback sooner, please email me directly.
