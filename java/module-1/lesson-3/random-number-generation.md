---
description: Generating random numbers using the Java utility.
---

# Random Number Generation

Generating random numbers in Java is coded very similarly to that of the Scanner. 

You import  `java.util.Random` at the beginning of the project \(line 3 in the code below\) and then instantiate the randomGenerator \(line 9\). 

Drop the above code into IntelliJ to confirm how the Random functions. 

```java
package com.company;

import java.util.Random;

public class Main {

    public static void main(String[] args) {

        Random randomGenerator = new Random();
        
       float randomFloat = randomGenerator.nextFloat();
       System.out.println(randomFloat);

       int randomInt = randomGenerator.nextInt(4);
       System.out.println(randomInt);
   
       
       int secondRandomInt = randomGenerator.nextInt(4) + 1;
       System.out.println(secondRandomInt);
    }
}
```

Examining the code on line 11, you will see that Random generates decimal numbers greater than or equal to  0 and less than 1. 

Because of how Random functions, the following line \(14\)`int randomInt=randomGenerator.nextInt(4);` will generate a number between 0 and 3 inclusive.  The is because int rounds down to the nearest whole integer. 

In order to capture the range 1 to 4, you must incorporate a 1 after the nextInt \(ie line 18\) 

{% embed url="https://youtu.be/6WjG2vHqr64" %}

