---
description: Example that shows that interfaces can be extended as well.
---

# Inheritance with Interfaces

"Inheritance works with interfaces as well! One interface can extend \(or specialize\) another interface just like a class can extend another class."

"We're going to go back to the examples we presented in the Interfaces lesson. We are going to extend the `Storable` interface and then have a new class implement the extended interface:"

```java
package com.company.interfaces;

public interface Storable {

    public void storeData();

    public void retrieveData();

    public default void sillyMethod () {
        // code here
    }
}

// =================================

package com.company.interfaces;

public interface SecureStorable extends Storable {

    public void encryptData();

    public void decryptData();
}
```

* The interface `Storable` is extended in the same way that a class would be. We use the `extends` keyword.
* The child interface \(`SecureStorable` in this case\) can have as many or as few new method definitions as needed. In this case, we just have two.

We have now seen what it looks like for one interface to inherit from another. It will be up to you in the next activity to implement the `SecureStorable` interface. 

