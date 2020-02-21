---
description: Comments are notes left for yourself and your team.
---

# Comments



Comments are for your teammates, but they are also for you. You may write some code and then switch to working on something else, only to return to your original code months later. By then, you might have forgotten where your head was at when you wrote the code or what you were aiming to do. Comments come in very handy in those cases!

Comments are completely ignored by the compiler. They are only for other humans to read. 

There are 2 types of comments - block comments and single-line comments. 

**Block comments** start with `/*` and end with `*/`. They can span multiple lines \(thus the name\).

**Single-line comments** start with `//`. They can only span a single line. 

```java
public class App {
    /* This method indicates the differences between the
        pre and post-increment operators. These same principles
        hold true for decrement operations. 
    */
    public static void main(String args[]){
        int num1 = 1; 
        
        //Print the resulting values
        System.out.println("pre-increment: " + ++num1);
        System.out.println("value after pre-increment: " + num1);
        System.out.println("post-increment: " + num1++);
        System.out.println("value after post-increment: " + num1);
        
    }
}
```

{% hint style="danger" %}
While comments can be helpful, too many comments make code difficult to read. As a general rule, write comments in two cases: 

1. To  explain code when it is not immediately clear what the code does 
2. To describe the utility of a method so other developers don't have to read the full method to know what it does \(We'll learn more about methods later\). 
{% endhint %}

{% hint style="info" %}
Note that there are many theories on what good commenting looks like. Developers tend to be very opinionated on this topic. Check out [Putting Comments in Code](https://www.freecodecamp.org/news/code-comments-the-good-the-bad-and-the-ugly-be9cc65fbf83/) or  [Never Comment Your Code](https://medium.com/@devlob/never-comment-your-code-again-d230462b84f) if you want to learn more. As a rule, just follow the conventions on your team. 
{% endhint %}

