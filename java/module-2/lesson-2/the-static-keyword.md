---
description: Class methods vs object methods
---

# The "static" Keyword

The concept of the `static` keyword can be confusing for new programmers because it doesn't have a counterpart in the real world like the other OOP concepts. Don't worry if some of this doesn't totally make sense right now. It will become clear over time as you use these tools more. 

Properties and methods marked with the `static` keyword are associated with the class and not with any particular object created from the class.

Every time we instantiate an object it gets its own unique copy of each of the non-static methods and properties. 

Because static properties and methods are associated with the class:

* There is only **one** copy of a static property or method \(no matter how many objects have been instantiated from the class\).
* Static methods can only directly access other static methods in a class. This is why we had to make all methods static in the classes we've created so far. Since the `main` method must be static, we could only call other static methods from `main`.
* Static methods can be accessed without creating an instance of the class:
  * For example of `Math.abs(...)` and `System.out.println(...)`
  * Contrast that with Scanner where we must create a Scanner object to use the methods `Scanner scanner = new Scanner(System.in)` `scanner.nextLine()`.

The main point here is that from here forward, we'll only use the `static` keyword when it is needed. In general, it isn't. 

Watch this video for more information on the "this" and "static" keywords! Also included in this video is more information on dot notation!

{% embed url="https://youtu.be/nYoF2qp0aww" %}

