# pandas
How we can perform Data Aggregation on Pandas DataFrame? Give an example.


Python is a great language for doing data analysis, primarily because of the fantastic ecosystem of data-centric Python packages. Pandas is one of those packages and makes importing and analyzing data much easier.

Dataframe.aggregate() function is used to apply some aggregation across one or more column. Aggregate using callable, string, dict, or list of string/callables. Most frequently used aggregations are:

sum: Return the sum of the values for the requested axis
min: Return the minimum of the values for the requested axis
max: Return the maximum of the values for the requested axis

Syntax: DataFrame.aggregate(func, axis=0, *args, **kwargs)

Parameters:
func : callable, string, dictionary, or list of string/callables. Function to use for aggregating the data. If a function, must either work when passed a DataFrame or when passed to DataFrame.apply. For a DataFrame, can pass a dict, if the keys are DataFrame column names.
axis : (default 0) {0 or ‘index’, 1 or ‘columns’} 0 or ‘index’: apply function to each column. 1 or ‘columns’: apply function to each row.

Returns: Aggregated DataFrame

Example #1: Aggregate ‘sum’ and ‘min’ function across all the columns in data frame.

filter_none
brightness_4
# importing pandas package 
import pandas as pd 
  
# making data frame from csv file 
df = pd.read_csv("nba.csv") 
  
# printing the first 10 rows of the dataframe 
df[:10] 
# Applying aggregation across all the columns  
# sum and min will be found for each  
# numeric type column in df dataframe 
df.aggregate(['sum', 'min']) 

