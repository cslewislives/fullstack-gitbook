# Random Number - Activity

![Rolling Dice](../../../.gitbook/assets/image%20%28102%29.png)

One of the uses you will encounter for the Random utility is generating random numbers that will simulate rolling dice. 

{% tabs %}
{% tab title="RollingDice Instructions" %}
Write a class called `RollingDice` with a main method that simulates that roll of two dice. Print the output of those rolls to the screen. 

As always, attempt the code before reviewing the solution file.  
{% endtab %}

{% tab title="RollingDice Solution Code" %}
```java
package com.company;

import java.util.Random;

public class RollingDice {

    public static void main(String[] args) {

        Random randomGenerator = new Random();

        int diceOne = randomGenerator.nextInt(6) + 1;

        int diceTwo = randomGenerator.nextInt(6) + 1;

        System.out.println("Your first roll was: " + diceOne);
        System.out.println("Your second roll was: " + diceTwo);
    }
}
```
{% endtab %}
{% endtabs %}

