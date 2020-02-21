---
description: An example and explanation of declaring and initializing Lists.
---

# List Declaration and Initialization

```java
List<String> names = new ArrayList<String>();
List<String> names = new ArrayList<>();
```

* The first example specifies the type the list will hold on both the declaration and initialization side. This works but is verbose.
* The second example uses the diamond operator \(&lt;&gt;\), which infers the type on the initialization side. This syntax is a bit cleaner.
* We are declaring a type using the interface \(List\) and instantiating a class that implements the interface \(ArrayList\).
  * This is a pattern that we will continue to use—**program to interfaces, not concrete classes**. It promotes interoperability and gives us the ability to swap implementations without having to change a bunch of code.
* There are `import` statements that get generated when we use List and ArrayList. This is because collections are not part of the core language, so we need to import these libraries for our use.

```java
import java.util.ArrayList;
import java.util.List;
```

## Basic List Operations

For this example we will be using Strings just to demonstrate how lists work. Code along in IntelliJ to try our these examples for yourself. 

{% hint style="info" %}
Try out the following inside a main method. Make sure to add the necessary List and ArrayList imports if they are not auto-imported. 
{% endhint %}

### Checking Size and Adding an Element

```java
List<String> names = new ArrayList<>();

// This will print 0 since we have not added any names yet.
System.out.println("How many names do we have? " + names.size());

// Adding an element
names.add("Joe");
// This will now print 1 since we have added "Joe".
System.out.println("How many names do we have? " + names.size());
```

### Accessing an Element in a List

```java
// Accessing an element - notice that this looks a lot like accessing
// an array element
String tempName = names.get(0);
System.out.println("The first name in the list is: " + tempName);
```

### Adding More Elements to a List

* Elements get added to the end of the list by default.
* Accessing a single element in the list is unchanged, all that changes is the index.

```java
// Add another element
names.add("Sally");
System.out.println("How many names do we have? " + names.size());

// Elements get added to the back of the list by default
tempName = names.get(0);
// The first name will still be "Joe"
System.out.println("The first name in the list is: " + tempName);

tempName = names.get(1);
// The second name will be "Sally";
System.out.println("The second name in the list is: " + tempName);
```

### Accessing a Nonexistent Element

* We will see how to handle exceptions in one of the upcoming lessons.

```java
// What happens if we try to access the third (non-existent) element?
// OOPS!!!  A big error...
tempName = names.get(2);
System.out.println("The third element in the list is: " + tempName);
```

### Removing an Element From a List

```java
// Removing an element
names.remove(0);
System.out.println("How many names do we have? " + names.size());

tempName = names.get(0);
System.out.println("The first name in the list is: " + tempName);
```

### Clearing a List

```java
// Clearing a list
names.clear();
System.out.println("How many names do we have? " + names.size());
```

