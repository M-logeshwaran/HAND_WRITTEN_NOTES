📄 10_object_oriented_programming.md

# Object Oriented Programming in Python

This document covers classes, objects, constructors, instance variables, class variables, methods, inheritance, polymorphism, encapsulation, and method resolution.

---

# 1. Introduction to OOP

Object Oriented Programming (OOP) is a programming paradigm based on objects.

Main concepts:

- Class
- Object
- Encapsulation
- Inheritance
- Polymorphism
- Abstraction

---

# 2. Class and Object

A class is a blueprint for creating objects.

Syntax:

```python
class ClassName:
    pass

Example:

class Student:
    name = ""

Creating object:

s1 = Student()


---

3. Constructor (init)

A constructor initializes object data.

class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

s1 = Student("Logesh", 20)

self refers to current object.

Constructor runs automatically when object is created.



---

4. Instance Variables

Variables defined using self.

Each object has its own copy.

class Student:
    def __init__(self, name):
        self.name = name


---

5. Class Variables

Variables shared by all objects.

class Student:
    school = "ABC School"

    def __init__(self, name):
        self.name = name

Access:

print(Student.school)


---

6. Types of Methods


---

6.1 Instance Method

Works with instance variables.

class Student:
    def display(self):
        print(self.name)


---

6.2 Class Method

Works with class variables.

class Student:
    school = "ABC"

    @classmethod
    def get_school(cls):
        return cls.school


---

6.3 Static Method

Does not use instance or class variables.

class Math:
    @staticmethod
    def add(a, b):
        return a + b


---

7. Inheritance

Inheritance allows one class to acquire properties of another class.


---

7.1 Single Inheritance

class Parent:
    def show(self):
        print("Parent class")

class Child(Parent):
    pass


---

7.2 Multilevel Inheritance

class Grandparent:
    pass

class Parent(Grandparent):
    pass

class Child(Parent):
    pass


---

7.3 Multiple Inheritance

class Father:
    pass

class Mother:
    pass

class Child(Father, Mother):
    pass


---

7.4 Hierarchical Inheritance

class Parent:
    pass

class Child1(Parent):
    pass

class Child2(Parent):
    pass


---

8. super() Function

Used to call parent class constructor or methods.

class Parent:
    def __init__(self):
        print("Parent Constructor")

class Child(Parent):
    def __init__(self):
        super().__init__()
        print("Child Constructor")


---

9. Polymorphism

Same method name behaving differently.


---

9.1 Method Overriding

class Parent:
    def show(self):
        print("Parent method")

class Child(Parent):
    def show(self):
        print("Child method")


---

10. Encapsulation

Encapsulation restricts direct access to variables.


---

10.1 Public Variable

self.name


---

10.2 Protected Variable

self._age


---

10.3 Private Variable

self.__salary

Private variables use name mangling:

object._ClassName__salary


---

11. Abstraction

Abstraction hides internal implementation.

Using abstract base class:

from abc import ABC, abstractmethod

class Shape(ABC):

    @abstractmethod
    def area(self):
        pass

Child class must implement abstract method.


---

12. Method Resolution Order (MRO)

Defines order in which base classes are searched.

print(Child.__mro__)


---

Summary

Class is a blueprint.

Object is instance of class.

Constructor initializes data.

Instance variables belong to object.

Class variables are shared.

Inheritance allows code reuse.

Polymorphism enables method overriding.

Encapsulation restricts access.

Abstraction hides implementation details.


---

Python documentation structure complete.  

If you want improvements, refinements, or add advanced concepts, tell me.
