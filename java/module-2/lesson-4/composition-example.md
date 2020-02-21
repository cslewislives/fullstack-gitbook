---
description: An example of composition with a new BetterAccount class.
---

# Composition Example

* Now that we have created an `Address` class that we can reuse, we can now better organize our previous `BadAccount` class.
  * We can use our `Address` class to simplify our account and create `homeAddress` and `shippingAddress` properties in our new `BetterAccount` class. 

```java
package com.company.composition;

public class BetterAccount {

    private String firstName;
    private String lastName;
    private String username;

    private Address homeAddress;
    private Address shippingAddress;

    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public Address getHomeAddress() {
        return homeAddress;
    }

    public void setHomeAddress(Address homeAddress) {
        this.homeAddress = homeAddress;
    }

    public Address getShippingAddress() {
        return shippingAddress;
    }

    public void setShippingAddress(Address shippingAddress) {
        this.shippingAddress = shippingAddress;
    }
}
```

