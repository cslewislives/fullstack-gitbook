---
description: Learn to use the index operator to access and update array elements.
---

# Accessing & Updating Array Elements

If you successfully completed the arrays activity, you already have an understand of how to access array elements. 

As demonstrated, you use the **index operator** to access the individual elements in an array. 

To access an array element, you reference the name of the array and the index number of the element that you want to view. Remember, the position of index elements begins with the number 0.

```java
        String[] Pets = {"dog", "cat", "rabbit", "ferret", "parrot"};

        //Pets[0] = "dog";
        
        System.out.println("Pets index element 0: " + Pets[0]);
```

To update an array element, you utilize the name of the array and index position as above, but you also incorporate the assignment operator \( the = sign\). 

```java
        String[] Pets = {"dog", "cat", "rabbit", "ferret", "parrot"};
        
        // To change Pets[3] from ferret to hermit crab, use the 
        // assignment operator
        
        Pets[3] = "hermit crab";
        
        System.out.println("Pets index element 3 has changed from ferret to " + Pets[3]);
```

Drop the following code into IntelliJ to see accessing and updating array elements in action. 

```java
package com.company;

import java.util.Arrays;

public class Animals {

    public static void main(String[] args) {



        String[] Pets = {"dog", "cat", "rabbit", "ferret", "parrot"};

        System.out.println("The original Pets Array: " + Arrays.toString(Pets));
        
        System.out.println("==========================");
        
// To access index position 0 we reference the name of the array and
// the position of the index.

        System.out.println("To access Pets index element 0 type Pets[0]: " + Pets[0]);
        
        System.out.println("==========================");
        
// To access Pets array element "ferrett" 
    
        System.out.println("To access Pets index element ferret type Pets[3]: " + Pets[3]);

        System.out.println("==========================");
        
// To change an index element you utilize the assignment operator (=).
// Here we are changing Pets index element three from ferret to hermit crab.

        Pets[3] = "hermit crab";
        
        System.out.println("Pets index element 3 has changed from ferret to " + Pets[3]);
        System.out.println("The NEW Pets array: " + Arrays.toString(Pets));

    }
}
```

