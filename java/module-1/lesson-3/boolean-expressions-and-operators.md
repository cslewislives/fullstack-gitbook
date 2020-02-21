---
description: >-
  Expressions that always evaluate to either true or false. There are two types
  of boolean expressions Relational and Logical.
---

# Boolean Expressions & Operators

Boolean expressions were referred to in Lesson 2, but let us review the highlights.

## Boolean Expressions Defined

* Boolean expressions **always evaluate** to either true or false. 
* Boolean expressions **control the flow** of a program by testing conditions:
  * True or false?
  * Equal to?
  * Greater than or less than?

There are two types of boolean expressions: **Relational Operators** and **Logical**. 

## Relational Operators

Relational operators can also be referred to as **comparison** operators \(as seen on Day 2\). They compare two or more values and evaluate to either true or false. They are often used in combination with conditional statements and loops, both of which will be discussed later in this lesson. 

The primary Relational \(or Comparison\) Operators are:

* `>` greater than
* `<` less than
* `==` equal to \(Don't confuse this with the assignment operator `=`\) 
* `>=` greater than or equal to
* `<=` less than or equal to
* `!=` not equal to \(the ! is the negation operator\)

Paste this code into IntelliJ for a reminder of how relational operators resolve. 

```java
public class App {
    public static void main(String[] args){
        int num1 = 6; 
        int num2 = 3; 
        
        System.out.println("Greater than: " + (num1 > num2));
        System.out.println("Less than: " + (num1 < num2));
        System.out.println("Equal to: " + (num1 == num2));
        System.out.println("Not equal to: " + (num1 != num2));
    }
}
```

## Logical Operators

Logical operators are also referred to as **conditional** operators \(specifically conditional-AND and conditional-OR\) because they only evaluate the second operand if needed. The power of logical operators also manifests when used in conjunction with conditionals and loops. 

There are only two logical operators `&&`\(And\) and `||`\(Or\).

The resolution of logical operators is best illustrated by the following "truth table".

![](../../../.gitbook/assets/image%20%2819%29.png)

Upon examination of this table, you will notice that:

* For the `&&` \(And\) construct, if either of the values is false, the entire expression evaluates to false. 
* For the `||` \(Or\) construct, if either of the values is true, the entire expression evaluates to true. 

{% embed url="https://youtu.be/EJKYYHvHTXQ" %}



As mentioned, the power of the relational and logical operators lies in their incorporation with conditionals and loop constructs.  Let us begin to examine those constructs now. 

