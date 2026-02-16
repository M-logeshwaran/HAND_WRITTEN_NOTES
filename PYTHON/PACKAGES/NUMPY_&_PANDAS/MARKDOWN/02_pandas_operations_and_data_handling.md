📄 02_pandas_operations_and_data_handling.md

# Pandas Operations and Data Handling

This section covers filtering, adding columns, updating data, sorting, handling missing values, and basic statistics.

---

# 1. Filtering Data

```python
import pandas as pd

data = {
    "Name": ["John", "Anna", "Peter", "Mike"],
    "Age": [23, 25, 21, 29],
    "City": ["Chennai", "Delhi", "Mumbai", "Delhi"]
}

df = pd.DataFrame(data)


---

1.1 Filter Rows Based on Condition

print(df[df["Age"] > 23])

Output:

Name  Age    City
1  Anna   25   Delhi
3  Mike   29   Delhi


---

1.2 Multiple Conditions

print(df[(df["Age"] > 22) & (df["City"] == "Delhi")])

Output:

Name  Age   City
1  Anna   25  Delhi
3  Mike   29  Delhi


---

2. Adding New Column

df["Salary"] = [30000, 40000, 25000, 50000]
print(df)

Output:

Name  Age     City  Salary
0   John   23  Chennai   30000
1   Anna   25    Delhi   40000
2  Peter   21   Mumbai   25000
3   Mike   29    Delhi   50000


---

3. Updating Data

3.1 Update Single Value

df.loc[0, "Age"] = 24
print(df)


---

3.2 Update Using Condition

df.loc[df["City"] == "Delhi", "City"] = "New Delhi"
print(df)


---

4. Dropping Data

4.1 Drop Column

df.drop("Salary", axis=1, inplace=True)
print(df)


---

4.2 Drop Row

df.drop(2, inplace=True)
print(df)


---

5. Sorting Data

5.1 Sort by One Column

print(df.sort_values(by="Age"))


---

5.2 Sort Descending

print(df.sort_values(by="Age", ascending=False))


---

6. Handling Missing Values

df2 = pd.DataFrame({
    "Name": ["A", "B", "C"],
    "Age": [20, None, 25]
})


---

6.1 Check Missing Values

print(df2.isnull())


---

6.2 Drop Missing Values

print(df2.dropna())


---

6.3 Fill Missing Values

print(df2.fillna(0))


---

7. Basic Statistics

print(df.describe())

Output:

Age
count    ...
mean     ...
std      ...
min      ...
25%      ...
50%      ...
75%      ...
max      ...


---

8. Unique Values

print(df["City"].unique())


---

9. Value Counts

print(df["City"].value_counts())


---

Summary

Filtering using conditions.

Add and update columns using loc.

drop() removes rows or columns.

sort_values() sorts data.

isnull(), dropna(), fillna() handle missing data.

describe() gives statistical summary.

unique() and value_counts() analyze categorical data.


---
