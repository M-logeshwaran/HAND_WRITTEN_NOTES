# 📄 `09-object-oriented-programming.md` (Full Detailed Version)

````md
# Object-Oriented Programming in C++

Object-Oriented Programming (OOP) organizes software design around objects.
An object contains data and functions that operate on that data.

Core OOP principles:
1. Encapsulation
2. Abstraction
3. Inheritance
4. Polymorphism

---

# 1. Class and Object

## 1.1 Class

A class is a blueprint for creating objects.

Syntax:

```cpp
class ClassName {
private:
    // data members

public:
    // member functions
};
````

---

## 1.2 Object

An object is an instance of a class.

```cpp
ClassName obj;
```

---

# 2. Access Specifiers

| Specifier | Description                               |
| --------- | ----------------------------------------- |
| private   | Accessible only inside class              |
| public    | Accessible everywhere                     |
| protected | Accessible inside class and derived class |

Default:

* class → private
* struct → public

---

# 3. Constructors

A constructor initializes the object.

Properties:

* Same name as class
* No return type
* Called automatically

---

## 3.1 Default Constructor

```cpp
class Student {
public:
    Student() {
        cout << "Default Constructor";
    }
};
```

---

## 3.2 Parameterized Constructor

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

## 3.3 Constructor Overloading

```cpp
class Test {
public:
    Test() {}
    Test(int a) {}
};
```

---

# 4. Destructor

Used to release resources.

* Begins with ~
* Automatically called when object goes out of scope

```cpp
class Test {
public:
    ~Test() {
        cout << "Destructor Called";
    }
};
```

---

# 5. Encapsulation

Encapsulation means binding data and methods together and restricting direct access.

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

This protects internal data.

---

# 6. Abstraction

Abstraction hides implementation details and shows only essential features.

In C++, abstraction is achieved using:

* Classes
* Access specifiers
* Pure virtual functions

---

## 6.1 Abstract Class Example

An abstract class contains at least one pure virtual function.

```cpp
class Shape {
public:
    virtual void draw() = 0;  // pure virtual function
};
```

Now any derived class must implement `draw()`.

```cpp
class Circle : public Shape {
public:
    void draw() {
        cout << "Drawing Circle";
    }
};
```

Abstract classes cannot be instantiated:

```cpp
// Shape s;  ❌ Not allowed
```

---

# 7. Inheritance

Inheritance allows one class to acquire properties of another class.

Syntax:

```cpp
class Derived : accessSpecifier Base {
};
```

---

# 7.1 Types of Inheritance

---

## 1. Single Inheritance

One derived class inherits from one base class.

```cpp
class Animal {
public:
    void eat() {
        cout << "Eating";
    }
};

class Dog : public Animal {
};
```

---

## 2. Multiple Inheritance

One class inherits from multiple base classes.

```cpp
class A {
public:
    void displayA() {}
};

class B {
public:
    void displayB() {}
};

class C : public A, public B {
};
```

---

## 3. Multilevel Inheritance

Derived class becomes base for another class.

```cpp
class A {
public:
    void displayA() {}
};

class B : public A {
};

class C : public B {
};
```

---

## 4. Hierarchical Inheritance

Multiple classes inherit from one base class.

```cpp
class Animal {
};

class Dog : public Animal {
};

class Cat : public Animal {
};
```

---

## 5. Hybrid Inheritance

Combination of multiple inheritance types.

Example:
Multilevel + Multiple.

---

# 8. Polymorphism

Polymorphism means "many forms".

Two types:

1. Compile-time (Static)
2. Run-time (Dynamic)

---

## 8.1 Compile-Time Polymorphism

### Function Overloading

```cpp
int add(int a, int b);
float add(float a, float b);
```

### Operator Overloading (Basic Idea)

```cpp
int a = 5;
int b = 3;
int c = a + b;
```

`+` works differently for different data types.

---

## 8.2 Run-Time Polymorphism

Achieved using:

* Inheritance
* Virtual functions

---

### Virtual Function Example

```cpp
class Animal {
public:
    virtual void sound() {
        cout << "Animal Sound";
    }
};

class Dog : public Animal {
public:
    void sound() {
        cout << "Dog Sound";
    }
};

int main() {
    Animal* ptr;
    Dog d;
    ptr = &d;

    ptr->sound();
}
```

Without `virtual`, base class function would execute.

---

# 9. Important Concepts

* Constructor initializes object.
* Destructor cleans object.
* Encapsulation protects data.
* Abstraction hides implementation.
* Inheritance allows reuse.
* Polymorphism allows flexibility.
* Virtual function enables runtime polymorphism.
* Abstract class enforces method implementation.

```

---

Now your OOP section is:

✔ Complete  
✔ Interview-ready  
✔ Structured  
✔ Professional GitHub level  

---

Next we still need:

📄 `10-exception-handling-and-advanced-concepts.md`

After that → your C++ foundation documentation is solid.

Ready? 😌🔥
```
