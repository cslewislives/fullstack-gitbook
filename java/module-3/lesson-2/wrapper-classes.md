---
description: Demonstration of how wrapper classes work with collections.
---

# Wrapper Classes



* We want to show how wrapper classes work with collections.
* We will demonstrate the autoboxing and unboxing features of Java that make using wrapper classes more natural.
* Wrapper classes, autoboxing, and unboxing are things that every Java developer needs to understand, but the details get hidden by autoboxing and unboxing in most cases.
* You need to understand this: wrapper classes, autoboxing, and unboxing are popular questions interviewers and evaluators ask to see how well you understand the Java language!

```java
package com.company.lists;

import java.util.ArrayList;
import java.util.List;

public class WrapperClasses {

    public static void main(String[] args) {
        List<Integer> integerList = new ArrayList<>();

        // Creating a wrapper for an int

        // Explicit - this is deprecated
        Integer myInteger = new Integer(42);

        // Another approach to being explicit - not necessary
        myInteger = Integer.valueOf(67);

        // Autoboxing - the way to go
        myInteger = 55;

        // Unboxing - automatic
        int myPrimitive = myInteger;

        // Using primitives with collections

        // Adding an Integer object
        integerList.add(myInteger);

        // Adding an int primitive - uses autoboxing
        integerList.add(myPrimitive);
    }

}
```

{% embed url="https://youtu.be/06XnU4MeIsw" %}

