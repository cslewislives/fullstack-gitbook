---
description: >-
  Explains the need for the Java Collections framework and describes some types
  and methods.
---

# Java Collections



* So far, the most complex data structure we've seen is the array, which is quite limited.
* The collections framework gives us some nice tools for organizing and manipulating data and objects in our programs.
* We're going to learn about the collections framework in general and the List interface \(and ArrayList implementation\) specifically.
* We'll learn to use lists in a program to do more complex things.

 **Prompt: What are some things you wish you could do with an array? What are some of the limitations of arrays? What are some advantages?**

Some limitations of arrays include:

* Fixed length / doesn't grow or shrink
* Can't insert or remove items from the middle \(similar to fixed length\)
* Have to know ahead of time how big it needs to be

The collections framework helps us address these shortcomings. The collections framework makes it easier for us to manipulate and process groups \(or collections\) of items in a flexible fashion. It is a great library that gives us some powerful tools.

{% hint style="info" %}
The following short activity will help you familiarize yourself with the Javadoc for the collections framework.
{% endhint %}

{% tabs %}
{% tab title="Instructions" %}
* Google "Java 8 collections framework Javadoc"
* Javadoc is a tool that allows developers \(like us or like the engineers working at Oracle\) to document their objects and interfaces so other developers know how to use them. All of the classes and interfaces that come with the JDK have Javadoc.
* As stated in the Javadoc for the collections framework: the design goal was to have a fairly small API that allowed developers to process groups of related objects/data.
  *  **API** stands for **application programming interface**. Take a look at the base Collection interface and its methods. This is the base API for collections. In Java, an API generally consists of an interface or the methods on a class.
* Take a look at the Javadoc page and look for the following:
  * Advantages
  * Components
  * The collection interface and its descendants
    * Explore the Collection interface and read about the methods `add` , `clear` , `contains` , and `remove` . 
  * Look at some of the implementations, specifically for List and ArrayList because we'll be looking at them later in the lesson.
  * Design Goals
  * Remember Javadoc is your friend! It can help us understand how classes and interfaces are supposed to work and how we're supposed to use them.
{% endtab %}

{% tab title=" Javadoc Link " %}
[https://docs.oracle.com/javase/8/docs/technotes/guides/collections/index.html](https://docs.oracle.com/javase/8/docs/technotes/guides/collections/index.html)
{% endtab %}
{% endtabs %}

