---
description: Using nested for-loops to access multi-dimensional arrays.
---

# Accessing Multi-Dimensional Arrays

Now that you understand how multi-dimensional arrays are structured and how to access specific positions within those arrays, it is time to examine how each of the element can be accessed within a program.

Similar to single dimension arrays, for loops will be utilized. But in the case of multi-dimensional arrays, the for loops will have to be **nested** one inside of the other. 

```java
    String[][] multiArr = { 
        {"a", "b", "c"}, {"1", "2", "3"},{"i", "ii", "iii"}
    };
```

In the prior section, it was demonstrated that every element in the above multi-dimensional array can be accessed by specifying its **index position**.  

* For example "3" was accessed by referencing multiArr\[1\]\[2\].

This syntax can be mirrored with the following code.

```java
public static void main(String[] args) {
    String[][] multiArr = {
            {"a", "b", "c"}, {"1", "2", "3"}, {"i", "ii", "iii"}
    };

    for (int i = 0; i < multiArr.length; i++) {
        for (int j = 0; j < multiArr[i].length; j++) {
            System.out.println( multiArr[i][j] );
        }
    }
}
```

* `int i` navigates through the top layer of the array.
* `int j` navigates through the elements that make up the top level array. 

Stepping through the cycle of the nested loops is as follows:

* The first loop begins and `int i` is initially set to 0. 
* Because of the structure of the code, the outer loop immediately looks to the inner loop and `int j` is set to 0. 
  * At this point the value of multiArr\[i\]\[j\] is multiArr\[0\]\[0\]. As determined previously, multiArr\[0\]\[0\] is "a". 
* Once '"a" is printed, the inner loops iterates again and `int j` becomes 1. multiArr\[0\]\[1\] is "b"\). 
* Once "b" is printed, the inner loops goes a third time producing multiArr\[0\]\[2\] or "c" and it is printed.
* On the next go, the inner loop meets it termination value where j \(now 3\) is no longer less than multiArr\[0\].length \(also 3\). 

{% hint style="warning" %}
Remember, **the length of the array is NOT the same as the last index value.** 

The length of the array is always one number greater because the we start counting the length from 1, but we start counting the index positions at 0. 
{% endhint %}

* Now the inner loop is finished and the outer loop is back in play. With the outer loop active, `int i` becomes 1 become of the outer iterator and the inner loop is back in play and the same cycle goes again...printing multiArr\[1\]\[0\], multiArr\[1\]\[1\] and multiArr\[1\]\[2\] until the inner loop terminates and the outerloop iterates through `int i` equal to 2. 

Copy the above code into IntelliJ to see how this process in action. 

```java
package com.company

public class App {

public static void main(String[] args) {
    String[][] multiArr = {
            {"a", "b", "c"},
            {"1", "2", "3"},
            {"i", "ii", "iii"}
    };

    for (int i = 0; i < multiArr.length; i++) {
        for (int j = 0; j < multiArr[i].length; j++) {
            System.out.println("The value of i is: " + i);
            System.out.println("The value of j is: " + j);
            System.out.println("The element is: " + multiArr[i][j] );
            System.out.println("=========");
        }
    }
 }
}
```

