# Reading Assignment 12

## Pandas

---

### Pandas in 10

---

- To create a Series with pandas, use the `pandas.Series` function and provide the data in parentheses within square brackets.
- Create a data frame by passing a NumPy array with a datetime index and labeled columns.
  - Or pass in a dictionary or objects
- To view the top and bottom rows of a data frame use the `data_frame.head()` and `data_frame.tail()` methods.
- To view the index or columns; `data_frame.index` and `data_frame.columns`.
- The fundamental difference between NumPy arrays and pandas DataFrames is that arrays have one data type for the array and DataFrames have one data type per column.
- `describe()` shows a quick summary of the data
- `data_frame.T` will transpose the data
- `data_frame.sort_index()` will sort by axis
- `data_frame.sort_values()` will sort by values
- For optimized production code, use the data access methods;
  - Selection by Label
    - `.loc`
    - `.at`
  - Selection by Position
    - `.iloc`
    - `.iat`
- You can use simple selection or slice syntax, but it's reccomended to use the methods.
- You can also select with Boolean indexing to get the values that meet a conditon
- You can also set new columns which automatically aligns the data by the indexes.
- pandas typically uses `np.nan` for missing data and is by default not included in computations.
- You can reindex to change/add/delete the index on a specified axis.
- There are multiple operations you can perform on a DataFrame like;
  - `data_frame.mean()` to get the average of the data
  - `data_frame.apply()` to apply a function to the data
  - You can also histogram the data
  - If the data is strings, you can also use some string methods on them.
- To merge DataFrames you can;
  - Concat the data with `concat()`
  - Join the data in the style of SQL with `panda.merge()`
- You can also "group" data which is composed of one or more of the following steps;
  - Split the data based on criteria
  - Apply a function to each element seperately
  - Combine the results into a data structure
- You can also restructure the data such as into;
  - A stack with `stack()` which compresses a level in the columns
    - The inverse is `unstack()` which works on the last level
  - Or a pivot table with `panda.pivot_table()`
- You can also perfom resample operations easily. This can be used for;
  - Conveting to another time zone, `series.tz_convert()`
  - Converting time span representations, `series.to_period()`/`series.to_timestamp()`
- You can also include catagorical data
- You can also plot data which follows the matplotlib API convention.
- To write and read from files you use the methods for each language;
  - `.to_csv` and `.read_csv` for CSV files
  - `.to_hdf` and `.read_hdf` for HDF5
  - `.to_excel` and `.read_excel` for Excel documents

### What is Pandas

---

- pandas is a great library of tools that can be used for data analysis.
- Some other methods are;
  - `.describe` to get a breakdown of the different values in the dataset
  - `.drop()` will get rid of unwanted columns  
  - `.value_counts` will get the count based on argument values.
