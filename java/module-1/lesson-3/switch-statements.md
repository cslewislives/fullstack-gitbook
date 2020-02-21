---
description: The switch statement is an alternative form of conditional evaluation.
---

# Switch Statements

As mentioned when examining the if-type constructs, you could need to write a lot of code if you are evaluating many different conditions. 

An example of this would be choosing an activity based on the month of the year.  If we wrote the code using the if/else if/else construct, it would look like the following:

```java
if (month == "January"){
    System.out.println("Let's go sledding!");
} else if (month == "February") {
    System.out.println("Let's go skiing!");
} else if (month == "March") {
    System.out.println("It's still cold. Let's go on vacation!");
}...else if (month =="November"){
    System.out.println("Let's go on a hay ride!");
}else {
    System.out.println("It is December. Happy Holidays!!");
} 
```

**Switch statements** present a more streamlined alternative to the above construct. 

The basic structure of a **switch** statement is found below. 

```java
switch (expression) {
    case value1:
 	   // execute code if expression == value1
 	   break;
    case value2:
 	   //execute code if expression == value2
 	   break;
    default:
 	   //execute code if no match found
 	   break;
}
```

{% hint style="warning" %}
The code block begins by evaluating the **expression**. 

In the case of the switch statement, the expression does not evaluate to either true or false \(no boolean expressions here!\), rather it evaluates to a **value**. 

The various possibilities for the **value** are detailed in each of the **case** statements.

If the **expression** evaluates to a specified **value**, the code associated with the value will be executed. This code will execute until it reaches the **break** statement. 

If the **expression** does not evaluate to any of the specified values, the **default** code block will execute. 
{% endhint %}

{% embed url="https://youtu.be/MUwPb5df2gI" %}

