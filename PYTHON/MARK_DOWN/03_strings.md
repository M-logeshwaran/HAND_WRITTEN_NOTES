📄 03_strings.md

# Strings in Python

This document covers string creation, immutability, indexing, slicing, operations, comparison, and commonly used string methods.

---

# 1. Introduction to Strings

A string is a sequence of characters enclosed in:

- Single quotes → 'Hello'
- Double quotes → "Python"

Example:

```python
name = "Logesh"

Strings are immutable (cannot be changed after creation).


---

2. String Immutability

Once created, a string cannot be modified.

text = "Python"
text[0] = "J"   # Error

To modify, create a new string:

text = "J" + text[1:]


---

3. Indexing

Each character has an index.

Positive indexing starts from 0.

P  y  t  h  o  n
0  1  2  3  4  5

Negative indexing starts from -1.

P  y  t  h  o  n
-6 -5 -4 -3 -2 -1

Example:

word = "Python"
print(word[0])
print(word[-1])


---

4. Slicing

Syntax:

string[start : stop : step]

Example:

text = "Python"

print(text[0:4])
print(text[::2])
print(text[::-1])


---

5. String Operations


---

5.1 Concatenation

a = "Hello"
b = "World"

print(a + b)


---

5.2 Repetition

print("Hi" * 3)


---

5.3 Membership

text = "Python"

print("P" in text)
print("z" not in text)


---

5.4 Comparison

Strings are compared lexicographically.

print("apple" < "banana")


---

6. Built-in String Functions


---

6.1 len()

Returns length of string.

print(len("Python"))


---

7. Common String Methods


---

7.1 capitalize()

text = "python"
print(text.capitalize())


---

7.2 lower() and upper()

text = "Python"
print(text.lower())
print(text.upper())


---

7.3 title()

text = "python programming"
print(text.title())


---

7.4 strip()

Removes leading and trailing spaces.

text = "  Python  "
print(text.strip())


---

7.5 count()

text = "banana"
print(text.count("a"))


---

7.6 find()

Returns index if found, otherwise -1.

text = "Python"
print(text.find("th"))


---

7.7 index()

Similar to find but raises error if not found.

print(text.index("th"))


---

7.8 replace()

text = "Python"
print(text.replace("Python", "Java"))


---

7.9 split()

Splits string into list.

text = "Python is easy"
print(text.split())


---

7.10 partition()

Splits into three parts.

text = "apple-banana"
print(text.partition("-"))


---

7.11 startswith() and endswith()

text = "Python"

print(text.startswith("Py"))
print(text.endswith("on"))


---

7.12 isalpha(), isdigit(), isalnum()

print("abc".isalpha())
print("123".isdigit())
print("abc123".isalnum())


---

8. String Formatting (f-strings)

Used to format values inside string.

name = "Logesh"
age = 20

print(f"My name is {name} and I am {age} years old")


---

Summary

Strings are immutable sequences of characters.

Support indexing and slicing.

Can be concatenated and repeated.

Many built-in methods help in string manipulation.

f-strings provide clean formatting.


---

Next:

👉 `Start py 04`  
(Data Structures: List, Tuple, Dictionary — this one will be detailed)
