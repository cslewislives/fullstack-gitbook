---
description: >-
  Debugging is the process of identifying and removing errors from computer
  hardware or software.
---

# Debugging

The debugger is a powerful tool that everyone should use. Breakpoints allow us to stop program execution and look at the state of the program. We can step through a program line by line. This allow us to see what the program is actually doing vs. what we think it is doing. 

{% embed url="https://youtu.be/agcIu9QLqjg" %}

Use the code below, to follow along with the instructional video. 

```java
public class DebuggingPractice {

    public static void main(String[] args) {
        int a = 1;
        int b = 45;
        int c = 352;
        int sum = 0;
        String message = "This is a test message!";
        String message2 = "This is a second message!!!";

        System.out.println("Value of a is: " + a);
        System.out.println("Value of b is " + b);
        System.out.println("Value of c is: " + c);

        sum = a + b + c;

        System.out.println("Sum = " + sum);
    }
}
```

