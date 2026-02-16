# 📄 `10-exception-handling-and-advanced-concepts.md`

````md
# Exception Handling and Advanced Concepts in C++

This document covers exception handling, file handling basics, namespaces, and other important advanced concepts.

---

# 1. Exception Handling in C++

Exception handling is used to handle runtime errors gracefully.

C++ uses:
- try
- throw
- catch

---

## 1.1 Basic Syntax

```cpp
try {
    // code that may cause exception
}
catch (exceptionType e) {
    // handling code
}
````

---

## 1.2 Example

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10;
    int b = 0;

    try {
        if (b == 0)
            throw "Division by zero error";

        cout << a / b;
    }
    catch (const char* msg) {
        cout << msg;
    }

    return 0;
}
```

---

## 1.3 Multiple Catch Blocks

```cpp
try {
    int x = 5;
    if (x == 5)
        throw x;
}
catch (int num) {
    cout << "Integer Exception: " << num;
}
catch (...) {
    cout << "Unknown Exception";
}
```

`catch(...)` handles any type of exception.

---

# 2. Standard Exception Example

Using standard library:

```cpp
#include <stdexcept>

try {
    throw runtime_error("Runtime error occurred");
}
catch (exception &e) {
    cout << e.what();
}
```

---

# 3. File Handling in C++

Requires:

```cpp
#include <fstream>
```

---

## 3.1 Writing to a File

```cpp
#include <fstream>

int main() {
    ofstream file("data.txt");
    file << "Hello World";
    file.close();
}
```

---

## 3.2 Reading from a File

```cpp
#include <fstream>
#include <iostream>
using namespace std;

int main() {
    ifstream file("data.txt");
    string text;

    while (getline(file, text)) {
        cout << text << endl;
    }

    file.close();
}
```

---

# 4. Namespaces

Namespace helps avoid name conflicts.

```cpp
namespace MySpace {
    int value = 10;
}

int main() {
    cout << MySpace::value;
}
```

---

# 5. Inline Function

Inline functions suggest compiler to replace function call with function code.

```cpp
inline int square(int x) {
    return x * x;
}
```

---

# 6. Const Keyword

## 6.1 Constant Variable

```cpp
const int x = 10;
```

Value cannot be modified.

---

## 6.2 Constant Parameter

```cpp
void display(const int x) {
    cout << x;
}
```

Prevents modification inside function.

---

# 7. Static Keyword

## 7.1 Static Local Variable

Retains value between function calls.

```cpp
void count() {
    static int x = 0;
    x++;
    cout << x;
}
```

---

## 7.2 Static Class Member

```cpp
class Test {
public:
    static int count;
};

int Test::count = 0;
```

---

# 8. Friend Function

Allows external function to access private members.

```cpp
class Test {
private:
    int x = 10;

    friend void show(Test t);
};

void show(Test t) {
    cout << t.x;
}
```

---

# 9. Important Notes

* Exceptions prevent program crash.
* Always handle critical runtime errors.
* Use `std::exception` for standard handling.
* File streams: `ifstream`, `ofstream`.
* Namespace prevents naming conflict.
* `static` preserves value.
* `const` ensures safety.

```
