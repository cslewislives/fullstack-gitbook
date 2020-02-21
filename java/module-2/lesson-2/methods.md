---
description: Adding behaviors to classes.
---

# Methods

We have already seen, created, and used methods. Now we are going to start learning more about methods and how they behave in objects.

Let's start off with a quick review of methods: 

* Methods are named blocks of code that we can call \(or invoke\) to do work for us.
* Methods are one good way to achieve code reuse; we write the method once but we call it over and over.
* Methods can have zero or more parameters. Parameters are values that we pass into the method. The method uses these values when doing its work.
  * Example: An add method takes in two numbers. The method adds those two numbers together to calculate the sum. The two numbers are the parameters. 
* A method may or may not return a value.
  * Example: That add method we mentioned before may return the sum of the two numbers passed in. But an alternate implementation of the add method may not return the sum; instead, it may just print the sum out to the console.

The methods that we write from now on will not automatically have the `static` keyword in front of them. The `static` keyword will only be used when appropriate. We'll learn more about the `static` keyword in the next article.

Add the methods below to your Lion class:

```java
public void roar() {
    System.out.println("ROAR");
}

public void pounce() {
    System.out.println("POUNCING");
}

public void nap() {
    System.out.println("ZzzZzzZzz");
}
```

We call methods on an object using dot notation:

```java
Lion jade = new Lion("King Jade", 22, 350);
jade.roar();
```

{% embed url="https://youtu.be/QkwhjbjdGpA" %}

