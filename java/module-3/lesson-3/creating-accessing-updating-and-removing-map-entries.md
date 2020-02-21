---
description: 'An example of creating, accessing, updating, and removing Map entries.'
---

# Creating, Accessing, Updating, and Removing Map Entries

* We're showing basic functionality here; the emphasis should be on how the Map API works.
* Why can we use an `int` to store Joe's height when maps only deal with objects? \(we can do this because of unboxing here\). 
*  `put` and `replace` have the same effect if the key exists in the map. If the key does not exist in the map, `put` will create a new entry whereas `replace` will do nothing.

```java
// Creating map entries
heights.put("Joe", 72);
heights.put("Jane", 63);
heights.put("Sally", 65);

// See how many entries there are
System.out.println("Number of entries in the map: " + heights.size());

// Get Joe's height
int joesHeight = heights.get("Joe");
System.out.println("Joe is " + joesHeight + " inches tall.");

// Update Joe's height with replace
heights.replace("Joe", 74);
joesHeight = heights.get("Joe");
System.out.println("Joe is " + joesHeight + " inches tall.");

// Update Joe's height with put
heights.put("Joe", 70);
joesHeight = heights.get("Joe");
System.out.println("Joe is " + joesHeight + " inches tall.");
```

* Removing an entry is straightforward - just call `remove` with the key of the entry you want to take out of the map

```java
// Now remove Jane's entry
heights.remove("Jane");

// See how many entries there are
System.out.println("Number of entries in the map: " + heights.size());
```

