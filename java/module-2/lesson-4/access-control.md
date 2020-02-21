---
description: Introduction of the protected access modifier.
---

# Access Control

 We have seen `public` \(everyone can see and use the code\) and `private` \(only code inside the class can see and use the code\). Since we now have a new relationships between classes \(inheritance\), we have a new access modifier `protected`. This means that only code inside this class or any classes that extend it can see and use the code. 

* Anything marked `private` cannot be seen or used by any derived classes. If you want a derived class to see/use the code, mark it `public` or `protected`.

```java
package com.company.inheritance;

public class Developer {

    public void estimateStoryPoints() {
        System.out.println("Estimating my own Developer story points.");
    }

    public void checkInCode() {
        // code here
    }

    private void privateMethod() {
        // code here
    }

    protected void protectedMethod() {
        // code here
    }
}
```

* The private method in this code would not be available to our `TeamLead` or `Architect` classes, but our protected method would be available to derived classes.

