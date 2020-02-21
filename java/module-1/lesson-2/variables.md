---
description: Variables store data that our program needs to access later.
---

# Variables

Variables are named bits of computer memory in which you can store a value. They are the core of any programming language. Thus far we've printed values, but we haven't stored them. But what would you do if you wanted to implement 2-factor authentication? You need a user to input a password, but you can't just print it. You need to store it and wait for the additional login code to be inputted before you begin the task of validating them.  

In short, you need to store values somewhere. 

How do we do this? With variables. Variables allow you to store values indefinitely. 

Creating, or declaring, a variable has 4 parts: 

```java
<type> <name> <assignment operator> <value>
```

What does this mean practically? You store the number 4 for late use in your program like: 

```java
int myNumber = 4; 
```

The assignment operator is always the equals sign `=`. Let's break the other three parts down. 

#### Type

There is a large number of types of variables but we'll start with just a few for now: 

* `int` - an integer number
* `double` - a decimal number \(`float` can also be used for this\)
* `String` - a series of characters like a word or sentence
* `boolean` - a true or false 

#### Name

This is just a name that you'll use to refer to the value being stored. It can be anything you want \(with a few exceptions that we'll cover in the next lesson\). The only important rules for now is that you can't have spaces in names and they should be camelCased, meaning that they begin with a lowercase letter and subsequent words begin with an uppercase letter. For example,  `myFavoriteBook` or `theLionKing`.

#### Value 

The value is the literal value that you want to store. 

For numbers like `int` or `double` the value would be something like `4` , `5.1`, or `3.7512`. 

For `String` type variables the value needs to be inside of quotation marks like `"Hello"`, `"c"` , or `"P4ssw0rd!"`. 

For `boolean` type variables the value can only be `true` or `false`. Booleans only have 2 states. 

{% embed url="https://youtu.be/lzoZgRAwE5Y" %}

