---
description: Discussion of the Map interface.
---

# Map Interface and Concepts

The map is a powerful key/value data structure that is widely used in Java programs. The map builds on many of the principles presented in the lesson on collections and lists. In this lesson, we cover the basics of using maps in a program. 

* Maps are similar in many ways to collections and lists: the Map interface defines an API that allows us to manipulate groups of related objects.
* Maps are a key/value data structure—we store values in the map and associate those values with keys. This is similar to a coat check: they store your coat in the closet and give you a token with a number that maps to the location of your coat in the closet. When you want your coat, you present your token and they use that to find your coat.
* Since the values are accessed by key, the Map interface makes no claim about the order of the values—order doesn't matter in a map. If you need a guaranteed order to your values, you should use a list.
* Each key can map to one and only one value and duplicate keys are not allowed. This makes sense if we go back to our coat check analogy: if the coat check token mapped to more than one coat, it would be impossible to keep track of who owned what coat. Similarly, if there are duplicate coat tokens that point to one coat, how do you know who to give the coat to?
* The values have fewer restrictions; for example, we can have duplicate values. Going back to the coat check, it is possible that two people have the exact same type and size of coat. We can still check both and we will be able to tell them apart because we have unique coat check tokens \(keys\).

## Map Declaration and Initialization

* Declaring and initializing a Map is very similar to how you would declare and initialize a List.
* We **program to interfaces**, not to concrete classes. We use a map reference to point to the HashMap implementation.
* Imports needed for using the Map interface and the HashMap class.

```java
package com.company;

import java.util.HashMap;
import java.util.Map;

public class App {

    public static void main(String[] args) {

        // Declare and initialize a map
        Map<String, Integer> heights = new HashMap<>();
    }
}
```

