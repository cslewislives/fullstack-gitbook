---
description: >-
  The concept of creating a class that is cohesive with a narrowly-defined area
  of responsibility.
---

# Encapsulation

## Defining Encapsulation

The examination of 'public interface vs. private implementation' leads directly into the Java concept of **encapsulation**. Understand the concept of encapsulation is integral to developing well-constructed classes. 

The over-arching ideas of encapsulation as it relates to Java classes are that:

* Each class has a well-defined area of responsibility - the class should do one thing \(**single-responsibility principle**\), do it well and do it completely \(**cohesion**\)
* Each class has a public interface that clearly defines what a class does. 
* Encapsulation can be achieved by declaring all of the variables in a class as private and writing public methods in the class to get the value of the variables.
  * By declaring variables as private, the data is hidden from other classes and methods. This is known as **data-hiding**. 
  * The data for a class can only be altered only through the public getter and setter methods. 

## Encapsulation Concepts

Expanding on some of the encapsulation concepts covered above.

#### Single-responsibility principle 

The single-responsibility principle states that every class should have responsibility over a single part of the functionality provided by the program. 

All of the associated variables and methods should be should be narrowly aligned with the functionality of that class. 

#### Cohesion

Cohesion , in object oriented programming, refers to how a single class is designed.  Classes should be designed with a single, well-focused purpose. The more narrowly focused a class is, the easier it is to maintain and the more reusable it becomes across the program. 

#### Data Hiding 

The concept of data-hiding is closely related to encapsulation. It simply means that the internal state, or attributes,  of the class is hidden from the rest of the world. The internal state of the object is part of the **private** implementation. 

#### Delegation

Delegation in Java is defined as using an another class as an instance variable in the current class. And example of this is importing and utilizing the Scanner class in order to assist in capturing user input. Delegation is imperative in developing a functional program where the classes are built on the single-responsibility principle.

{% embed url="https://youtu.be/AwXnDkp02P4" %}

