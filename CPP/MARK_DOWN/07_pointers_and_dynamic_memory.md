# 📄 `07-pointers-and-dynamic-memory.md`

````md
# Pointers and Dynamic Memory in C++

This document covers pointers, address operators, dereferencing, and dynamic memory allocation using new and delete.

---

# 1. What is a Pointer?

A pointer is a variable that stores the address of another variable.

---

# 2. Address Operator (&)

Used to get the memory address of a variable.

```cpp
int a = 10;
cout << &a;
````

---

# 3. Declaring a Pointer

Syntax:

```cpp
datatype *pointerName;
```

Example:

```cpp
int a = 10;
int *ptr = &a;
```

---

# 4. Dereferencing Operator (*)

Used to access the value stored at the address.

```cpp
cout << *ptr;
```

Output:
10

````

---

# 5. Example Program

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 5;
    int *ptr = &a;

    cout << "Value of a: " << a << endl;
    cout << "Address of a: " << &a << endl;
    cout << "Pointer value: " << ptr << endl;
    cout << "Value using pointer: " << *ptr << endl;

    return 0;
}
````

---

# 6. Null Pointer

A pointer that does not point to any valid memory location.

```cpp
int *ptr = nullptr;
```

Using `nullptr` is recommended over `NULL`.

---

# 7. Pointer Arithmetic

If a pointer points to an integer:

```cpp
int arr[3] = {10, 20, 30};
int *ptr = arr;

cout << *(ptr + 1);
```

Output:
20

Pointer moves according to data type size.

---

# 8. Dynamic Memory Allocation

Memory allocated during runtime.

---

## 8.1 Allocating Single Variable

```cpp
int *ptr = new int;
*ptr = 10;
```

---

## 8.2 Deallocating Memory

```cpp
delete ptr;
```

Important:
Always free dynamically allocated memory to avoid memory leaks.

---

# 9. Dynamic Array

```cpp
int n;
cin >> n;

int *arr = new int[n];

for (int i = 0; i < n; i++) {
    cin >> arr[i];
}

delete[] arr;
```

---

# 10. Dangling Pointer

Occurs when memory is deleted but pointer still holds the old address.

```cpp
delete ptr;
ptr = nullptr;
```

Setting to `nullptr` avoids accidental usage.

---

# 11. Pointer and Functions

Pass by reference using pointer:

```cpp
void modify(int *x) {
    *x = 50;
}

int main() {
    int a = 10;
    modify(&a);
    cout << a;   // Output: 50
}
```

---

# Summary

* Pointer stores address of a variable.
* `&` gives address.
* `*` dereferences pointer.
* `new` allocates memory.
* `delete` frees memory.
* `delete[]` frees dynamic arrays.
* Always avoid memory leaks.
* Set pointer to `nullptr` after delete.

```

---

Now we’re almost at OOP level.

Next:

📄 `08-structures-and-enum.md`

After that → OOP concepts 😌🔥
```
