📄 06_modules_and_packages.md

# Modules and Packages in Python

This document covers creating modules, importing modules, different import styles, built-in modules, and basic package structure.

---

# 1. What is a Module?

A module is a Python file containing variables, functions, or classes.

Example file: mymodule.py

```python
def greet(name):
    return f"Hello {name}"

pi = 3.14


---

2. Importing a Module


---

2.1 Import Entire Module

import mymodule

print(mymodule.greet("Logesh"))
print(mymodule.pi)


---

2.2 Import Specific Members

from mymodule import greet

print(greet("Logesh"))


---

2.3 Import Multiple Members

from mymodule import greet, pi


---

2.4 Import with Alias

import mymodule as mm

print(mm.pi)


---

2.5 Import All (Not Recommended)

from mymodule import *


---

3. Built-in Modules


---

3.1 math Module

import math

print(math.sqrt(25))
print(math.ceil(4.3))
print(math.floor(4.7))
print(math.pow(2, 3))


---

3.2 random Module

import random

print(random.randint(1, 10))
print(random.random())
print(random.choice([1, 2, 3]))


---

3.3 statistics Module

import statistics

data = [10, 20, 30, 40]

print(statistics.mean(data))
print(statistics.median(data))
print(statistics.mode(data))


---

4. The name Variable

Every Python file has a special variable called __name__.

When a file is run directly:

print(__name__)

It prints:

__main__

Common usage:

if __name__ == "__main__":
    print("Executed directly")


---

5. What is a Package?

A package is a collection of modules inside a folder.

Example structure:

mypackage/
    __init__.py
    module1.py
    module2.py

Import from package:

from mypackage import module1


---

Summary

A module is a Python file.

Modules are imported using import.

Built-in modules provide ready-to-use functions.

__name__ helps identify execution context.

A package is a folder containing modules.


---

Reply with:

`Start py 07`
