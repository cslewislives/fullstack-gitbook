---
description: An example to show how inheritance is implemented in Java classes.
---

# Inheritance with Classes

In this example, we model roles on a software development team.

* Developer: can estimate story points \(we'll see how to do that in future lessons\) and check in code.
* TeamLead: extends Developer and can plan sprints \(we'll learn about sprints in future lessons; for now, just think about it as the work for the next chunk of time, such as a week\) and can assign work to Developers.
* Architect: extends TeamLead and can create the technology road map and evaluate vendors.
* This is a hierarchical set of relationships: the TeamLead extends the Developer and the Architect extends the TeamLead.

This structure would look like this:

* Developer -&gt; TeamLead -&gt; Architect

Now lets take a look at what the code for this would look like: 

```java
package com.company.inheritance;

public class Developer {

    public void estimateStoryPoints() {
        // code here
    }

    public void checkInCode() {
        // code here
    }
}

// ===========================

package com.company.inheritance;

public class TeamLead extends Developer {

    public void planSprint() {
        // code here
    }

    public void assignWork(Developer dev) {
        // code here
    }
}
```

Here you have the code for Developer and TeamLead, but it will be up to you to create the Architect class in the next activity!

{% embed url="https://youtu.be/3LamWnDIVyI" %}



