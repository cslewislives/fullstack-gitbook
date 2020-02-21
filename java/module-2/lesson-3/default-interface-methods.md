---
description: A sample use case for default method implementations in Java 8.
---

# Default Interface Methods

### Default Methods

* Default methods in interfaces allow us to add methods to an interface even if there are already classes that implement the old version.
* Before default methods, adding methods to an existing interface would break all classes that implemented the old version of the interface.

#### Why we might need a default method

* If we were to add additional methods to an interface that is already implemented, it would break all classes that implement that interface.
  * You could go to all of these classes and add the required methods, but if a large number of classes have implemented the interface, this would be very tedious and time consuming.
  * Default methods allow us to provide a default implementation in an interface.

```java
package com.company.interfaces;

public interface Storable {

    public void storeData();

    public void retrieveData();

    public default void sillyMethod () {
        // code here
    }
}
```

* Once we have the default keyword, we can provide a method body without getting any errors.
* Classes implementing the `Storable` interface previously are not affected by this additional method, since it now has a default implementation.

