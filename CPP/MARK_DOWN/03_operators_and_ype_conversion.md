# 📄 `03-operators-and-type-conversion.md`

````md
# Operators and Type Conversion in C++

This document covers arithmetic, assignment, comparison, logical operators, and type conversion.

---

## 1. Arithmetic Operators

Used to perform mathematical operations.

| Operator | Meaning |
|----------|----------|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `%` | Modulus (remainder) |
| `++` | Increment |
| `--` | Decrement |

---

### 1.1 Example

```cpp
int a = 5;
int b = 6;

int sum = a + b;
int diff = a - b;
int product = a * b;
int division = a / b;

cout << "Sum: " << sum << endl;
cout << "Difference: " << diff << endl;
cout << "Product: " << product << endl;
cout << "Division: " << division << endl;
````

---

### 1.2 Integer Division

If both operands are integers:

```cpp
int a = 5;
int b = 6;
int result = a / b;
```

Result: `0` (decimal part is removed)

---

### 1.3 Floating Point Division

```cpp
float result = float(a) / b;
```

or

```cpp
float result = (float)a / b;
```

Now decimal value is preserved.

---

### 1.4 Modulus Operator `%`

Returns remainder.

```cpp
int a = 9;
int b = 5;
int mod = a % b;
```

Output: `4`

---

## 2. Increment and Decrement

### 2.1 Post Increment

```cpp
int a = 15;
a++;
```

Value becomes `16`.

### 2.2 Pre Increment

```cpp
++a;
```

Both increase the value by 1.

Same logic applies for decrement:

```cpp
a--;
--a;
```

---

## 3. Assignment Operators

Used to assign or update values.

| Operator | Example  | Meaning   |
| -------- | -------- | --------- |
| `=`      | `a = 5`  | Assign    |
| `+=`     | `a += 2` | a = a + 2 |
| `-=`     | `a -= 2` | a = a - 2 |
| `*=`     | `a *= 2` | a = a * 2 |
| `/=`     | `a /= 2` | a = a / 2 |

Example:

```cpp
int n1 = 25;
n1 += 1;
```

---

## 4. Comparison Operators

Used to compare values.

| Operator | Meaning               |
| -------- | --------------------- |
| `==`     | Equal to              |
| `!=`     | Not equal             |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |

Example:

```cpp
int n1 = 5, n2 = 8;

cout << (n1 > n2) << endl;
cout << (n1 == n2) << endl;
```

Output:

* `1` → true
* `0` → false

---

## 5. Logical Operators

Used to combine conditions.

| Operator | Meaning |   |    |
| -------- | ------- | - | -- |
| `&&`     | AND     |   |    |
| `        |         | ` | OR |
| `!`      | NOT     |   |    |

---

### 5.1 Truth Table Concept

**AND (`&&`)**

* True only if both operands are true.

**OR (`||`)**

* True if at least one operand is true.

**NOT (`!`)**

* Reverses the condition.

---

### 5.2 Example

```cpp
bool condition = (age >= 18 && gender == 'M');
cout << condition;
```

---

## 6. Type Conversion

### 6.1 Implicit Conversion

Automatically done by compiler.

```cpp
int a = 6.7;
```

Decimal part is removed.

---

### 6.2 Explicit Conversion (Type Casting)

Manually converting type.

```cpp
float b = 6.8;
cout << int(b);
```

Output: `6`

---

## 7. Important Notes

* Integer division removes decimal part.
* Logical operators work with boolean values.
* Type casting helps control data type behavior.
* Comparison operators return boolean values (`1` or `0`).

```

---

This file now covers:

- Arithmetic
- Increment/decrement
- Assignment
- Comparison
- Logical operators
- Truth table idea
- Type conversion

All aligned with your handwritten content, just cleaned and structured.

---

Next:

📄 `04-conditional-statements-and-loops.md`  

Ready? 🚀
```
