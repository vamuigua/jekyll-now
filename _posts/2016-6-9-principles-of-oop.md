---
layout: post
title:Principles of Object Oriented Programming
---
**The Four major principles of Object-Oriented Programming**<br/>
**1. Encapsulation:**
Encapsulation means that the internal representation of an object is generally hidden from view outside of the object’s definition;only the object’s own methods can directly inspect or manipulate its fields.
(Encapsulation is the hiding of data implementation by restricting access to accessors and mutators.)

An **accessor** is a method that is used to ask an object about itself.These are usually in the form of properties, which have a *get* method, which is an accessor method but the accessor methods are not restricted to properties & can be any public method that gives information about the state of the object.

A **mutator** is public method that is used to modify the state of an object, while hiding the implementation of exactly how the data gets modified. It’s the *set* method that lets the caller modify the member data behind the scenes.

All this can be summed up as-Hiding the internals of an object to protect its integrity by preventing users from setting the internal data of the component into an invalid or inconsistent state....Encapsulation.
**Benefit of encapsulation**-It can reduce system complexity.

**2. Abstraction**
Data Obstraction is the development of classes, objects, types in terms of their interfaces and functionality, instead of their implementation details.
*“An abstraction denotes the essential characteristics of an object that distinguish it from all other kinds of object and thus provide crisply defined conceptual boundaries, relative to the perspective of the viewer.” — G. Booch*(His defination)

In short, data abstraction is nothing more than the implementation of an object that contains the same essential properties and actions we can find in the original object we are representing.

**3. Inheritance**
Inheritance is a way to reuse code of existing objects, or to establish a subtype from an existing object, or both, depending upon programming language support.

In classical inheritance where objects are defined by classes, classes can inherit attributes and behavior from pre-existing classes called base classes, superclasses, parent classes or ancestor classes.The resulting classes are known as derived classes, subclasses or child classes. The relationships of classes through inheritance gives rise to a hierarchy. 

**Subclasses and Superclasses**
A *subclass* is a modular, derivative class that inherits one or more properties from another class (called the **superclass**). The properties commonly include class data variables, properties, and methods or functions. The superclass establishes a common interface and foundational functionality, which specialized subclasses can inherit, modify, and supplement. The software inherited by a subclass is considered reused in the subclass.
In some cases, a subclass may customize or redefine a method inherited from the superclass. A superclass method which can be redefined in this way is called a **virtual method**.

**4. Polymorphism**
Polymorphism means *one name, many forms*. It manifests itself by having multiple methods all with the same name, but
slighty different functionality.

The two basic types of polymorphism are:**Overriding** & **Overloading**

**1.Overriding**-also called *run-time polymorphism*;the compiler determines which method will be executed, and this decision is made when the code gets compiled.is a type of function which occurs in a class which inherits from another class. An override function "replaces" a function inherited from the base class, but does so in such a way that it is called even when an instance of its class is pretending to be a different type through polymorphism.

**2.Overloading**-also *compile-time polymorphism*;s the action of defining multiple methods with the same name, but with different parameters. It is unrelated to either overriding or polymorphism.
