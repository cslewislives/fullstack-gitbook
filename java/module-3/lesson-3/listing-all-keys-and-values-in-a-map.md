---
description: An example of listing the keys and values in a Map.
---

# Listing All Keys and Values in a Map

### Keys

* We can ask the map for all of its keys.
* The keys from the map are returned in a Set collection, so we can use an iterator to access each key.
* Sets are generic classes and require us to specify the type of object that will be in the set \(in this case, Strings\). 
* Why do you think the keys are returned as a set? What are the characteristics of a set? Sets can't have duplicates, just like we can't have duplicate keys.

```java
    // Now let's get all of the keys and print them out
    Set<String> myKeys = heights.keySet();
    for (String key : myKeys) {
        System.out.println(key);
    }
```

### Values

* We can ask the Map for all of its values as well.
* Values are returned as a collection.
* Again, remember that collections are generics, so we have to specify the type of the object that will be in the collection \(integer, in our case\).
* Why do you think values are returned as a collection; why not a set? We could have duplicate values, so a set would not work for the values.

```java
    // New let's get all of the values
    Collection<Integer> myValues = heights.values();
    for (Integer value : myValues) {
        System.out.println(value);
    }
```

### Using the Key Set to List All Values

* What if we want to list out the keys and their associated values?
* One way to do this is to get the set of keys, go through them one by one, and use each to access its associated value.

```java
// Now let's get all of the keys and use them to print out our key/value pairs
// We'll reuse the myKeys reference
myKeys = heights.keySet();
for (String key : myKeys) {
   System.out.println("Key = " + key + " : " + " Value = " + heights.get(key));
}
```

### Entry Set of a Map

* We can accomplish the same this using the entry set of the map.
* Each key/value pair forms a `Map.Entry` in the map. `Map.Entry` is also a generic, so now we have generics two-deep \(a set of entries of String/integer\)!
* Definitely go through this syntax slowly!

```java
// Now let's use the entry set to print all the key/values pairs
Set<Map.Entry<String, Integer>> myEntries = heights.entrySet();
for (Map.Entry<String, Integer> entry : myEntries) {
    System.out.println("Key = " + entry.getKey() + " : " + " Value = " + entry.getValue());
}
```

{% embed url="https://youtu.be/gWjj1n-3d2E" %}



