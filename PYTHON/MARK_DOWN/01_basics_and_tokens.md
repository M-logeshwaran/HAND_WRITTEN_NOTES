📄 01_basics_and_tokens.md

# Basics and Tokens in Python

This document covers the fundamental building blocks of Python including tokens, variables, data types, type conversion, and identity behavior.

---

# 1. Introduction to Python

Python is a high-level, interpreted programming language known for its simplicity and readability.

- Case-sensitive language
- No need for data type declaration
- Indentation is mandatory

---

# 2. Tokens in Python

Tokens are the smallest units of a Python program.

There are five types of tokens:

1. Keywords
2. Identifiers
3. Literals
4. Operators
5. Punctuators (Delimiters)

---

## 2.1 Keywords

Keywords are reserved words that have special meaning in Python.

Examples:

if, else, elif, while, for, break, continue, def, return, class, try, except, import, True, False, None, global

Keywords cannot be used as variable names.

---

## 2.2 Identifiers

Identifiers are names given to:

- Variables
- Functions
- Classes
- Modules

Rules:

- Must start with a letter (a-z, A-Z) or underscore (_)
- Cannot start with a number
- Can contain letters, numbers, underscore
- Case-sensitive

Valid examples:

```python
name
_age
student1

Invalid examples:

1name
class


---

2.3 Literals

Literals represent fixed values.

Types of Literals:

1. Numeric Literals

Integer → 10

Float → 3.14

Complex → 2+3j



2. String Literals

"Hello"

'Python'



3. Boolean Literals

True

False



4. Special Literal

None





---

2.4 Operators

Operators are symbols used to perform operations.

Example:

a = 10
b = 20
c = a + b

(Operators will be discussed in detail in next document.)


---

2.5 Punctuators (Delimiters)

Symbols used to structure code:

( )  { }  [ ]  ,  :  ;  .  =


---

3. Variables in Python

Variables are used to store data.

Python does not require explicit type declaration.

Example:

a = 10
name = "Logesh"
marks = 85.5

Type is determined automatically.


---

4. Multiple Assignment

4.1 Same Value to Multiple Variables

a = b = c = 10

All variables store 10.


---

4.2 Multiple Values in One Line

x, y, z = 10, 20, 30

This is called unpacking.


---

5. Type Checking

Use type() to check data type.

a = 10
print(type(a))


---

6. Type Conversion

6.1 Implicit Type Conversion

Python automatically converts smaller type to larger type.

a = 10
b = 5.5
c = a + b

Result becomes float.


---

6.2 Explicit Type Conversion

Manual conversion using:

int()
float()
str()
bool()

Example:

x = "10"
y = int(x)


---

7. Identity Operators

Used to compare memory location.

is

is not


Example:

a = 10
b = 10

print(a is b)


---

8. id() Function

Returns memory address of an object.

x = 100
print(id(x))


---

Summary

Tokens are smallest units of Python.

Python is dynamically typed.

Variables do not require explicit declaration.

Type conversion can be implicit or explicit.

is compares memory identity.

id() returns memory address.


---

Tell me when to continue:

👉 `Start py 02`  

We go operators and control flow next. 🔥
