# 📄 `09-object-oriented-programming.md`

````md
# Object-Oriented Programming in C++

This document covers classes, objects, access specifiers, constructors, destructors, and basic OOP principles.

---

# 1. What is OOP?

Object-Oriented Programming (OOP) is a programming paradigm based on objects.

An object contains:
- Data (variables)
- Functions (methods)

---

# 2. Class and Object

## 2.1 Class Syntax

```cpp
class ClassName {
private:
    // data members

public:
    // member functions
};
````

---

## 2.2 Example

```cpp
#include <iostream>
using namespace std;

class Student {
public:
    string name;
    int age;

    void display() {
        cout << name << " " << age << endl;
    }
};

int main() {
    Student s1;

    s1.name = "Logesh";
    s1.age = 20;

    s1.display();

    return 0;
}
```

---

# 3. Access Specifiers

| Specifier | Access Level                 |
| --------- | ---------------------------- |
| private   | Accessible only inside class |
| public    | Accessible outside class     |
| protected | Accessible in derived class  |

Default:

* `class` → private
* `struct` → public

---

# 4. Constructor

A constructor is a special function that initializes objects.

* Same name as class
* No return type

---

## 4.1 Default Constructor

```cpp
class Student {
public:
    Student() {
        cout << "Constructor Called";
    }
};
```

---

## 4.2 Parameterized Constructor

```cpp
class Student {
public:
    string name;
    int age;

    Student(string n, int a) {
        name = n;
        age = a;
    }
};
```

---

# 5. Destructor

* Automatically called when object is destroyed
* Same name as class with `~`
* No return type

```cpp
class Student {
public:
    ~Student() {
        cout << "Destructor Called";
    }
};
```

---

# 6. Encapsulation

Encapsulation means hiding data and allowing access through public methods.

Example:

```cpp
class Student {
private:
    int marks;

public:
    void setMarks(int m) {
        marks = m;
    }

    int getMarks() {
        return marks;
    }
};
```

---

# 7. Inheritance

Allows one class to inherit properties of another class.

```cpp
class Animal {
public:
    void sound() {
        cout << "Animal Sound";
    }
};

class Dog : public Animal {
};
```

---

# 8. Polymorphism

Same function behaving differently.

## 8.1 Function Overloading

```cpp
int add(int a, int b);
float add(float a, float b);
```

---

## 8.2 Method Overriding

```cpp
class Animal {
public:
    void sound() {
        cout << "Animal";
    }
};

class Dog : public Animal {
public:
    void sound() {
        cout << "Dog";
    }
};
```

---

# 9. Abstraction

Showing only essential features and hiding implementation details.

Achieved using:

* Classes
* Access specifiers

---

# Summary

* Class is blueprint.
* Object is instance of class.
* Constructor initializes object.
* Destructor cleans up.
* Encapsulation protects data.
* Inheritance allows code reuse.
* Polymorphism allows flexibility.
* Abstraction hides complexity.

```

---

Last file next:

📄 `10-exception-handling-and-advanced-concepts.md`

After that your C++ core foundation will be fully documented cleanly for GitHub 🔥
```
