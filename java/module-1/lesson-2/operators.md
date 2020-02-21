---
description: Operators are used to combine values to create a new value.
---

# Operators

{% embed url="https://www.youtube.com/watch?v=LPM3c-unrHU&feature=youtu.be" caption="" %}

## Arithmetic Operators 

Arithmetic operators are used to make a single numerical value from two or more numerical operands. That's a long-winded way to say you can add a few numbers to get a new number. 

There are a few types of operators that we're concerned with. Let's start with some that likely look familiar:

* `+` addition\*
* `-` subtraction
* `*` multiplication
* `/` division
* `%` modulus \(this gives the remainder from division\)
* `++` increment \(this increases a number by 1\)
* `--` decrement \(this decreases a number by 1\)

**\*The `+` operator can also be used to combine Strings.**

{% tabs %}
{% tab title="Code" %}
```java
public class App {
    public static void main(String args[]){
        int num1 = 6; 
        int num2 = 3; 
        
        System.out.println("Sum: " + (num1 + num2));
        System.out.println("Difference: " + (num1 - num2));
        System.out.println("Product: " + (num1 * num2));
        System.out.println("Quotient: " + (num1 / num2));
    }
}
```
{% endtab %}

{% tab title="Output" %}
```bash
Sum: 9
Difference: 3
Product: 18
Quotient: 2
```
{% endtab %}
{% endtabs %}

Increment and decrement operators come in two forms: pre-increment/pre-decrement and post-increment/post-decrement. 

**Pre-increment**, ****denoted by  `++` before the variable, increments the variable immediately.   
**Post-increment**, denoted by  `++` after the variable, increments the variable after the current line executes.  

{% tabs %}
{% tab title="Code" %}
```java
public class App {
    public static void main(String args[]){
        int num1 = 1; 
        
        System.out.println("pre-increment: " + ++num1);
        System.out.println("value after pre-increment: " + num1);
        System.out.println("post-increment: " + num1++);
        System.out.println("value after post-increment: " + num1);
        
    }
}
```
{% endtab %}

{% tab title="Output" %}
```bash
pre-increment: 2
value after pre-increment: 2
post-increment: 2
value after post-increment: 3
```
{% endtab %}
{% endtabs %}

## Comparison Operators

Comparison operators form an expression that compares two or more values and evaluates to a true or false. 

The primary Comparison Operators are:

* `>` greater than
* `<` less than
* `==` equal to \(Don't confuse this with the assignment operator `=`\) 
* `>=` greater than or equal to
* `<=` less than or equal to
* `!=` not equal to

As an example `3 > 4` evaluates to false because 3 is not greater than 4. 

In your IDE, paste in the following code and see what output you get:

```java
public class App {
    public static void main(String args[]){
        int num1 = 6; 
        int num2 = 3; 
        
        System.out.println("Greater than: " + num1 > num2);
        System.out.println("Less than: " + num1 < num2);
        System.out.println("Equal to: " + num1 == num2);
        System.out.println("Not equal to: " + num1 != num2);
    }
}
```

