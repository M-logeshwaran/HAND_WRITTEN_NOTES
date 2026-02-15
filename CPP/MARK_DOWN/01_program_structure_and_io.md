# 📄 `01-program-structure-and-io.md`

````md
# C++ Program Structure and Input/Output

This document covers the basic structure of a C++ program and standard input/output operations.

---

## 1. Basic Structure of a C++ Program

A minimal C++ program looks like this:

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello World";
    return 0;
}
````

### Explanation:

* `#include <iostream>`
  Includes the standard input/output library.

* `using namespace std;`
  Allows direct use of standard library features like `cout` and `cin` without prefixing `std::`.

* `int main()`
  Entry point of the program. Execution starts from here.

* `return 0;`
  Indicates successful execution.

---

## 2. Using std:: Without Namespace

If `using namespace std;` is not used:

```cpp
#include <iostream>

int main() {
    std::cout << "Hello World";
    return 0;
}
```

`std::` must be explicitly mentioned before `cout`.

---

## 3. Output in C++

### 3.1 Printing Output

```cpp
cout << "Hello";
```

The `<<` operator is called the **insertion operator**.

---

### 3.2 Printing Multiple Values

```cpp
int age = 18;
cout << "I am " << age << " years old";
```

---

### 3.3 New Line Methods

**Method 1: Using `\n`**

```cpp
cout << "Hello\n";
```

**Method 2: Using `endl`**

```cpp
cout << "Hello" << endl;
```

Both move the cursor to the next line.

---

## 4. Escape Sequences

Escape sequences are special characters used inside strings.

| Escape Sequence | Meaning             |
| --------------- | ------------------- |
| `\n`            | New line            |
| `\t`            | Tab space           |
| `\"`            | Print double quotes |
| `\a`            | Alert sound         |

Example:

```cpp
cout << "Hello\tWorld";
cout << "She said \"Hi\"";
```

---

## 5. Input in C++

### 5.1 Taking Integer Input

```cpp
int age;
cout << "Enter your age: ";
cin >> age;
cout << age;
```

The `>>` operator is called the **extraction operator**.

---

### 5.2 Taking Multiple Inputs

```cpp
int n1, n2;
cin >> n1 >> n2;
```

Inputs must be separated by space or newline.

---

## 6. Single Line vs Multi Line Output

Single line:

```cpp
cout << "Hello World";
```

Multi-line:

```cpp
cout << "Line 1" << endl;
cout << "Line 2";
```

---

## 7. Important Notes

* `main()` is the starting point of execution.
* Statements must end with a semicolon `;`.
* C++ is case-sensitive.
* If `std` is not imported, `std::` must be used explicitly.

```

---

This file strictly follows your handwritten content:
- Program structure
- cout / cin
- insertion/extraction operator
- namespace usage
- escape sequences
- new line methods

Clean. Professional. No unnecessary extra theory.

---

If this formatting is good, I’ll generate:

📄 `02-variables-and-data-types.md`

Let me know if you want any small style tweak before we continue.
```
