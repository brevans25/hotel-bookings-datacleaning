# hotel-bookings-datacleaning
A mini-project that walks through essential techniques for cleaning and preparing real-world data.

## Concepts worked in this notebook:

1. **Visualizing the data:**

`pd.read_csv()` to read dataset into a pandas dataframe;<br>
<code>for eachColumn in df.columns:<br>
&nbsp;&nbsp;&nbsp;&nbsp;print(eachColumn)</code> to display columns;

<br>

2. **Dropping and Renaming Columns:**

 Function    | Parameter 1| Parameter 2 | Parameter 3 |
 ----------- | -----------| ------------| ----------- |
 **.drop()** | columns=[*'columnToBeDropped'*]| inplace=*True* | *_*
**.rename()**   | {'Old_Name': 'New_Name'}| axis=*1* | inplace=*True*

<br>

3. **Handling Missing Values (NaNs):**

`.dropna()` drops rows or columns containing `nulls`, depending on parameters;<br>
`.fillna()` replaces nulls with a given value;<br>
`.isnull()` returns a boolean value where values are null;<br>
`.isna()` ? 

<br>

4. **Investigate Data Types**

`.dtypes` to investigate data types in each column;<br>
`.astype()` takes a dictionary where each **key** is the column containing the wrong data type and each **value** is the new data type for that column.

<br>

5. **Bin Columns**

`.pd.cut()` function to bin values into groups.<br>
It requires: <br>
    - `bins` => the numeric boundaries;<br>
    - `labels` => names for each bin.<br>

This function will lookup the value in a column and assign a value based on which bin it falls under

<br>

6. **Separate Columns**

`.split()` Splits a column by a delimiter. Returns a Series of lists.<br>
If `expand=True` is passed as an argumnent, it outputs new columns. <br>
`.pop()` to "pop" a column out of its place:<br>
`.insert()` Inserts a column at a specific `index`.

<br>

7. **String Cleaning**

Use `regex` to remove undesired characters in specific strings

<br>

8. **Remove Duplicates**

`.duplicated()` marks the values that are duplicates across **all** columns as `True`/`False`;<br>
If `keep=False` is passed as a parameter, all duplicate rows will be marked as `True`.
`.drop_duplicates` does what it says. It can take a `subset` parameter that will only drop duplicates across the specified columns in the subset.<br>
Also, it takes a `keep` parameter that will take `first` as value to keep the first instance of the row and drop the additional duplicates, `last` to keep the last or `False`.





