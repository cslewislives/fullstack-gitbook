# Inheritance with Classes - Activity

![Architect Extends TeamLead](../../../.gitbook/assets/image%20%2845%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt. 

{% tabs %}
{% tab title="Instructions" %}
1. Create a new class called `Architect` which inherits from `TeamLead`
2. This class should have two additional methods:
   * `createTechRoadmap` which takes no parameters and returns nothing
   * `evaluateVendor` which takes no parameters and returns nothing
{% endtab %}

{% tab title="Solution Code" %}
```java
package com.company.inheritance;

public class Architect extends TeamLead {

    public void createTechRoadmap() {
        // code here
    }

    public void evaluateVendor() {

    }
}
```

* A TeamLead **is=a** developer, an Architect **is-a** TeamLead, and an Architect **is-a** Developer too!!
* TeamLead and Architect get methods "for free" from their base classes.
  * TeamLead inherits the methods from the Developer class and Architect inherits the methods from the TeamLead class which include the methods from the Developer class.
* This is an instance of code reuse: derived classes get to reuse code in parent classes.
* There are also methods inherited from Object.
{% endtab %}
{% endtabs %}

 

