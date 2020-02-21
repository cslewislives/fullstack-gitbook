---
description: For-loops are the primary way of iterating through the elements in an array.
---

# Arrays and Loops

### Basic For Loops and Arrays

For loops and arrays work very well together. 

Arrays allow you to access the elements by referencing the number of the index position and for loops allow you to utilize numbers to determine the time you are cycling through the loop. 

We will continue to use the Pets array to demonstrate.

```java
        String[] Pets = {"dog", "cat", "rabbit", "hermit crab", "parrot"};
        
        for (int i = 0; i < Pets.length; i++) {
            System.out.println(Pets[i]);
        }
```

There are several items of note from the above code. 

* We use `int i` for the counter just like any other for loop. We start at 0 because we want to start with the first element in the array, which has an index of 0.
* Our termination condition says that we’ll keep going as long as `i` &lt; the length of the Pets array.
  * The length of the Pets array is 5 elements. Because the index position starts at 0 we can loop through ALL of the elements of the array  \(positions 0, 1, 2, 3 & 4\) before we reach the termination condition value of 5. 
* We increment `i` just like any other for loop.
* We access each element in the array by using the value of `i` as the index.

Input the following code into IntelliJ to see the process of iterating through an array using the for loop.

```java
package com.company;

public class Animals {

    public static void main(String[] args) {

        String[] Pets = {"dog", "cat", "rabbit", "hermit crab", "parrot"};
        
// int i is the counter. It begins at 0, just like the first index position
// of our array.

// The termination condition stops at Pets.length

// The iterator is by 1 to capture all of the index position in the Pets array. 
        
        for (int i = 0; i < Pets.length; i++) {
            System.out.println("The value of i: " + i);
            System.out.println("The value of Pets[i]: " + Pets[i]);
            System.out.println("================");
        }

    }
}
```

### Enhanced For Loops

An alternative to utilizing a traditional for loop, is to utilize an enhanced for loop. 

An **enhanced** for loop replaced the initialization, termination and increment pieces  with the following syntax:

```java
for (String element : Pets) {
    System.out.println(element)
    }
```

* The variable declared to the left of the enhanced for loop **must be the same data type** as the overall array. 
* The **variable** declared on the left side of the enhanced for loop is what is **utilized in the body** of the loop to denote each element that you are looping through. 
* The item to the right of the colon is the  **array** over which you want to iterate. 

For each iteration through the loop, each item in the given array is stored by the variable 'element' and then executed in the body of the loop. 

Given the above example, the loops iterates through the Pets array and then prints each of the pets to the console. 

Copy this code into IntelliJ to review the output resulting from the enhanced for loop. 

```java
package com.company;

public class Animals {

    public static void main(String[] args) {

        String[] Pets = {"dog", "cat", "rabbit", "hermit crab", "parrot"};
        
   
        for (String element : Pets) {
            System.out.println("The pets in the Pets array are: " + element);
            System.out.println("================");
        }

    }
}
```

{% embed url="https://youtu.be/CULgEFmZOGU" %}



