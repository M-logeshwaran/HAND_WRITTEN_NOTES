📄 04_queries_and_joins.md

# Queries and Joins in MySQL

This document covers SELECT queries, filtering, sorting, and different types of joins.

---

# 1. SELECT Statement

Used to retrieve data from a table.

Basic syntax:

```sql
SELECT column_name FROM table_name;

Select all columns:

SELECT * FROM student;

Select specific columns:

SELECT name, age FROM student;


---

2. WHERE Clause

Used to filter records.

SELECT * FROM student
WHERE age > 20;

Using AND / OR:

SELECT * FROM student
WHERE age > 18 AND name = 'Ram';


---

3. Comparison Operators

Operator	Meaning

=	Equal
!=	Not equal
>	Greater than
<	Less than
>=	Greater than or equal
<=	Less than or equal



---

4. LIKE Operator

Used for pattern matching.

SELECT * FROM student
WHERE name LIKE 'R%';

% → Any number of characters

_ → Single character



---

5. ORDER BY

Used to sort records.

Ascending (default):

SELECT * FROM student
ORDER BY age;

Descending:

SELECT * FROM student
ORDER BY age DESC;


---

6. LIMIT

Used to limit number of rows.

SELECT * FROM student
LIMIT 5;


---

7. Joins

Joins are used to combine rows from multiple tables based on a related column.


---

7.1 INNER JOIN

Returns matching records from both tables.

SELECT student.name, department.dept_name
FROM student
INNER JOIN department
ON student.dept_id = department.id;


---

7.2 LEFT JOIN

Returns all records from left table and matching records from right table.

SELECT student.name, department.dept_name
FROM student
LEFT JOIN department
ON student.dept_id = department.id;


---

7.3 RIGHT JOIN

Returns all records from right table and matching records from left table.

SELECT student.name, department.dept_name
FROM student
RIGHT JOIN department
ON student.dept_id = department.id;


---

7.4 FULL JOIN

MySQL does not directly support FULL JOIN.

It can be achieved using UNION of LEFT JOIN and RIGHT JOIN.


---

8. Alias

Used to rename table or column temporarily.

Column alias:

SELECT name AS student_name FROM student;

Table alias:

SELECT s.name
FROM student s;


---

Summary

SELECT retrieves data.

WHERE filters data.

ORDER BY sorts data.

LIMIT restricts number of rows.

INNER JOIN returns matching records.

LEFT JOIN returns all left table records.

RIGHT JOIN returns all right table records.

Alias is used for temporary naming.


---
