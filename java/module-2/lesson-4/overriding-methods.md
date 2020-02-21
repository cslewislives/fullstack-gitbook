---
description: Explanation and an example of overriding methods.
---

# Overriding Methods

First let us start out with a quick review of **method overloading** so that there is no confusion between the two concepts. 

#### What We Know About Method Overloading

* Overloading refers to having multiple methods with the same name but different parameter lists.
* The requirement is that **the signature must be different**.
* Think back to the class that has several `add` methods or the `println()` method.

### Main Points of Method Overriding

* Code reuse from a parent class is great but what if the parent class implementation is not sufficient for your needs? Method overriding gives us a tool to address this situation.
* Method overriding means we are **replacing** \(i.e. overriding\) the base class implementation of a method.
* In order to do that, the method you implement **must have the same signature** as the method in the base class \(this makes sense because we're **replacing** the base implementation with our own\).

```java
package com.company.inheritance;

public class Developer {

    public void estimateStoryPoints() {
        System.out.println("Estimating my own Developer story points.");
    }

    public void checkInCode() {
        // code here
    }
}

// =====================================

package com.company.inheritance;

public class TeamLead extends Developer {

    public void planSprint() {
        // code here
    }

    public void assignWork(Developer dev) {
        // code here
    }

    public void estimateStoryPoints() {
        System.out.println("Estimating my story points (TeamLead)");
        System.out.println("Make sure everyone on my team has estimated their story points.");
    }
}

```

* Notice that the `estimateStoryPoints()` method is inherited in our `TeamLead` class from our `Developer` class. 
  * The parent class implementation \(`Developer` in this case\) is not sufficient for our needs in the `Team Lead` class. 
  * In order to remedy this, we must override the method and provide our own implementation in the `TeamLead` class.
* When overriding the method we need to  use **the same signature** as the method in the base class.

