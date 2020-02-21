---
description: Explanation and an example of polymorphism with interfaces.
---

# Polymorphism and Interfaces

Polymorphism applies to interfaces in two ways:

* A class that implements an interface can be referred to with a reference that is the type of the interface.
  * For example, `SchoolRecord` can be referred to as a `SchoolRecord` type or as a `Storable` type. 
* Because interfaces can be extended just like classes, you can refer to an object that implements an extended interface with a reference that is the type of the base interface.

```java
public interface Auditable {

    public void runAudit();

    public void sendAuditToState();
}

// =================================

public interface Storable {

    public void storeData();

    public void retrieveData();

}

// ==================================

public class SchoolRecord implements Storable, Auditable {

    public void storeData() {
        // code here
    }

    public void retrieveData() {
        // code here
    }


    public void runAudit() {
        // code here
    }

    public void sendAuditToState() {
        // code here
    }
}

// =======================================

public class App {

    public static void main(String[] args) {

        // Interface examples
        SchoolRecord record = new SchoolRecord();

        // This works because we can use an interface reference to point to an instance of a class
        // that implements that interface
        Auditable auditableRecord = record;
        Storable storableRecord = record;
    }
}
```

* This is basically the same as with classes and polymorphism
* When we use the `Auditable` type, only the methods from that interface are available.
* When we use the `Storable` type, only the methods from that interface are available.

{% embed url="https://youtu.be/OZYjf1m0Nbc" %}

