📄 06_mysql_with_python.md

# MySQL with Python (MySQL Connector)

This document covers connecting MySQL with Python, executing queries, fetching data, and understanding return formats.

---

# 1. Installing MySQL Connector

Install using pip:

```bash
pip install mysql-connector-python


---

2. Import Module

import mysql.connector


---

3. Connecting to MySQL

import mysql.connector

conn = mysql.connector.connect(
    host="localhost",
    user="root",
    password="your_password",
    database="college"
)

print("Connected successfully")


---

4. Creating Cursor

Cursor is used to execute SQL queries.

cursor = conn.cursor()

If dictionary format is needed:

cursor = conn.cursor(dictionary=True)


---

5. Executing Query

cursor.execute("SELECT * FROM student")


---

6. Fetching Data

6.1 fetchone()

Returns one row.

row = cursor.fetchone()
print(row)

Return Format:

Single row

Tuple format


Example output:

(1, 'Ram', 20)

Type:

<class 'tuple'>


---

6.2 fetchall()

Returns all rows.

rows = cursor.fetchall()
print(rows)

Return Format:

List of tuples


Example output:

[(1, 'Ram', 20), (2, 'Ravi', 22)]

Type:

<class 'list'>

Each row inside list is a tuple.


---

6.3 fetchmany(n)

Returns specified number of rows.

rows = cursor.fetchmany(2)
print(rows)

Return Format:

List of tuples

Contains n rows


Example output:

[(1, 'Ram', 20), (2, 'Ravi', 22)]


---

7. Accessing Returned Data

Since rows are tuples:

row = (1, 'Ram', 20)

print(row[0])  # id
print(row[1])  # name
print(row[2])  # age

For fetchall():

for row in rows:
    print(row[1])  # print name


---

8. Dictionary Format (Optional)

If cursor is created with:

cursor = conn.cursor(dictionary=True)

Now data is returned as dictionary.

Example output:

{'id': 1, 'name': 'Ram', 'age': 20}

Type:

<class 'dict'>

Access using column name:

print(row['name'])


---

9. Inserting Data

query = "INSERT INTO student (id, name, age) VALUES (%s, %s, %s)"
values = (3, "Kumar", 21)

cursor.execute(query, values)
conn.commit()

commit() is required to save changes.


---

10. Updating Data

cursor.execute("UPDATE student SET age = 22 WHERE id = 3")
conn.commit()


---

11. Deleting Data

cursor.execute("DELETE FROM student WHERE id = 3")
conn.commit()


---

12. Closing Connection

cursor.close()
conn.close()

Always close connection after operations.


---

Summary

Install mysql-connector-python.

Use connect() to establish connection.

Use cursor() to execute queries.

execute() runs SQL command.

fetchone() → returns tuple.

fetchall() → returns list of tuples.

fetchmany(n) → returns list of tuples.

Use dictionary=True for dictionary format.

commit() saves changes.

Always close connection.
