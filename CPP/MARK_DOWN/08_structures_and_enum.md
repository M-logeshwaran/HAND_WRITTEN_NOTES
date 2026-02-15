# 📄 `08-structures-and-enum.md`

````md
# Structures and Enum in C++

This document covers structures (struct), accessing members, arrays of structures, and enumerations (enum).

---

# 1. Structure in C++

A structure is a user-defined data type that groups related variables of different data types.

---

## 1.1 Syntax

```cpp
struct structureName {
    datatype variable1;
    datatype variable2;
};
````

---

## 1.2 Example

```cpp
#include <iostream>
using namespace std;

struct Student {
    string name;
    int age;
    float marks;
};

int main() {
    Student s1;

    s1.name = "Logesh";
    s1.age = 20;
    s1.marks = 85.5;

    cout << s1.name << endl;
    cout << s1.age << endl;
    cout << s1.marks << endl;

    return 0;
}
```

---

# 2. Structure Initialization

```cpp
Student s1 = {"Logesh", 20, 85.5};
```

---

# 3. Array of Structures

```cpp
Student students[2];

students[0] = {"A", 18, 75.5};
students[1] = {"B", 19, 88.0};
```

---

# 4. Nested Structure

```cpp
struct Address {
    string city;
    int pincode;
};

struct Person {
    string name;
    Address addr;
};

Person p1;
p1.name = "Logesh";
p1.addr.city = "Chennai";
p1.addr.pincode = 600001;
```

---

# 5. Structure vs Class

* `struct` → members are public by default.
* `class` → members are private by default.

Both are similar in C++.

---

# 6. Enum in C++

Enum (enumeration) is a user-defined type consisting of named integer constants.

---

## 6.1 Syntax

```cpp
enum enumName {
    value1,
    value2,
    value3
};
```

---

## 6.2 Example

```cpp
enum Day {
    Monday,
    Tuesday,
    Wednesday,
    Thursday,
    Friday
};

int main() {
    Day today = Wednesday;
    cout << today;
}
```

Output:
2

(Default numbering starts from 0)

---

## 6.3 Custom Values

```cpp
enum Level {
    Low = 1,
    Medium = 5,
    High = 10
};
```

---

# 7. Typedef with Struct (Optional Improvement)

```cpp
typedef struct {
    string name;
    int age;
} Person;
```

Now we can write:

```cpp
Person p1;
```

---

# Summary

* Structure groups related variables.
* Access members using `.` operator.
* Structures can be nested.
* Enum represents named integer constants.
* Default enum values start from 0.
* `struct` and `class` differ mainly in default access specifier.

```

---

Next:

📄 `09-object-oriented-programming.md`

Now we step into constructors, classes, objects, encapsulation 😌🔥
```
