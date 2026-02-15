📄 02_operators_and_control_flow.md

# Operators and Control Flow in Python

This document covers arithmetic, relational, logical, bitwise, identity, membership operators, operator precedence, and control flow statements.

---

# 1. Operators in Python

Operators are symbols used to perform operations on variables and values.

---

1.1 Arithmetic Operators

Used for mathematical operations.

| Operator | Meaning |
|----------|----------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division (float result) |
| // | Floor Division |
| % | Modulus (Remainder) |
| ** | Exponent |

Example:

```python
a = 10
b = 3

print(a + b)
print(a // b)
print(a % b)
print(a ** b)


---

1.2 Relational (Comparison) Operators

Used to compare values.

Operator	Meaning

==	Equal to
!=	Not equal to
>	Greater than
<	Less than
>=	Greater than or equal
<=	Less than or equal


Example:

a = 10
b = 20

print(a == b)
print(a < b)

Returns Boolean values (True / False).


---

1.3 Logical Operators

Used to combine conditions.

Operator	Meaning

and	True if both are True
or	True if at least one is True
not	Reverse the condition


Example:

a = 10
b = 20

print(a < b and b > 5)
print(not(a > b))


---

1.4 Bitwise Operators

Operate on binary representation.

Operator	Meaning

&	AND
	
^	XOR
~	NOT
<<	Left Shift
>>	Right Shift


Example:

a = 5   # 0101
b = 3   # 0011

print(a & b)
print(a | b)
print(a << 1)


---

1.5 Identity Operators

Used to compare memory location.

is

is not


Example:

a = [1, 2]
b = a

print(a is b)


---

1.6 Membership Operators

Used to check presence in sequence.

in

not in


Example:

text = "Python"

print("P" in text)
print("z" not in text)


---

# 2. Operator Precedence

Order of evaluation (high to low):

1. **


2. *, /, //, %


3. +, -


4. Relational operators


5. not


6. and


7. or



Example:

result = 10 + 5 * 2
print(result)

Multiplication happens first.


---

# 3. Control Flow Statements

Control flow statements decide how program executes.


---

3.1 if Statement

age = 18

if age >= 18:
    print("Eligible")


---

3.2 if-else Statement

if age >= 18:
    print("Eligible")
else:
    print("Not Eligible")


---

3.3 if-elif-else Ladder

marks = 85

if marks >= 90:
    print("Grade A")
elif marks >= 75:
    print("Grade B")
else:
    print("Grade C")


---

3.4 Nested if

num = 10

if num > 0:
    if num % 2 == 0:
        print("Positive Even")


---

# 4. Looping Statements


---

4.1 for Loop

Used to iterate over sequence.

for i in range(5):
    print(i)


---

4.2 range() Function

Syntax:

range(start, stop, step)

Example:

for i in range(1, 10, 2):
    print(i)


---

4.3 while Loop

Used when number of iterations is not fixed.

count = 1

while count <= 5:
    print(count)
    count += 1


---

4.4 break Statement

Stops loop immediately.

for i in range(10):
    if i == 5:
        break
    print(i)


---

4.5 continue Statement

Skips current iteration.

for i in range(5):
    if i == 2:
        continue
    print(i)


---

# Summary

Python supports arithmetic, logical, relational, bitwise, identity, and membership operators.

Operator precedence determines execution order.

if-elif-else controls decision making.

for and while are looping constructs.

break and continue control loop execution.


---

Tell me when to continue:

👉 `Start py 03` (Strings — detailed section from your notes) 🔥
