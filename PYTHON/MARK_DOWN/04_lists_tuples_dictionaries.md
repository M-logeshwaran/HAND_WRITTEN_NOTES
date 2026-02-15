📄 04_lists_tuples_dictionaries.md

# Lists, Tuples and Dictionaries in Python

This document covers creation, properties, operations, slicing, comparison, mutability, and commonly used methods for lists, tuples, and dictionaries.

---

# 1. Lists in Python

A list is an ordered, mutable collection of elements.

Lists are written using square brackets [].

Example:

```python
numbers = [10, 20, 30, 40]


---

1.1 Properties of Lists

Ordered

Mutable (can be modified)

Allows duplicate values

Can store different data types


Example:

data = [10, "Python", 3.14]


---

1.2 Accessing List Elements

Using indexing:

lst = [10, 20, 30]
print(lst[0])
print(lst[-1])


---

1.3 List Slicing

lst = [1, 2, 3, 4, 5]

print(lst[1:4])
print(lst[::-1])


---

1.4 List Operations

Concatenation

a = [1, 2]
b = [3, 4]
print(a + b)

Repetition

print([1, 2] * 2)

Membership

print(2 in [1, 2, 3])

Comparison

Lists are compared element by element.

print([1, 2] == [1, 2])


---

1.5 Copy vs Reference

Reference:

a = [1, 2]
b = a

Both refer to same memory.

Copy:

a = [1, 2]
b = a.copy()

Now both are separate objects.


---

1.6 List Methods


---

append()

Adds single element.

lst = [1, 2]
lst.append(3)


---

extend()

Adds multiple elements.

lst.extend([4, 5])


---

insert()

lst.insert(1, 100)


---

remove()

Removes first occurrence.

lst.remove(100)


---

pop()

Removes element by index.

lst.pop()
lst.pop(0)


---

clear()

lst.clear()


---

count()

lst = [1, 2, 2, 3]
print(lst.count(2))


---

index()

print(lst.index(2))


---

reverse()

lst.reverse()


---

min(), max(), sum()

print(min(lst))
print(max(lst))
print(sum(lst))


---

2. Tuples in Python

A tuple is an ordered, immutable collection.

Tuples are written using parentheses ().

Example:

t = (10, 20, 30)


---

2.1 Properties of Tuples

Ordered

Immutable

Allows duplicates

Faster than lists



---

2.2 Single Element Tuple

Must include comma:

t = (10,)


---

2.3 Tuple Access and Slicing

t = (1, 2, 3, 4)

print(t[1])
print(t[1:3])


---

2.4 Tuple Methods

Tuples have limited methods.

count()

t.count(2)

index()

t.index(3)


---

2.5 sorted()

Returns a list.

t = (3, 1, 2)
print(sorted(t))


---

3. Dictionaries in Python

A dictionary stores data in key-value pairs.

Written using curly braces {}.

Example:

student = {
    "name": "Logesh",
    "age": 20
}


---

3.1 Properties of Dictionary

Unordered (insertion order preserved in Python 3.7+)

Mutable

Keys must be immutable

No duplicate keys



---

3.2 Accessing Values

print(student["name"])

Using get():

print(student.get("age"))


---

3.3 Adding and Updating

student["marks"] = 90
student["age"] = 21


---

3.4 Removing Elements

student.pop("age")
student.popitem()
student.clear()


---

3.5 Dictionary Methods

keys()

print(student.keys())

values()

print(student.values())

items()

print(student.items())

update()

student.update({"city": "Chennai"})

copy()

new_student = student.copy()

setdefault()

student.setdefault("grade", "A")

fromkeys()

keys = ["a", "b"]
d = dict.fromkeys(keys, 0)


---

3.6 Nested Dictionary

data = {
    "student1": {"name": "A", "age": 18},
    "student2": {"name": "B", "age": 19}
}


---

Summary

List → Mutable, ordered sequence.

Tuple → Immutable, ordered sequence.

Dictionary → Key-value mapping, mutable.

Lists have many modification methods.

Tuples are immutable and faster.

Dictionary keys must be immutable.


---

Next:

👉 `Start py 05`  
(Functions & Scope — detailed)
