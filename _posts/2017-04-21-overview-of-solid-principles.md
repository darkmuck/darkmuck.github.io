---
layout: post
title: Overview of SOLID Principles
published: true
---

### What is SOLID?
These 5 principles stand for the 5 basic principles of object-oriented programming and design. The intention is that these principles will make it more likely that we will create systems that are easier to maintain and extend.
The SOLID acronym stands for:
* S - Single Responsibility principle
* O - Open/Closed principle
* L - Liskov Substitution principle
* I - Interface segregation principle
* D - Dependency inversion principle

### Single Responsibility Principle
Every module or class should have responsibility over a single functionality. Any additional responsibilities should be delegated to other classes or modules. This principle makes the code much easier to understand and to reuse throughout the system.

### Open/Closed principle
Software objects (class, module, function, etc.) should be open for extension but closed for modification. This means that the objects' behavior should be allowed to be extended without modifying the original code.

### Liskov Substitution principle
If an object (class, module, etc.) is using a base then the reference to the base should be able to be replaced with a derived object without affecting the functionality of the program. As an example, if you are extending a class then you want the new derived classes to extend without replacing the functionality of the original base.

### Interface segregation principle
A client shouldn't be forced to implement an interface they don't need. Instead of a single 'fat interface' we should have many small interfaces based on groups of methods. We shouldn't be unnecessarily forced to provide implementations for methods that we will not use.

### Dependency inversion principle
High level objects should not depend on low level objects. An abstraction layer should exist between the layers. In doing this the high level objects will not depend upon the low level objects. Basically, it is better to depend upon an 'idea' rather than an 'implementation'. The abstraction layer will reduce coupling and allow for many implementations of an 'idea'.
