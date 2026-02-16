📄 03_pandas_groupby_merge_and_file_handling.md

# Pandas GroupBy, Merge and File Handling

This section covers:
- GroupBy operations
- Merging DataFrames
- Concatenation
- Reading and Writing files (CSV)

---

# 1. GroupBy Operation

GroupBy is used to group data based on a column and perform aggregation.

```python
import pandas as pd

data = {
    "Name": ["John", "Anna", "Peter", "Mike"],
    "City": ["Delhi", "Delhi", "Mumbai", "Mumbai"],
    "Salary": [30000, 40000, 25000, 50000]
}

df = pd.DataFrame(data)


---

1.1 Group By Single Column

grouped = df.groupby("City")
print(grouped["Salary"].sum())

Output:

City
Delhi     70000
Mumbai    75000
Name: Salary, dtype: int64


---

1.2 Multiple Aggregations

print(df.groupby("City")["Salary"].agg(["sum", "mean", "max"]))

Output:

sum     mean    max
City
Delhi   70000  35000.0  40000
Mumbai  75000  37500.0  50000


---

2. Merge DataFrames

Used to combine two DataFrames based on common column.

df1 = pd.DataFrame({
    "ID": [1, 2, 3],
    "Name": ["John", "Anna", "Peter"]
})

df2 = pd.DataFrame({
    "ID": [1, 2, 4],
    "Salary": [30000, 40000, 50000]
})


---

2.1 Inner Merge

print(pd.merge(df1, df2, on="ID", how="inner"))

Output:

ID   Name  Salary
0   1   John   30000
1   2   Anna   40000


---

2.2 Left Merge

print(pd.merge(df1, df2, on="ID", how="left"))

Output:

ID   Name   Salary
0   1   John  30000.0
1   2   Anna  40000.0
2   3  Peter      NaN


---

3. Concatenation

Used to combine DataFrames vertically or horizontally.

df3 = pd.DataFrame({"A": [1, 2]})
df4 = pd.DataFrame({"A": [3, 4]})

3.1 Vertical Concatenation

print(pd.concat([df3, df4]))

Output:

A
0  1
1  2
0  3
1  4


---

4. Reading CSV File

df = pd.read_csv("data.csv")
print(df.head())


---

5. Writing CSV File

df.to_csv("output.csv", index=False)


---

6. Handling Excel File

6.1 Read Excel

df = pd.read_excel("data.xlsx")


---

6.2 Write Excel

df.to_excel("output.xlsx", index=False)


---

Summary

groupby() is used for grouping and aggregation.

merge() combines DataFrames using keys.

concat() joins DataFrames.

read_csv() and to_csv() handle CSV files.

read_excel() and to_excel() handle Excel files

---
