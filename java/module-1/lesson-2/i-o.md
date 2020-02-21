---
description: >-
  Input and output are the way we create interactive programs. We've seen how to
  print to the console but we haven't seen how to take user input.
---

# I/O

There are several ways to get console input from the user. We are going to use something called the Scanner. 

{% embed url="https://youtu.be/M0brf3l57JA" %}

Below is some sample code to use as a reference when you need to get console Input: 

```java
import java.util.Scanner;

public class HelloAndAdd {
  public static void main(String[] args) {
    Scanner scan = new Scanner(System.in);

    System.out.println("What is your name?");
    String name = scan.nextLine();

    System.out.println("Hello, " + name);

    System.out.println("Please enter a number.");
    int num1 = Integer.parseInt(scan.nextLine());

    System.out.println("Please enter another number.");
    int num2 = Integer.parseInt(scan.nextLine());

    int sum = num1 + num2;
    System.out.println("The sum of your numbers is " + sum);
  }
}
```

