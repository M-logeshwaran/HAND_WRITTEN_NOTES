📄 07_file_handling_and_csv.md

# File Handling and CSV in Python

This document covers file modes, reading and writing text files, file methods, pointer control, and CSV file handling.

---

# 1. File Handling in Python

File handling allows storing and retrieving data from files.

Basic syntax:

```python
file = open("filename", "mode")
file.close()

Recommended method:

with open("filename", "mode") as file:
    statements

with automatically closes the file.


---

2. File Modes

Mode	Meaning

r	Read (default)
w	Write (overwrites file)
a	Append
r+	Read and Write
rb	Read binary
wb	Write binary
ab	Append binary



---

3. Reading from File


---

3.1 read()

Reads entire file.

with open("data.txt", "r") as f:
    content = f.read()
    print(content)


---

3.2 readline()

Reads one line at a time.

with open("data.txt", "r") as f:
    line = f.readline()
    print(line)


---

3.3 readlines()

Reads all lines into a list.

with open("data.txt", "r") as f:
    lines = f.readlines()
    print(lines)


---

4. Writing to File


---

4.1 write()

with open("data.txt", "w") as f:
    f.write("Hello World")


---

4.2 writelines()

lines = ["Line1\n", "Line2\n"]

with open("data.txt", "w") as f:
    f.writelines(lines)


---

5. File Pointer Methods


---

5.1 tell()

Returns current position of file pointer.

with open("data.txt", "r") as f:
    print(f.tell())


---

5.2 seek()

Moves file pointer.

with open("data.txt", "r") as f:
    f.seek(0)

Seek with offset:

f.seek(5)       # move to 5th byte
f.seek(2, 1)    # relative to current position
f.seek(0, 2)    # move to end of file


---

6. Working with Raw File Paths

Use raw string to avoid escape errors.

path = r"C:\Users\Logesh\data.txt"


---

7. CSV File Handling

Python provides csv module.


---

7.1 Writing CSV File

import csv

with open("students.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerow(["Name", "Age"])
    writer.writerow(["Logesh", 20])


---

7.2 Writing Multiple Rows

rows = [
    ["A", 18],
    ["B", 19]
]

with open("students.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerows(rows)


---

7.3 Reading CSV File

import csv

with open("students.csv", "r") as f:
    reader = csv.reader(f)
    for row in reader:
        print(row)


---

Summary

Files are opened using open().

with statement automatically closes file.

Different modes control reading and writing.

tell() and seek() control file pointer.

csv module helps handle CSV files.


---

Reply:

`Start py 08`
