# Design Patterns
Software is always in a state of change. Each change can have a negative impact on a whole project, the essential thing is to prevent damage that can be done while implementing all new changes. 

Classes are building blocks of any java application. If these blocks are not strong, building (i.e. application)is going to face tough time in future, which essentially means that not so well-written code can lead to very difficult situations when  application scope goes up or faces certain design issues either in production or maintenance. On the other hand, set of well designed and written classes can speed up coding process by leaps and bounds, while reducing number of bugs in comparison. 

# SOLID 
SOLID is a collection of important programming practices that were developed by Robert C. Martin. One of the most popular sets of design principles in object-oriented software development. It’s a mnemonic acronym for the following five design principles:
S: Single Responsibility Principle
O: Open/Closed Principle
L: Liskov Substitution Principle
I: Interface Segregation Principle
D: Dependency Inversion

SOLID consists of below coding practices:
SRP - Single responsibility principle
OCP - Open/close principle
LSP - Liskov substitution principle
ISP - Interface segregation principle
DIP - Dependency inversion principle
SRP - Single responsibility principle
SRP - says that each method / class should be responsible for one specific activity. Inserting everything into one method does not meet the basic assumptions of objectivity, but also makes it difficult to read, repair or expand programs.

This principle is very noticeable when we write an application that begins to grow with time. It is enriched with new functionalities. Then we want to use already existing classes and their capabilities. However, it turns out, that the class that A should do is also do B, C and D, which is not desired by the currently created implementation. Then the problem arises because we can no longer use the given class. In this situation, you can avoid sticking to the SRP.

OCP - Open/close principle
The OCP principle says that the classes that we create are open to extensions and closed to modifications.

The application that we create must be ready for extensions, because the systems are changing very quickly these days. Thanks to the OCP principle, we are able to repeatedly use our classes for various tasks, which promotes reusability of the code, but also makes it easy to understand.

# LSP - Liskov substitution principle
Functions that use pointers or references to base classes must also be able to use class objects that inherit from the base classes without having a thorough knowledge of these objects.

# ISP - Interface segregation principle
ISP says: "Many dedicated interfaces are better than one overall".

The interface should give a specific shape to the class, and the methods that must be implemented within the class should be common to all implementation classes.

# DIP - Dependency inversion principle
The DIP principle is a part of S.O.L.I.D. principles which represents fifth letter D.

As a Java programmer, you’ve likely heard about code coupling and have been told to avoid tightly coupled code. Ignorance of writing “good code” is the main reason of tightly coupled code existing in applications. As an example, creating an object of a class using the new operator results in a class being tightly coupled to another class. Such coupling appears harmless and does not disrupt small programs. But, as you move into enterprise application development, tightly coupled code can lead to serious adverse consequences.

Usually abstraction means an abstract class or interface. Essentially, introducing a certain abstraction allows us to exchange individual elements of program with other ones more suitable for a specific task. We try not to enter into classes depending on its smaller parts. When one class knows explicitly about the design and implementation of another class, changes to one class raise the risk of breaking the other class. Such changes can have rippling effects across the application making the application fragile. To avoid such problems, you should write “good code” that is loosely coupled, and to support this you can turn to the Dependency Inversion Principle.

The principle states,
A. High-level modules should not depend on low-level modules. Both should depend on abstractions.
B. Abstractions should not depend on details. Details should depend on abstractions.

Conventional application architecture follows a top-down design approach where a high-level problem is broken into smaller parts. In other words, the high-level design is described in terms of these smaller parts. As a result, high-level modules that gets written directly depends on the smaller (low-level) modules.

What Dependency Inversion Principle says is that instead of a high-level module depending on a low-level module, both should depend on an abstraction. Let us look at it in the context of Java through this figure.

# Dependency Inversion Principle

Problem :
In this project, if we hardcode JavaEditor class into IDE class. Then the IDE is bound to only edit Java specific code. We don't want that. The IDE must be able to edit any language code.

Solution :
So, the solution is to make an abstraction of Editor as an interface and both IDE and JavaEditor or CppEditor depends on Editor interface. Now IDE is able to edit any code.

# YAGNI - You ain’t gonna need it
The principle says not to create functionality until it is actually needed. This is a good practice because we do not create redundancy in the application and we do not leave code that is not used in any way.

YAGNI on Wiki

# DRY - Don’t repeat yourself
Analysis of the written code and the desire to improve it are always key in software writing.

When writing several classes with similar properties, we may encounter similar problems. This is a sign that the code inside these classes is common and it may indicate that it should be separated into another class that will deal with repetitive tasks in one place. Thanks to this operation, both classes will use the same code, and thus, the probability of error will drop.

DRY on Wiki

# KISS - Keep It Simple, Stupid!
This rule is often mentioned when discussing architecture or details of building projects. Its essence is striving to maintain an elegant and transparent structure, without adding unnecessary elements.

KISS on Wiki

# SOC - Separation of Concern
The separation of issues consists in the division of the program into separate modules that overlap with as little functionality as possible. We call this kind of program modular. Each element of the system should have its separate and singular application. The purpose of SoC (Separation of Concern) is to create a system in which each part plays a significant role while maintaining the possibility of maximum adaptation to changes. SoC does not refer only to the system architecture, but to various issues, eg to divide the application into layers (presentation, business logic, access to data, database).

SOC on Wiki

# CQS - Command Query Separation
It is a rule that says that every method in the system should be classified into one of two groups:

Command - these are methods that change the state of the application and do not return anything.
Query - these are methods that return something, but do not change the state of the application.
CQS on Wiki
