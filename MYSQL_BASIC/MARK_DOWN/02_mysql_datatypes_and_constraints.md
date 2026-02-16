📄 02_mysql_datatypes_and_constraints.md

# MySQL Data Types and Constraints

This document covers commonly used MySQL data types and constraints.

---

# 1. Data Types in MySQL

Data types define the type of data that can be stored in a column.

---

## 1.1 Numeric Data Types

| Data Type | Description |
|------------|-------------|
| INT | Integer values |
| FLOAT | Decimal numbers |
| DOUBLE | Large decimal numbers |
| DECIMAL(M,D) | Fixed decimal precision |

Example:

```sql
age INT,
salary DECIMAL(10,2)


---

1.2 String Data Types

Data Type	Description

CHAR(n)	Fixed-length string
VARCHAR(n)	Variable-length string
TEXT	Large text data


Example:

name VARCHAR(50)


---

1.3 Date and Time Data Types

Data Type	Description

DATE	Stores date (YYYY-MM-DD)
TIME	Stores time (HH:MM:SS)
DATETIME	Stores date and time
TIMESTAMP	Date and time with auto update


Example:

dob DATE


---

2. Constraints in MySQL

Constraints enforce rules on table columns.


---

2.1 NOT NULL

Ensures column cannot have NULL value.

name VARCHAR(50) NOT NULL


---

2.2 UNIQUE

Ensures all values are different.

email VARCHAR(100) UNIQUE


---

2.3 PRIMARY KEY

Uniquely identifies each row

Cannot be NULL

Only one primary key per table


id INT PRIMARY KEY


---

2.4 FOREIGN KEY

Maintains relationship between two tables.

FOREIGN KEY (dept_id) REFERENCES department(id)


---

2.5 DEFAULT

Assigns default value.

status VARCHAR(20) DEFAULT 'active'


---

2.6 CHECK

Ensures condition is satisfied.

age INT CHECK (age >= 18)


---

2.7 AUTO_INCREMENT

Automatically increases numeric value.

id INT AUTO_INCREMENT PRIMARY KEY


---

3. Example Table with Constraints

CREATE TABLE student (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    age INT CHECK (age >= 18),
    email VARCHAR(100) UNIQUE,
    status VARCHAR(20) DEFAULT 'active'
);


---

Summary

Data types define column type.

Numeric, String, and Date types are commonly used.

Constraints enforce data integrity.

PRIMARY KEY ensures uniqueness.

FOREIGN KEY maintains relationships.

AUTO_INCREMENT automatically increases values.


---
