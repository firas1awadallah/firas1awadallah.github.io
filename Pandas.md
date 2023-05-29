## What kind of data does pandas handle?
* In [2]: import pandas as pd

* Import the package, aka import pandas as pd

* A table of data is stored as a pandas DataFrame

* Each column in a DataFrame is a Series

* You can do things by applying a method to a DataFrame or Series

## How do I read and write tabular data?
* Getting data in to pandas from many different file formats or data sources is supported by read_* functions.

* Exporting data out of pandas is provided by different to_*methods.

* The head/tail/info methods and the dtypes attribute are convenient for a first check.

## How do I select a subset of a DataFrame?
* When selecting subsets of data, square brackets [] are used.

* Inside these brackets, you can use a single column/row label, a list of column/row labels, a slice of labels, a conditional expression or a colon.

* Select specific rows and/or columns using loc when using the row and column names.

* Select specific rows and/or columns using iloc when using the positions in the table.

* You can assign new values to a selection based on loc/iloc.

## How do I create plots in pandas?

* The .plot.* methods are applicable on both Series and DataFrames.

* By default, each of the columns is plotted as a different element (line, boxplot,…).

* Any plot created by pandas is a Matplotlib object.

## How to create new columns derived from existing columns

* Create a new column by assigning the output to the DataFrame with a new column name in between the [].

* Operations are element-wise, no need to loop over rows.

* Use rename with a dictionary or function to rename row labels or column names.

## How to calculate summary statistics

* Aggregation statistics can be calculated on entire columns or rows.

* groupby provides the power of the split-apply-combine pattern.

* value_counts is a convenient shortcut to count the number of entries in each category of a variable.

## How to reshape the layout of tables
* Sorting by one or more columns is supported by sort_values.

* The pivot function is purely restructuring of the data, pivot_table supports aggregations.

* The reverse of pivot (long to wide format) is melt (wide to long format).

## How to combine data from multiple tables
* Multiple tables can be concatenated both column-wise and row-wise using the concat function.

* For database-like merging/joining of tables, use the merge function.

## How to handle time series data with ease
* Valid date strings can be converted to datetime objects using to_datetime function or as part of read functions.

* Datetime objects in pandas support calculations, logical operations and convenient date-related properties using the dt accessor.

* A DatetimeIndex contains these date-related properties and supports convenient slicing.

* Resample is a powerful method to change the frequency of a time series.
## How to manipulate textual data
* String methods are available using the str accessor.

* String methods work element-wise and can be used for conditional indexing.

* The replace method is a convenient method to convert values according to a given dictionary.

## Reading Questions
1. Explain the purpose and basic functionality of the Pandas library. What are some common operations that can be performed on data using Pandas, and how do they contribute to data analysis and manipulation?
The Pandas library is a popular open-source data manipulation and analysis tool for Python. It provides high-performance, easy-to-use data structures and data analysis tools for handling structured data. Pandas is built on top of NumPy, another Python library for numerical computing.

* The purpose of Pandas is to simplify data manipulation and analysis tasks by providing intuitive data structures, such as Series (1-dimensional labeled arrays) and DataFrame (2-dimensional labeled data tables). These data structures enable efficient data handling and allow for various operations on data.

Some common operations that can be performed on data using Pandas include:

1. Data Loading: Pandas allows you to load data from various file formats such as CSV, Excel, SQL databases, and more. 
2. Data Exploration: Pandas provides functions to inspect and explore data.

3. Data Selection and Filtering: Pandas enables you to select specific rows or columns from a DataFrame based on conditions. 

4. Data Manipulation: Pandas offers powerful tools for manipulating data.

5. Data Aggregation and Grouping: Pandas allows you to perform aggregations on data, such as calculating the sum, mean, count, or other statistics for specific groups of data. 

6. Data Visualization: While Pandas itself does not provide visualization capabilities, it seamlessly integrates with other libraries like Matplotlib and Seaborn to create plots, charts, and graphs from the data stored in DataFrames. 

* These operations and functionalities provided by Pandas contribute to data analysis and manipulation by simplifying the process of loading, cleaning, transforming, exploring, and summarizing data. Pandas helps researchers, data scientists, and analysts work with data efficiently, allowing them to extract insights and make informed decisions based on the data at hand.

2. What are the primary data structures in Pandas, and how do they differ in terms of use cases?

The primary data structures in Pandas are the :
1. Series:
A Series is a one-dimensional labeled array that can hold any data type. It is similar to a column in a spreadsheet or a database table.
2. DataFrame:
A DataFrame is a two-dimensional labeled data structure, resembling a table or a spreadsheet with rows and columns.
It is a highly versatile data structure and the most commonly used in Pandas. 


* Both Series and DataFrames provide similar functionality for data manipulation, but DataFrames are generally more flexible and powerful for handling complex datasets. DataFrames can be thought of as a collection of Series, where each column is a Series and the columns share a common index. This structure allows for efficient operations on the data, such as column-wise operations, grouping, and aggregation, which are essential for data analysis and manipulation tasks.
3. Describe the process of loading a dataset into a Pandas DataFrame. What are some common file formats that can be used, and which Pandas functions are utilized to read these formats?

To load a dataset into a Pandas DataFrame, you typically follow these steps:

1. Install Pandas: If you haven't already, you need to install the Pandas library.
2. Import the Pandas library: Once Pandas is installed, you need to import it into your Python script or Jupyter Notebook using the following import statement:

3. Choose a file format: Determine the file format in which your dataset is stored. 

4. the appropriate Pandas function: Select the Pandas function that corresponds to the file format you're working with. :

5. CSV: Comma-separated values (CSV) files are one of the most common file formats for storing structured data. Pandas provides the read_csv() function to read CSV files. You can use it like this:

6. Explore and manipulate the data: Once the dataset is loaded into a DataFrame, you can start exploring and manipulating the data using the rich functionality provided by Pandas. 

## Things I want to know more about
* i want to know more about Banda and Numpy
