# Implementing Multiple Interfaces - Activity

![Implementing Multiple Interfaces](../../../.gitbook/assets/image%20%2830%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt. 

{% tabs %}
{% tab title="Instructions" %}
Remember:

* Classes can implement more than one interface.
* The interfaces are listed in a comma-delimited list after the `implements` keyword.
* All methods from all interfaces must be implemented by the class.

Instructions:

1. Create the interface, `Storable()`.
2. `Storable()` should define two methods, `storeData()` and `retrieveData()`. Both methods should return nothing and take no parameters.
3. Then add it to the list of interfaces the `SchoolRecord` implements.

Hint: If you a compiler error occurs, remember that you need to provide the implementations the `Storable()` methods!
{% endtab %}

{% tab title="Solution Code" %}
```java
public interface Storable {
    public void storeData();
    public void retrieveData();
}

//===========================

public class SchoolRecord implements Storable, Auditable {
    // Properties here
    // Additional methods here

    // Storable methods here
    public void storeData() {
        // method body implementation here
    }

    public void retrieveData() {
        // method body implementation here
    }

    // Auditable methods here
    public void runAudit() {
        // method body implementation here
    }

    public void sendAuditToState() {
        // method body implementation here
    }
}
```
{% endtab %}
{% endtabs %}

