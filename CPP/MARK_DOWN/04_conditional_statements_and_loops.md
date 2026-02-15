# 📄 `04-conditional-statements-and-loops.md`

````md
# Conditional Statements and Loops in C++

This document covers decision-making statements and looping constructs.

---

# 1. Conditional Statements

Conditional statements allow a program to execute code based on a condition.

---

## 1.1 if Statement

Syntax:

```cpp
if (condition) {
    // code block
}
````

Example:

```cpp
int age = 20;

if (age >= 18) {
    cout << "You are an adult";
}
```

---

## 1.2 if-else Statement

```cpp
if (age >= 18) {
    cout << "You are an adult";
} else {
    cout << "You are a child";
}
```

---

## 1.3 else-if Ladder

Used when multiple conditions exist.

```cpp
if (age < 18) {
    cout << "Child";
} else if (age >= 60) {
    cout << "Senior Citizen";
} else {
    cout << "Adult";
}
```

---

## 1.4 Nested if (Leap Year Example)

```cpp
int year;
cin >> year;

if (year % 100 == 0) {
    if (year % 400 == 0) {
        cout << "Leap Year";
    } else {
        cout << "Not a Leap Year";
    }
} else if (year % 4 == 0) {
    cout << "Leap Year";
} else {
    cout << "Not a Leap Year";
}
```

---

## 1.5 Ternary Operator

Short form of if-else.

Syntax:

```cpp
(condition) ? statement1 : statement2;
```

Example:

```cpp
int age = 14;
(age < 18) ? cout << "Child" : cout << "Adult";
```

---

## 1.6 Switch Statement

Alternative to multiple if-else statements.

```cpp
int day = 2;

switch (day) {
    case 1:
        cout << "Monday";
        break;
    case 2:
        cout << "Tuesday";
        break;
    case 3:
        cout << "Wednesday";
        break;
    default:
        cout << "Invalid day";
}
```

### Important:

* `break` prevents fall-through.
* `default` executes if no case matches.

---

# 2. Looping Statements

Loops are used to repeat a block of code.

---

## 2.1 while Loop (Entry-Controlled)

Syntax:

```cpp
while (condition) {
    // code
}
```

Example:

```cpp
int i = 1;
int n = 5;

while (i <= n) {
    cout << i << endl;
    i++;
}
```

---

## 2.2 do-while Loop (Exit-Controlled)

Runs at least once.

```cpp
int i = 1;
int n = 5;

do {
    cout << i << endl;
    i++;
} while (i <= n);
```

---

## 2.3 for Loop

Most commonly used loop.

Syntax:

```cpp
for (initialization; condition; increment) {
    // code
}
```

Example:

```cpp
for (int i = 1; i <= 5; i++) {
    cout << i << endl;
}
```

---

## 2.4 Nested Loops

Loop inside another loop.

```cpp
for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
        cout << i << " " << j << endl;
    }
}
```

---

# 3. Break and Continue

## 3.1 break

Stops the loop completely.

```cpp
for (int i = 0; i <= 10; i++) {
    if (i == 5)
        break;
    cout << i << endl;
}
```

---

## 3.2 continue

Skips current iteration.

```cpp
for (int i = 0; i <= 8; i++) {
    if (i % 2 != 0)
        continue;
    cout << i << endl;
}
```

Output:
0 2 4 6 8

---

# 4. Math Functions

Requires:

```cpp
#include <cmath>
```

Common functions:

```cpp
cout << max(5, 7) << endl;
cout << min(5, 7) << endl;
cout << sqrt(81) << endl;
cout << pow(9, 3) << endl;
cout << round(5.4) << endl;
cout << ceil(5.4) << endl;
cout << floor(5.6) << endl;
cout << log(2) << endl;
```

---

# Summary

* `if`, `else`, `switch` → decision making
* `while`, `do-while`, `for` → repetition
* `break` and `continue` control loop execution
* Math functions require `<cmath>`

```

---

This covers everything from your conditional + looping section + math functions.

Next:

📄 `05-arrays-and-strings.md`

We’re entering structured data now 😌🔥
```
