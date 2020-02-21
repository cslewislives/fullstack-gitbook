---
description: >-
  While and Do/While loops enable a block of code to repeat until a condition
  evaluates to false.
---

# While and Do/While Loops

Continuing our story of the autonomous car at the stoplight, if you look up and the light is red, are you all done? Do you check again? How many times? 

We're going to talk about repeating ourselves with loops in this section.

## What are loops?

Loops are constructs that allow us to **repeat** a statement or code block based on some **condition**.

There are two main categories of loops:  **While** and **Do/While** loops and **For** loops

### While and Do/While loops

* While and Do/While loops repeat code until a certain condition is met.
  * Like the if and else/if constructs, this condition must evaluate to either true or false. The code will only execute if the condition evaluates to true. 
* We do **NOT** know ahead of time how many times the loop should repeat.
* Real-world examples:

  * Sitting at the stop light until it turns green.
  * Wash dishes until they are done. 
  * Ask for input until it is valid.

The code construct for a  **While** loop is as follows.

```java
while (condition) {
    // repeat while condition is true
}
```

* The condition is a boolean value or expression.
* The condition is checked and then the code block is run if the condition is true.
* After the code block is executed, the condition is checked again.
* If the condition is true, the code block is executed again; if not, we exit the loop and continue with the code following the closing curly brace of the while loop.

The code construct for a **Do/While** loop is as follows.

```java
do {
     // repeat while condition is true
} while (condition);

```

* The code block is executed.
* After the code block is executed, the condition is checked. If the condition is true, the do portion of the code block is executed again. This cycle repeats until the condition evaluates to false.

{% hint style="warning" %}
Use a **Do/While** loop if you **must** execute the code at least once. 
{% endhint %}

Drop the following code into IntelliJ to see how the While loop functions.

```java
package com.company;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner myScanner = new Scanner(System.in);

        System.out.println("Would you like to print some words to the screen? (y for yes)");
        String userInput = myScanner.nextLine();

        // enter the while loop if the user typed in 'y'
        while(userInput.equals("y")) {
            System.out.println("Type a word you want to print to the screen:");
            String word = myScanner.nextLine();
            System.out.println(word);

            System.out.println("Would you like to try again? (y for yes)");
            userInput = myScanner.nextLine();
        }

        System.out.println("OK - see you later!");
    }
}
```

{% hint style="warning" %}
Introducing **.equals**

From line 15 of the code above, notice the **.equals** used in the evaluation expression. 

The .equals\(\) method allows for the comparison of **strings**. If ANY character of the string is NOT matched, the expression evaluates to false. 

This is in contrast to == \(double equal\) which is used to compare numerical values. 
{% endhint %}

