# 📄 `06-functions-and-scope.md`

````md
# Functions and Scope in C++

This document covers function declaration, definition, parameters, return types, and variable scope.

---

# 1. What is a Function?

A function is a block of code that performs a specific task.

It improves:
- Code reusability
- Readability
- Modularity

---

# 2. Function Syntax

```cpp
return_type function_name(parameters) {
    // function body
}
````

---

# 3. Example: Simple Function

```cpp
#include <iostream>
using namespace std;

void greet() {
    cout << "Hello, World!";
}

int main() {
    greet();
    return 0;
}
```

---

# 4. Function with Parameters

```cpp
void greet(string name) {
    cout << "Hello " << name;
}

int main() {
    greet("Logesh");
}
```

---

# 5. Function with Return Value

```cpp
int add(int a, int b) {
    return a + b;
}

int main() {
    int result = add(5, 3);
    cout << result;
}
```

---

# 6. Function Declaration (Prototype)

A function can be declared before `main()` and defined later.

```cpp
int add(int, int);   // declaration

int main() {
    cout << add(5, 3);
}

int add(int a, int b) {
    return a + b;
}
```

---

# 7. Pass by Value

A copy of the variable is passed.

```cpp
void modify(int x) {
    x = 100;
}

int main() {
    int a = 10;
    modify(a);
    cout << a;   // Output: 10
}
```

Original value does not change.

---

# 8. Pass by Reference

Reference is passed using `&`.

```cpp
void modify(int &x) {
    x = 100;
}

int main() {
    int a = 10;
    modify(a);
    cout << a;   // Output: 100
}
```

Original value changes.

---

# 9. Default Parameters

```cpp
void greet(string name = "User") {
    cout << "Hello " << name;
}

int main() {
    greet();
}
```

---

# 10. Recursion

A function calling itself.

Example: Factorial

```cpp
int factorial(int n) {
    if (n == 0)
        return 1;
    return n * factorial(n - 1);
}
```

---

# 11. Variable Scope

## 11.1 Local Variable

Declared inside a function.

Accessible only within that function.

```cpp
void test() {
    int a = 10;   // local
}
```

---

## 11.2 Global Variable

Declared outside all functions.

Accessible throughout the program.

```cpp
int a = 10;   // global

void test() {
    cout << a;
}
```

---

# 12. Function Overloading

Multiple functions with same name but different parameters.

```cpp
int add(int a, int b) {
    return a + b;
}

float add(float a, float b) {
    return a + b;
}
```

---

# Summary

* Functions improve modularity.
* Parameters allow data input.
* Return type sends output.
* Pass by value → copy.
* Pass by reference → original modified.
* Scope determines variable visibility.
* Recursion allows self-calling functions.
* Overloading allows same function name with different parameters.

```

---

Next:

📄 `07-pointers-and-dynamic-memory.md`

Now we’re entering serious C++ territory 😌🔥
```
