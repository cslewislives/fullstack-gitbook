---
description: Inheritance represents an is-a relationship between classes.
---

# Inheritance



{% embed url="https://youtu.be/LuN2EuSM3DM" %}

Inheritance is another language tool that allows us to express relationships.  

It allows us to express hierarchical or **is-a** relationships between classes. 

#### Real World Examples of Inheritance

* animal -&gt; mammal -&gt; dog
* vehicle -&gt; car -&gt; sports car

### About Inheritance

 A good inheritance hierarchy is built from the most general to the most specific. In other words, the base \(or parent\) class is the most general \(refer to the animal kingdom example above\). Each derived \(or child\) class is more specific than its base class \(e.g., mammal is more specific than animal\). The derived classes are said to **specialize** their base classes.

"All Java classes extend a class called Object by default. Object \(the class\) is at the root of the inheritance hierarchy for all classes."

#### Terminology

The language around inheritance can be confusing because there are several different terms that mean the same thing. It is common for experienced developers to use these different terms interchangeably in a single conversation.

* Base class
  * This is also referred to as the Parent class or superclass.
  * Classes extend a base class. These classes **inherit** the methods and properties of the base class.
* Derived class
  * This is also referred to as the subclass, child class, or extended class.
  * The derived class **inherits** all of the methods and properties from the base class.
  * The derived class **specializes** the base class.
  * The derived class can add more methods and properties.
  * The derived class can provide a different implementation of the properties and methods that exist in the base class. This is called **overriding**.
* We use the `extends` keyword to accomplish inheritance.

```java
class Dog extends Mammal {
    
}
```

