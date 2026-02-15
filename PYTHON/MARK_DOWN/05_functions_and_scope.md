📄 05_functions_and_scope.md

# Functions and Scope in Python

This document covers user-defined functions, parameters, return values, argument types, scope rules, and namespace behavior.

---

# 1. Introduction to Functions

A function is a reusable block of code that performs a specific task.

Syntax:

```python
def function_name(parameters):
    statements
    return value

Example:

def add(a, b):
    return a + b

result = add(10, 20)
print(result)


---

2. Types of Functions

2.1 Built-in Functions

Examples:

print()
len()
type()
id()
int()
float()
str()
bool()


---

2.2 User-Defined Functions

Created using the def keyword.

def greet():
    print("Hello")


---

3. Function Parameters


---

3.1 Positional Arguments

Arguments must follow correct order.

def display(name, age):
    print(name, age)

display("Logesh", 20)


---

3.2 Keyword Arguments

Arguments passed using parameter names.

display(age=20, name="Logesh")


---

3.3 Default Arguments

def greet(name="Guest"):
    print("Hello", name)

greet()
greet("Logesh")


---

3.4 Combination of Arguments

Positional arguments must come before keyword arguments.

Correct:

display("Logesh", age=20)

Incorrect:

display(name="Logesh", 20)   # Error


---

4. Return Statement

Used to send value back to caller.

def square(n):
    return n * n

If no return statement, function returns None.


---

5. Scope and Namespace

Python follows LEGB rule:

L – Local

E – Enclosing

G – Global

B – Built-in



---

5.1 Local Scope

Variables defined inside a function.

def test():
    x = 10
    print(x)


---

5.2 Global Scope

Variables defined outside function.

x = 100

def show():
    print(x)


---

5.3 Modifying Global Variable

Use global keyword.

x = 10

def modify():
    global x
    x = 20


---

6. Mutable and Immutable Behavior


---

6.1 Immutable Example

def change(x):
    x = 50

a = 10
change(a)
print(a)

Original value remains unchanged.


---

6.2 Mutable Example

def modify(lst):
    lst.append(100)

mylist = [1, 2, 3]
modify(mylist)
print(mylist)

Original list gets modified.


---

7. Nested Functions (Enclosing Scope)

def outer():
    x = 10

    def inner():
        print(x)

    inner()


---

8. Anonymous Function (Lambda)

square = lambda x: x * x
print(square(5))


---

9. Recursion

A function calling itself.

def factorial(n):
    if n == 1:
        return 1
    return n * factorial(n - 1)


---

Summary

Functions improve modularity and reusability.

Arguments can be positional, keyword, or default.

Scope follows LEGB rule.

Mutable objects can be modified inside functions.

Lambda creates anonymous functions.

Recursion allows function to call itself.


---

`Start py 06`
