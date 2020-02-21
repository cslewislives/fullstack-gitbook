---
description: Introduction to abstract base classes.
---

# Abstract Base Classes

Abstract base classes are another organizational too, that are something in between an interface and a regular class.

### Characteristics of an Abstract Class

1. They cannot be instantiated. Abstract base classes are meant to be extended; they are not meant to stand on their own.
2. They can provide implementations of methods \(just like regular classes\).
3. They can have properties \(just like regular classes\).
4. They can define methods with no implementation. Regular classes cannot do this; this is similar to an interface. Any class that extends the abstract base class MUST provide an implementation for each of these methods.

### Example of Use

```java
package com.company.inheritance;

public abstract class StaffMember {
    protected String name;
    protected String department;

    public abstract void submitTimeCard();

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getDepartment() {
        return department;
    }

    public void setDepartment(String department) {
        this.department = department;
    }
}

// =====================================

package com.company.inheritance;

public class Developer extends StaffMember {

    public void submitTimeCard() {
        System.out.println("Submitting time card...");
    }

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

* The `StaffMember` abstract class defines a method that must be implemented in classes that extend it like an interface would.

  ```java
  public abstract void submitTimeCard();
  ```

* The `Developer` class must provide an implementation for the `submitTimeCard()` method.
* Abstract base classes are just another tool in the toolbox. They are a pretty specialized tool, so they won't be using them very often, especially as junior engineers, but they do solve specific problems and are great when needed.

{% embed url="https://youtu.be/e97ZiLLyYx4" %}

