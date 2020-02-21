---
description: 'Exploring if, if/else and if/else if/else conditional statements.'
---

# If-type Constructs

Before we begin to examine conditional statements, take a moment to ponder the following:

> What would go in to programming an autonomous car to decide whether or not to move forward from at stoplight?

Think about how you would evaluate the conditions that would trigger the cars movement.

* If the light was green, the car would move forward.
* If no pedestrians were present in the crosswalk, the car would move forward. 
* Can you think of any others?

**If-statements** are one of the two main types of conditionals. 

## If 

The first construct is the **if** statement. The basic code structure is as follows:

```java
if (condition) {
    // execute code if condition 
    // is true
}
```

The `condition` in the above statement is either a boolean value or a boolean expression. The if statements only allows for the evaluation of **one** condition. 

{% hint style="warning" %}
**If** the `condition` evaluates to **true** the code detailed inside the code block \({}\) **will** be executed. 

**If** the `condition` evaluates to **false,** **nothing** will be executed. 
{% endhint %}

Copy the following code into IntelliJ to see an example of how an if-statement works. 

```java
package com.company;

public class Main {

    public static void main(String[] args) {

        int age = 19;

        if (age > 18) {
            System.out.println("You can vote!");
        }
}
```

Change the **age to equal 17** and see how the output changes. 

## If/else

In contrast to the if statement, the if/else statement gives you two options for code execution.

First, the basic code structure is as follows:

```java
if (condition) {
    // execute code if condition is true
} else {
    // execute code if condition is false
}  
```

As with the if statement, the `condition` in the above statement is either a boolean value or a boolean expression. Again, the if/else statements allows for the evaluation of only one condition, but it now allows for the execution of two different code blocks. 

{% hint style="warning" %}
**If** the `condition` evaluates to **true** the code detailed inside the **if** section of code block \({}\) **will** be executed. 

**If** the `condition` evaluates to **false** the code block will execute the instructions in the **else** portion of the code. 
{% endhint %}

Copy the following code into IntelliJ to see an if/else statement at work. 

```java
package com.company;

public class Main {

    public static void main(String[] args) {

        int age = 19;

        if (age > 18) {
            System.out.println("You can vote!");
        } else {
            System.out.println("You are not old enough to vote yet!");
        }

    }
}
```

Again change the **age to 17**. Contrast the output for this if/else statement to that from the simple if-statement. 

## If/else if/else

This construct allows the programmer to string together **multiple conditions** for evaluation and execution. 

```java
if (condition1) {
    // execute code if condition1 is true
} else if (condition2) {
    // execute code if condition2 is true
  // and condition1 was false
} else {
    // execute code if all conditions above
  // were false
}
```

{% hint style="warning" %}


**If** `condition1` evaluates to **true** the code detailed inside the **if** section of code block \({}\) **will** be executed. 

**If** `condition2` evaluates to true the code detailed inside of the associated **else if** block \({}\) will be executed. 

**If** none of the stated conditions evaluates to true the code inside the **else** block will be executed. 
{% endhint %}

The if/else if/else construct is a logical coding choice if you only have two or three distinct conditions to evaluate, but what if you had twelve conditions? That would be a lot of code to write. An alternate solution is the **switch** statement.

