📄 05_aggregate_groupby_and_advanced.md

# Aggregate Functions, GROUP BY and Advanced Queries

This document covers aggregate functions, GROUP BY, HAVING, and subqueries.

---

# 1. Aggregate Functions

Aggregate functions perform calculations on multiple rows and return a single value.

---

## 1.1 COUNT()

Returns number of rows.

```sql
SELECT COUNT(*) FROM student;

Count specific column:

SELECT COUNT(age) FROM student;


---

1.2 SUM()

Returns total sum.

SELECT SUM(salary) FROM employee;


---

1.3 AVG()

Returns average value.

SELECT AVG(age) FROM student;


---

1.4 MAX()

Returns maximum value.

SELECT MAX(salary) FROM employee;


---

1.5 MIN()

Returns minimum value.

SELECT MIN(age) FROM student;


---

2. GROUP BY

GROUP BY is used to group rows having same values.

Example:

SELECT dept_id, COUNT(*)
FROM student
GROUP BY dept_id;

This counts number of students in each department.


---

3. HAVING Clause

HAVING is used to filter grouped results.

Difference:

WHERE filters rows before grouping.

HAVING filters after grouping.


Example:

SELECT dept_id, COUNT(*)
FROM student
GROUP BY dept_id
HAVING COUNT(*) > 2;


---

4. Subquery

A query inside another query.

Example:

SELECT name
FROM student
WHERE age > (SELECT AVG(age) FROM student);

Subquery executes first.


---

5. IN Operator

Used to match multiple values.

SELECT * FROM student
WHERE dept_id IN (1, 2, 3);


---

6. BETWEEN Operator

Used to select range.

SELECT * FROM student
WHERE age BETWEEN 18 AND 25;


---

7. DISTINCT

Removes duplicate values.

SELECT DISTINCT dept_id FROM student;


---

Summary

Aggregate functions perform calculations.

GROUP BY groups similar values.

HAVING filters grouped results.

Subquery is query inside query.

IN checks multiple values.

BETWEEN selects range.

DISTINCT removes duplicates.


---
