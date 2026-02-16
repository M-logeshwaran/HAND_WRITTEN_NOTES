📄 01_pandas_basics_and_data_structures.md

# Pandas Basics and Data Structures

Pandas is a powerful library for data analysis and manipulation.

It mainly provides two data structures:
1. Series (1D)
2. DataFrame (2D)

---

# 1. Import Pandas

```python
import pandas as pd


---

2. Pandas Series

Series is a one-dimensional labeled array.

2.1 Creating Series from List

s = pd.Series([10, 20, 30, 40])
print(s)

Output:

0    10
1    20
2    30
3    40
dtype: int64


---

2.2 Custom Index

s1 = pd.Series([100, 200, 300], index=['a', 'b', 'c'])
print(s1)

Output:

a    100
b    200
c    300
dtype: int64


---

2.3 Accessing Values

print(s1['a'])

Output:

100


---

3. Pandas DataFrame

DataFrame is a two-dimensional labeled data structure.


---

3.1 Creating DataFrame from Dictionary

data = {
    "Name": ["John", "Anna", "Peter"],
    "Age": [23, 25, 21],
    "City": ["Chennai", "Delhi", "Mumbai"]
}

df = pd.DataFrame(data)
print(df)

Output:

Name  Age     City
0   John   23  Chennai
1   Anna   25    Delhi
2  Peter   21   Mumbai


---

4. Viewing Data

4.1 Head

print(df.head())

Displays first 5 rows.


---

4.2 Tail

print(df.tail())

Displays last 5 rows.


---

5. DataFrame Information

5.1 Shape

print(df.shape)

Output:

(3, 3)


---

5.2 Columns

print(df.columns)

Output:

Index(['Name', 'Age', 'City'], dtype='object')


---

5.3 Data Types

print(df.dtypes)

Output:

Name    object
Age      int64
City    object
dtype: object


---

5.4 Info

print(df.info())

Output:

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3 entries, 0 to 2
Data columns (total 3 columns):
...


---

6. Selecting Data

6.1 Selecting Column

print(df["Name"])

Output:

0     John
1     Anna
2    Peter
Name: Name, dtype: object


---

6.2 Selecting Multiple Columns

print(df[["Name", "Age"]])

Output:

Name  Age
0   John   23
1   Anna   25
2  Peter   21


---

7. Accessing Rows

7.1 Using loc (label based)

print(df.loc[0])

Output:

Name      John
Age          23
City    Chennai
Name: 0, dtype: object


---

7.2 Using iloc (index based)

print(df.iloc[1])

Output:

Name     Anna
Age         25
City    Delhi
Name: 1, dtype: object


---

Summary

Series is 1D data structure.

DataFrame is 2D tabular data.

Use head(), tail() to view data.

shape, columns, dtypes give structure info.

loc and iloc are used for row access.


---
