---
description: Understand how to declare and initialize an array.
---

# Declaring & Initializing an Array

## Declaring an Array

The difference between arrays and the previous variable that we have examined is that arrays are made up of **more than one element**.  

Arrays must be declared and initialized just like the variables that we’ve already seen, but arrays  require a special syntax. 

```java
String[] cars;
```

* Arrays **require square brackets** after the specified data type. ie \(String \[ \]\).
* The name of the data type is declared as with our previously seen variables. 

```java
    int[] nums = new int[4];
```

* In this example we are declaring an array of ints. This first half of the equation declares the array \(ie **int \[ \]**\) and the variable name \(ie **nums**\)
* The second half of the equation declares that we are reserving space for 4 ints in the nums array. 
* The keyword `new` tells the computer to reserve space in memory for the elements in this array.  Additional information about the **new** keyword will be forthcoming. 

Now that we have declared the **nums** array, it is time to initialize the elements in the array. 

## Initializing an Array

One an array has been declared, it must be initialized. In other works, the elements that comprise the array must be added. 

There are two ways to initialize an array: on a per-element basis, or using an initializer. 

### Initializing Per-element

Declare the array with the number of elements you want to include. 

Once the array has been declared, reference the array name, the position and then set it equal to the value you want it to hold. 

{% hint style="warning" %}
If you are initializing an array on a per-element basis is that **indexing of an array starts at zero**. 
{% endhint %}

```java
        int[] arr1 = new int[4];
        arr1[0] = 10;
        arr1[1] = 20;
        arr1[2] = 30;
        arr1[3] = 40;
```

Drop the following code into IntelliJ to see an example of initializing an array on a per-element basis. 

Note that we are importing `java.util.Arrays` \(line 3\) and referencing into with the `.toString()` method \(line 15\) when you want to print the entire array. This is not necessary when printing out each element individually. 

```java
package com.company;

import java.util.Arrays;

public class App {

    public static void main(String[] args) {

        int[] arr1 = new int[4];
        arr1[0] = 10;
        arr1[1] = 20;
        arr1[2] = 30;
        arr1[3] = 40;

        System.out.println("Array 1: " + Arrays.toString(arr1));
        System.out.println("Array 1 position 0: " + arr1[0]);
        System.out.println("Array 1 position 1: " + arr1[1]);
        System.out.println("Array 1 position 2: " + arr1[2]);
        System.out.println("Array 1 position 3: " + arr1[3]);

    }
}
```

### Using the Initializer

When using the initializer to declare an array, you effectively combine the steps from above. 

```java
int[] arr2 = {10, 20, 30, 40};
```

Drop the following code into IntelliJ to see how the initializer works. 

```java
package com.company;

import java.util.Arrays;

public class App {

    public static void main(String[] args) {

        int[] arr2 = {5, 15, 25, 35};

        System.out.println("Array 2: " + Arrays.toString(arr2));
        System.out.println("Array 2 position 0: " + arr2[0]);
        System.out.println("Array 2 position 1: " + arr2[1]);
        System.out.println("Array 2 position 2: " + arr2[2]);
        System.out.println("Array 2 position 3: " + arr2[3]);

    }
}
```

{% embed url="https://youtu.be/6fO7mcw0FhA" %}

