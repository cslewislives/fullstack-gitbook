---
description: A brief explanation of generics.
---

# Generics

> "Generics allow you to specify the type of objects that a collection can contain."

* All of the data structures in in the collections framework and in the maps family \(next lesson\) hold references to objects. For example, you could have a Set of Student objects or a List of Address objects.
* We need a way to specify the type of objects a particular instance of a collection can hold.
* That mechanism is called a "generic class or interface," commonly referred to as a "generic."
* Generics have a slightly different declaration syntax: not only do we have to specify the type of the collection \(i.e., List, Set, etc.\) but we also have to specify the type of object that the collection can hold. 

#### Generics Examples

```java
List addressList<Address>;

List cityList<City>;
```

* The declaration pattern for generics is basically the same as for other types: `data-type variable-name` 
* We are simply adding the angle brackets after the variable name to specify the type of object that can be held in the collection \(List, in this case\).
* The first example List holds `Address` objects, while the second List holds `City` objects.
* We will see this in action in the next section.

{% embed url="https://youtu.be/JBWAy0xokV8" %}

