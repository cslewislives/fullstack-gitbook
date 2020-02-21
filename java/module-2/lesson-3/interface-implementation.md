---
description: Implement a Java Interface.
---

# Interface Implementation

 After an interface is declared, we must create a class to **implement** the interface.

There are two parts to this:

* We must indicate that the class will be adhering to the interface \(we call this **implementing** the interface\).
* The class must provide and implement each of the methods declared in the interface.

```java
public class SchoolRecord implements Storable {
    // Properties here
    // Additional methods here

    public void storeData() {
        // method body implementation here
    }

    public void retrieveData() {
        // method body implementation here
    }
}
```

* Once we have added the implementation with the  `implements Storable` code, we need to provide an implementation of the methods defined in the interface. If we do not, IntelliJ will give us an error message that shows that we are missing methods. 
* Once we have added the methods shown above, our class will live up to the Storable contract, and the errors from IntelliJ will go away.
  * Notice that we do not actually have to put any code into the method body; we just need to have these methods with at least an empty method body for the compiler to be happy.
* If we wanted to add additional methods, such as a  `printReport()` method, we can do it as long as the interface methods are there as well. We can add as many additional methods as we would like. 

#### More on Implementation

* The `implements` keyword is used to indicate that this class will adhere to the interface.
* Each of the methods defined in the interface will have an implementation.
*  Classes can implement more than one interface. The interfaces are listed in after the `implements` keyword and then all methods from all interfaces must be implemented in the class.

{% embed url="https://youtu.be/E3KaZxH8Pmc" %}

