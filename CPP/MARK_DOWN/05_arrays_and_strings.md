# 📄 `05-arrays-and-strings.md`

````md
# Arrays and Strings in C++

This document covers one-dimensional arrays, multi-dimensional arrays, and string handling.

---

# 1. Arrays

An array stores multiple values of the same data type in a single variable.

---

## 1.1 Declaring an Array

Syntax:

```cpp
datatype arrayName[size];
````

Example:

```cpp
int numbers[5];
```

---

## 1.2 Initializing an Array

```cpp
int numbers[5] = {10, 20, 30, 40, 50};
```

Or:

```cpp
int numbers[] = {10, 20, 30};
```

Size is automatically determined.

---

## 1.3 Accessing Array Elements

Array index starts from 0.

```cpp
cout << numbers[0];
cout << numbers[1];
```

---

## 1.4 Taking Input into Array

```cpp
int n = 5;
int arr[5];

for (int i = 0; i < n; i++) {
    cin >> arr[i];
}
```

---

## 1.5 Printing Array

```cpp
for (int i = 0; i < 5; i++) {
    cout << arr[i] << " ";
}
```

---

## 1.6 Finding Sum of Array Elements

```cpp
int sum = 0;

for (int i = 0; i < 5; i++) {
    sum += arr[i];
}

cout << "Sum: " << sum;
```

---

# 2. Multi-Dimensional Arrays

## 2.1 2D Array Declaration

```cpp
int matrix[2][3];
```

---

## 2.2 Initialization

```cpp
int matrix[2][3] = {
    {1, 2, 3},
    {4, 5, 6}
};
```

---

## 2.3 Accessing Elements

```cpp
cout << matrix[0][1];
```

---

## 2.4 Input and Output in 2D Array

```cpp
int matrix[2][2];

for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 2; j++) {
        cin >> matrix[i][j];
    }
}
```

Printing:

```cpp
for (int i = 0; i < 2; i++) {
    for (int j = 0; j < 2; j++) {
        cout << matrix[i][j] << " ";
    }
    cout << endl;
}
```

---

# 3. Strings in C++

C++ supports two types of strings:

1. C-style strings (character arrays)
2. `string` class (recommended)

---

# 4. C-Style Strings

Declared as character arrays.

```cpp
char name[10] = "Logesh";
```

---

## 4.1 Reading String

```cpp
char name[20];
cin >> name;
```

Note:
`cin` stops reading at space.

---

# 5. String Class

Requires:

```cpp
#include <string>
```

---

## 5.1 Declaration

```cpp
string name = "Logesh";
```

---

## 5.2 Input with Space

```cpp
string fullName;
getline(cin, fullName);
```

---

## 5.3 Common String Functions

```cpp
string text = "Hello";

cout << text.length() << endl;
cout << text.size() << endl;
cout << text[0] << endl;
cout << text.at(1) << endl;
```

---

## 5.4 String Concatenation

```cpp
string first = "Hello";
string second = "World";

string result = first + " " + second;
```

---

## 5.5 Compare Strings

```cpp
string a = "Hello";
string b = "Hello";

if (a == b) {
    cout << "Equal";
}
```

---

# 6. Looping Through String

```cpp
string text = "Hello";

for (int i = 0; i < text.length(); i++) {
    cout << text[i] << endl;
}
```

---

# Summary

* Arrays store multiple values of same type.
* Index starts from 0.
* 2D arrays are arrays of arrays.
* C-style strings are character arrays.
* `string` class is easier and recommended.
* `getline()` reads full line including spaces.

```

---

Next:

📄 `06-functions-and-scope.md`

Now we step into structured programming concepts 🔥
```
