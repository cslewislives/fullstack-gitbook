# Arrays - Activity

![Initialize Animals Arrays](../../../.gitbook/assets/image%20%28103%29.png)

In the following activity, initialize two arrays of animals. One will be initialized using the per-element method, the other will be done using the initialized. You will need to print both arrays to the screen.  

{% tabs %}
{% tab title="Animals Arrays Instructions" %}
In this activity you are going to initialize two arrays and print both entire arrays and the individual elements to the screen.  Include both arrays in the same IntelliJ project. 

Create a project and java class called Animals. Use the com.company package. 

Fish Array - Using the **per-element method**, initialize an array called Fish that holds 3 different types of fish. Print the entire array and each individual element to the screen. 

Pets Array - Using the **initializer,** create an array called Pets that holds 5 different types of pets. Print the entire array and each individual element to the screen. 

As always, you can use the code in the prior examples and Google to assist you in this activity. 
{% endtab %}

{% tab title="Animals Arrays Solution Code" %}
```java
package com.company;

import java.util.Arrays;

public class Animals {

    public static void main(String[] args) {


        String[] Fish = new String[3];
        Fish[0] = "shark";
        Fish[1] = "whale";
        Fish[2] = "barracuda";

        System.out.println("Fish: " + Arrays.toString(Fish));
        System.out.println("Pets position 0: " + Fish[0]);
        System.out.println("Pets position 1: " + Fish[1]);
        System.out.println("Pets position 2: " + Fish[2]);



        System.out.println("==========================");



        String[] Pets = {"dog", "cat", "rabbit", "ferret", "parrot"};

        System.out.println("Pets: " + Arrays.toString(Pets));
        System.out.println("Pets position 0: " + Pets[0]);
        System.out.println("Pets position 1: " + Pets[1]);
        System.out.println("Pets position 2: " + Pets[2]);
        System.out.println("Pets position 3: " + Pets[3]);
        System.out.println("Pets position 3: " + Pets[4]);



    }
}
```
{% endtab %}

{% tab title="Animals Array Output" %}
![](../../../.gitbook/assets/image%20%2823%29.png)
{% endtab %}
{% endtabs %}

