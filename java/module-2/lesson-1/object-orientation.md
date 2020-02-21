---
description: Examining the 5 basic properties of an object-oriented programming language
---

# Object Orientation

### Properties of an Object-Oriented Language

Alan Kay, the gentleman that coined the term "object-oriented programming" \(or OOP\) way back in 1966, summarized OOP in this way: 

* **Everything is an object**.
  * A Java object is a combination of data and procedures working on the available data.
  * Primitive types in Java are NOT objects. Rather each object contains a single value of the corresponding primitive type. 
  * All user-defined types are objects. 
* **A program is a collection of objects telling each other what to do by sending messages.**
  * In Java’s case, these messages are method calls and return values are what is being passed back and forth. 
* **Each object can be made up of other objects.**
  * This is called composition in Java.
  * For example -  A house \(object\) has \(or contains\) a stove \(object\), a refrigerator \(object\), a washing machine \(object\) and a television\(object\). 
* **Every object has a type**.
  * We have discussed that data types for primitives - boolean, byte, char, short, long, int, float and double - they contain pure, simple values of a kind. 
  * Similarly, classes and objects have type - for instance a student object could have a **S**tudent type. Much more on this later. 
* **All objects of a particular type can receive the same messages**.
  * In Java this means that they all have the same methods. This makes sense because all objects of the same type were created with the same code. 

### Defining an Object

Every object is said to have a state/properties, behaviors/methods and an identity. 

* **State/Properties**
  * Using a car as an example - Every car has color. That is a **property** of a car. 
  *  But each car can have a different color values. That makes color the **state** of the car. 
  * You can change the state of a car by painting it a different color, at which time the value of the color property would change. This changes the **state** of the car.
* **Behavior/Methods**
  * This speaks to the capabilities of the object. 
* **Identity**
  * Distinguishes each object from all of the other objects in the program.

{% embed url="https://youtu.be/OVanriY7Z\_w" %}

