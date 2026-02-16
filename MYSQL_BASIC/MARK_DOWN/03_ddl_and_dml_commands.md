📄 03_ddl_and_dml_commands.md

# DDL and DML Commands in MySQL

This document covers Data Definition Language (DDL) and Data Manipulation Language (DML) commands.

---

# 1. SQL Command Categories

SQL commands are mainly divided into:

- DDL (Data Definition Language)
- DML (Data Manipulation Language)
- DQL (Data Query Language)
- DCL (Data Control Language)
- TCL (Transaction Control Language)

This document focuses on DDL and DML.

---

# 2. DDL (Data Definition Language)

DDL commands are used to define and modify database structure.

---

## 2.1 CREATE

Used to create database or table.

Create Database:

```sql
CREATE DATABASE college;

Create Table:

CREATE TABLE student (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);


---

2.2 DROP

Used to delete database or table.

Drop Database:

DROP DATABASE college;

Drop Table:

DROP TABLE student;


---

2.3 ALTER

Used to modify table structure.

Add Column:

ALTER TABLE student ADD email VARCHAR(100);

Modify Column:

ALTER TABLE student MODIFY age INT;

Drop Column:

ALTER TABLE student DROP email;


---

2.4 TRUNCATE

Deletes all records from table but keeps structure.

TRUNCATE TABLE student;

Difference:

DELETE removes row by row.

TRUNCATE removes all rows instantly.



---

3. DML (Data Manipulation Language)

DML commands are used to manipulate data inside tables.


---

3.1 INSERT

Insert single record:

INSERT INTO student VALUES (1, 'Ram', 20);

Insert with column names:

INSERT INTO student (id, name, age)
VALUES (2, 'Ravi', 22);


---

3.2 UPDATE

Used to modify existing records.

UPDATE student
SET age = 21
WHERE id = 1;

If WHERE is not used, all rows will be updated.


---

3.3 DELETE

Used to remove records.

DELETE FROM student
WHERE id = 1;

Without WHERE, all records will be deleted.


---

4. Difference Between DELETE and TRUNCATE

DELETE	TRUNCATE

Removes specific rows	Removes all rows
Can use WHERE	Cannot use WHERE
Slower	Faster
Can rollback (in transaction)	Cannot rollback in some cases



---

Summary

DDL modifies database structure.

CREATE, DROP, ALTER, TRUNCATE are DDL commands.

DML modifies table data.

INSERT, UPDATE, DELETE are DML commands.

WHERE clause is important in UPDATE and DELETE.


---
