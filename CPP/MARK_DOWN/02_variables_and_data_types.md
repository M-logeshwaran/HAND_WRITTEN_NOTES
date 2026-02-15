# 📄 `02-variables-and-data-types.md`

````md
# Variables and Data Types in C++

This document covers variable declaration, naming rules, constants, and fundamental data types in C++.

---

## 1. Variables

A variable is a container used to store data in memory.

### 1.1 Declaration

```cpp
int age;
````

This declares a variable named `age` of type `int`.

---

### 1.2 Initialization

```cpp
age = 24;
```

Assigning a value to a variable after declaration.

---

### 1.3 Declaration + Initialization

```cpp
int age = 25;
```

---

### 1.4 Multiple Variable Declaration

```cpp
int num1 = 1, num2 = 2;
```

You can also assign the same value:

```cpp
num1 = num2 = 9;
```

---

## 2. Rules for Naming Variables

* Only letters, numbers, and underscore (`_`) are allowed.
* Cannot start with a number.
* Cannot contain spaces.
* Must not be a reserved keyword.
* Case-sensitive.

Example:

```cpp
int Age;     // different from age
int age_1;   // valid
```

---

## 3. Constants

A constant is a variable whose value cannot be changed after initialization.

```cpp
const int dob = 2000;
```

Rules:

* Must be initialized at declaration.
* Value cannot be modified.
* Attempting to modify results in a compile-time error.

---

## 4. Fundamental Data Types

### 4.1 Integer (`int`)

Stores whole numbers.

```cpp
int age = 24;
```

---

### 4.2 Floating Point Numbers

#### float

* Used for decimal numbers.
* Approx. 6–7 digits precision.
* 4 bytes.

```cpp
float pi = 3.1415;
```

#### double

* Higher precision than float.
* 8 bytes.

```cpp
double pi = 3.1415161478;
```

---

### 4.3 Controlling Decimal Precision

To control precision:

```cpp
#include <iomanip>

double pi = 3.1415161478;
cout << fixed << setprecision(10) << pi;
```

* `fixed` → prevents scientific notation.
* `setprecision()` → controls number of digits after decimal.

---

### 4.4 Boolean (`bool`)

Stores `true` or `false`.

```cpp
bool isAdult = true;
cout << isAdult;
```

Output:

* `1` → true
* `0` → false

---

### 4.5 Character (`char`)

Stores a single character.

```cpp
char gender = 'M';
cout << gender;
```

Characters are stored using ASCII values:

```cpp
char letter = 65;
cout << letter;   // Output: A
```

---

### 4.6 String (Basic)

Used to store text.

```cpp
#include <string>

string greeting = "Hi";
cout << greeting;
```

A string is a sequence of characters.

---

## 5. Memory Size of Data Types

| Data Type | Size (Approx.) |
| --------- | -------------- |
| int       | 4 bytes        |
| float     | 4 bytes        |
| double    | 8 bytes        |
| char      | 1 byte         |
| bool      | 1 byte         |

---

## 6. Finding Size of a Variable

Use `sizeof` operator:

```cpp
int age = 24;
cout << sizeof(age);
```

Example:

```cpp
float gpa = 9.5;
cout << sizeof(gpa);
```

---

## 7. Taking Input for Variables

```cpp
int age;
cout << "Enter your age: ";
cin >> age;
```

The `>>` operator extracts input from the user.

```

---

This file includes:

- Variable rules  
- Declaration & initialization  
- Constants  
- Data types  
- Precision control  
- sizeof operator  
- Basic string introduction  

All based strictly on your notes (cleaned and corrected).

---

Ready for:

📄 `03-operators-and-type-conversion.md` ? 🚀
```
