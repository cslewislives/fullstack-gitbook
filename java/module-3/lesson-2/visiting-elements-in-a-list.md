# Visiting Elements in a List

We can visit individual elements of an array using for loops, enhanced for loops, and iterators.

### Loops

The Loop examples are pretty straightforward and should be familiar to you.

First we will create our Array List and add elements to it.

```java
package com.company.lists;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class VisitingElements {

    public static void main(String[] args) {
        List<String> names = new ArrayList<>();

        // Add a bunch of names to the list
        names.add("Joe");
        names.add("Sally");
        names.add("John");
        names.add("Sue");
        names.add("Jane");
        names.add("Mike");
        names.add("James");
        names.add("Jeff");
        names.add("Curt");
        names.add("Dana");

        System.out.println("How many names do we have? " + names.size());
    }
}
```

Next we will access the elements using a for loop

```java
for (int i = 0; i < names.size(); i++) {
    System.out.println(names.get(i));
}
```

Pretty straightforward. Again we will access the elements now using an enhanced for loop.

```java
for (String currentName : names) {
    System.out.println(currentName);
}
```

### Iterators

The iterator example is more involved:

* Step one is declaring and initializing the iterator. Iterators are generics as well, so we have to specify which objects will be in the iterator.

```java
Iterator<String> iter = names.iterator();
```

* The type of objects in the iterator is dictated by the type of objects in the collection from which we get the iterator.

```java
while (iter.hasNext()) {
    System.out.println(iter.next());
}
```

* You can only visit all the elements once when using an iterator.
* If you want to go through the elements again, you have to get a new iterator from the collection.

### Complete Example

```java
package com.company.lists;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class VisitingElements {

    public static void main(String[] args) {
        List<String> names = new ArrayList<>();

        // Add a bunch of names to the list
        names.add("Joe");
        names.add("Sally");
        names.add("John");
        names.add("Sue");
        names.add("Jane");
        names.add("Mike");
        names.add("James");
        names.add("Jeff");
        names.add("Curt");
        names.add("Dana");

        System.out.println("How many names do we have? " + names.size());

        // Visit each name using a regular for loop
        for (int i = 0; i < names.size(); i++) {
            System.out.println(names.get(i));
        }

        System.out.println("============================");

        // Visit each name using an enhanced for loop
        for (String currentName : names) {
            System.out.println(currentName);
        }

        System.out.println("============================");

        // Visit each element using an iterator

        // We first need to get an iterator from the names List
        Iterator<String> iter = names.iterator();

        while (iter.hasNext()) {
            System.out.println(iter.next());
        }
    }
}
```

{% embed url="https://youtu.be/p77CM6d2FPA" %}



