---
description: A quick look at the Java 8 Javadoc for the List interface.
---

# List and ArrayList Javadoc

{% tabs %}
{% tab title="Instructions" %}
Navigate through the Java 8 Javadoc for the List interface. Use the Javadoc link on the second tab and the directions below: 

* List is an interface.
* List is a generic \(or parameterized\) interface that is marked by the angle brackets and the placeholder type "E".
* The List interface extends the Collection interface, which in turn extends the Iterable interface.
* We're seeing interfaces and inheritance in action here. Frameworks and libraries like the collections framework are places where inheritance is used quite a bit. We won't be writing frameworks and libraries, so we won't use inheritance very much. We'll use interfaces a lot, though. **Right tool for the right job!**
* Take a look at the method list and look at how much more capable lists are compared to arrays.
* One of the implementations of the List interface is the ArrayList. We'll be using ArrayLists a lot.
{% endtab %}

{% tab title="Javadoc Link" %}
[https://docs.oracle.com/javase/8/docs/api/java/util/List.html](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)
{% endtab %}
{% endtabs %}

> **Aside: Wrapper Classes**  
> Collections hold objects, but what if you want a collection of ints or booleans? We learned early on that Java primitive types are not objects, so what to do? Wrapper classes solve this problem. Wrapper classes encapsulate Java primitives so they can be used with generic types. We'll explore the ins and outs of using wrapper classes and converting back and forth between primitives and wrapper classes in the following code examples.

