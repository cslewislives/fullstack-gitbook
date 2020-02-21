---
description: 'Interfaces allow us to express loosely coupled, contract-like relationships.'
---

# Introduction to Interfaces

Interfaces are a tool to help us organize our code and express relationships between objects.

So far, we have looked at individual classes/objects, but we do not have a way to capture relationships in a reusable way. Interfaces allow us to express loosely coupled, contract-like relationships. An interface advertises to the world that an implementing class has a particular set of capabilities. If two classes say they fulfill the contract expressed in a particular interface, you can count on the two classes to act the same with respect to the capabilities defined in the interface \(they may have other, completely unrelated capabilities as well\).

#### Real-World Examples of Interfaces

* Super charging stations: Tesla is one brand, but as long as your charger meets the specs and has the right kind of connectors \(i.e., interface\), your charger is interoperable with any other \(i.e., any vehicle that needs a supercharger can recharge at your station\).
* Credit card terminals: Traditional vs. Square—different companies make the hardware, but they all adhere to a set of specifications.
* After-market/third-party products:
  * Video game controllers
  * Car stereos
  * Motorcycle and car parts

#### What is an Interface?

* We talked earlier about public interface / private implementation. We mentioned at that time that the word interface has a special \(but related\) meaning in Java - here is it!
* An **interface** is a contract.
  * It defines a set of methods that must be implemented by any class that says it lives up to the contract \(we call that implementing the interface\).
  * An interface defines the methods that must be implemented but does not provide an implementation \(except in some special cases\).
  * Interfaces help us define, in a reusable, portable way, the "public interface" of a class.
* Interfaces are good at expressing relationships based on living up to a contract - these relationships are loosely coupled and say nothing about how the functionality behind the contract is fulfilled.
* Interfaces are a good way to create a specification that allows different components to "plug into" a system.

{% embed url="https://youtu.be/p4OK8XveCIY" %}

