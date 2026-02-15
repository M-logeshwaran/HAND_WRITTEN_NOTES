📄 09_exception_handling.md

# Exception Handling in Python

This document covers errors, exceptions, try-except blocks, multiple exceptions, else, finally, raising exceptions, and custom exceptions.

---

# 1. What is an Exception?

An exception is an error that occurs during program execution.

Common errors:

- ZeroDivisionError
- ValueError
- TypeError
- IndexError
- KeyError
- FileNotFoundError

---

# 2. Basic try-except

Syntax:

```python
try:
    statements
except:
    statements

Example:

try:
    a = 10 / 0
except:
    print("Error occurred")


---

3. Handling Specific Exceptions

try:
    num = int(input("Enter number: "))
    result = 10 / num
except ZeroDivisionError:
    print("Cannot divide by zero")
except ValueError:
    print("Invalid input")


---

4. Multiple Exceptions in One Block

try:
    a = int(input())
    b = 10 / a
except (ZeroDivisionError, ValueError) as e:
    print("Error:", e)


---

5. else Block

The else block executes if no exception occurs.

try:
    num = int(input())
except ValueError:
    print("Invalid input")
else:
    print("You entered:", num)


---

6. finally Block

The finally block always executes.

try:
    f = open("data.txt", "r")
except FileNotFoundError:
    print("File not found")
finally:
    print("Execution completed")

Used for cleanup operations like closing files.


---

7. Raising Exceptions

You can manually raise exceptions using raise.

age = int(input("Enter age: "))

if age < 0:
    raise ValueError("Age cannot be negative")


---

8. Custom Exception

Create user-defined exception by inheriting from Exception.

class InvalidAgeError(Exception):
    pass

age = int(input("Enter age: "))

if age < 18:
    raise InvalidAgeError("Age must be 18 or above")


---

9. Using Exception as Object

try:
    a = 10 / 0
except ZeroDivisionError as e:
    print("Error message:", e)


---

Summary

Exceptions are runtime errors.

try block contains risky code.

except handles errors.

else runs if no exception.

finally always executes.

raise is used to generate exceptions.

Custom exceptions can be created.


---

Reply:

`Start py 10`
