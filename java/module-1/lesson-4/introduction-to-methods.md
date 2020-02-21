---
description: The antidote to code repetition and bloat.
---

# Introduction To Methods

In software engineering, Don't Repeat Yourself \(DRY\) is a principle of software development aimed at reducing repetition of software patterns. 

Methods are one of our greatest tools for avoiding repetition. Remember that a large part of writing good software is good code organization. Methods are an organizational tool that allow us to reuse code that we’ve already written and to break down large, complex tasks into simpler steps. 

An important note: Methods don’t really allow us to do anything we couldn’t do before—they just allow us to make our code better organized.

Methods are like mathematical functions. They take 0 or more inputs, perform some work on the inputs, and then produce some kind of result.

If you don't like math, you can think of methods like the order counter at the ice cream shop. The inputs are your order and your money; the output is some delicious ice cream. The ice cream you get depends on what you ordered and whether or not you have enough money.

Over the next few articles, we'll learn all about methods. For now check out the code below and see which tab looks cleaner to you. 

{% tabs %}
{% tab title="Without Methods" %}
```java
public class App {
    public static void main(String[] args){
        
        for (int i = 0; i < 5; i++){
            System.out.println("Hello");
        }
        
        for (int i = 0; i < 3; i++){
            System.out.println("three times!");
        }
        
        for (int i = 0; i < 10; i++){
            System.out.println("Weeeee!");
        }
        
        for (int i = 0; i < 2; i++){
            System.out.println("What are we doing?");
        }
        
        for (int i = 0; i < 2; i++){
            System.out.println("Again???");
        }
        
    }
}
```
{% endtab %}

{% tab title="With Methods" %}
```java
public class App {
    public static void main(String[] args){
    
        printLoop(5, "Hello");
        printLoop(3, "three times!");
        printLoop(10, "Weeeee!");
        printLoop(2, "What are we doing?");
        printLoop(2, "Again???");
        
    }
    
    public static void printLoop(int num, String printString){
        for (int i = 0; i < num; i++){
            System.out.println(printString);
        }
    } 
}
```
{% endtab %}
{% endtabs %}

Play with the above code. Paste it in IntelliJ and run it. Alter it and see what you can intuit. 

