📄 08_binary_files_and_pickle.md

# Binary Files and Pickle in Python

This document covers binary file handling, serialization, deserialization, and usage of the pickle module.

---

# 1. Binary Files

Binary files store data in binary format instead of plain text.

Binary modes:

| Mode | Meaning |
|------|----------|
| rb | Read binary |
| wb | Write binary |
| ab | Append binary |

---

# 2. What is Serialization?

Serialization is the process of converting a Python object into a byte stream.

Deserialization converts byte stream back into Python object.

Python provides `pickle` module for this purpose.

---

# 3. Using Pickle Module

```python
import pickle


---

4. Writing Object to Binary File (Pickling)

import pickle

data = {"name": "Logesh", "age": 20}

with open("data.dat", "wb") as f:
    pickle.dump(data, f)

dump() writes object to binary file.



---

5. Reading Object from Binary File (Unpickling)

import pickle

with open("data.dat", "rb") as f:
    data = pickle.load(f)
    print(data)

load() reads object from file.



---

6. Reading Multiple Objects

import pickle

with open("data.dat", "rb") as f:
    try:
        while True:
            obj = pickle.load(f)
            print(obj)
    except EOFError:
        pass

EOFError occurs when end of file is reached.


---

7. Example with Class Object

import pickle

class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

s1 = Student("Logesh", 20)

with open("student.dat", "wb") as f:
    pickle.dump(s1, f)

with open("student.dat", "rb") as f:
    obj = pickle.load(f)
    print(obj.name, obj.age)


---

8. Difference Between Text and Binary Files

Text File:

Human readable

Stores data as characters


Binary File:

Not human readable

Stores data in byte format

Faster for complex objects



---

Summary

Binary files use rb, wb, ab modes.

Pickle is used for serialization and deserialization.

dump() writes object.

load() reads object.

EOFError is used when reading multiple objects.


---

Reply:

`Start py 09`
