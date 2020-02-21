---
description: How to create a new method.
---

# Method Definition

You've already seen methods. In fact, you've been working with them since Lesson 1. The main method is needed to run any application and we've included it in every project so far. The main methods primary job is to supply your project with a starting point when you run it. You can create new methods to do new jobs. 

Similar to a variable, we have to define a method before we can use it. We define a method by using a method declaration. The method declaration has several parts. We’ll start with the basics and build outward. The main pieces are: 

* The name of the method
* The body \(code block\) of the method
* Any parameters that the method takes \(more on this later\)
* The type of data returned by this method \(again, more on this later\)
* Parameters and return type

  * Explanation for now: Oftentimes, methods take parameters and return a value. Think of a simple method that adds two numbers together: it would take two numbers in as parameters and return the sum.

Let's walk through a basic method declaration: 

```java
public static void doSomething(int a,int b) {   
    // Code that does something 
}
```

`public` **-** public is an **ACCESS MODIFIER**. Your access modifier can be public, private, or protected. This controls which parts of your application have access to this method. Just use public for now; we'll talk about the others in Module 2. 

`static` - We’ll get into this in the next unit. It is not always required, but it is for the activities this week.

`void` - This is the **RETURN TYPE**. Methods are like a box - data can only be passed in through parameters and can only escape the curly braces through the return keyword. We'll take an in-depth look at the article labelled "Return Type". For now, just know that we have to declare what type of variable will come back out of the function. `void` means that nothing is returned where as `int` would indicate that an integer will be returned. 

`doSomething` - This is the **METHOD NAME**. The method name can be literally anything \(barring keywords and names that contain illegal characters, remember this list? - [https://www.geeksforgeeks.org/list-of-all-java-keywords/](https://www.geeksforgeeks.org/list-of-all-java-keywords/)\). It's like a variable name and it's how you'll use, or call, the method later. By convention, method names should begin with a verb. 

`int a, int b` - These are **PARAMETERS**. Parameters always appear inside parentheses and are how data get passed into the function. 

## Calling a Method

To call a method, you simply write its name, followed by parentheses, like `doSomething()`. Inside the parentheses, you can add values that will become the values of the parameters, like `doSomething(1, 3)`.  

Let's put this all together: 

```java
public static void main(String args[]) {
    int sum1 = add(1, 2);
    
    System.out.println(sum1);
}

public static int add(int a, int b) {
    return a + b;    
}
```

Copy the above code into IntelliJ. What prints? Do you understand why you get the output that you do? 

On line 7, we defined the method `add` and stated that it would take in two integer parameters and return an integer. 

On line 2, we are setting the `int` variable `sum1` equal to whatever is _returned_ from the method `add` when we pass it `1` and `2`. 

Inside the `add` method for this particular run, the variable`a` holds the value `1` and the variable`b` holds the value `2`. Therefore, on line 8, `a+b` evaluated to `3`. 

The returned value is `3` so `sum1` now equals `3`. 

{% hint style="danger" %}
You can name variables anything. `a` and `b` are just placeholder names for this example. Name them descriptively like you would any variable. 
{% endhint %}

{% hint style="danger" %}
While the method definition has multiple parts, the **METHOD SIGNATURE** is term used to refer to just the method name and parameter list. You'll need to know this later. 
{% endhint %}

