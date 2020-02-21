# Interface Implementation - Activity

![](../../../.gitbook/assets/image%20%2833%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
Again, now it's your turn to implement your newly created interface, `Auditable`.

1. Create a new class called `SchoolRecord` that implements `Auditable`.
2. The `runAudit()` method should simply print the word “auditing” to the console.
3. The `sendAuditToState()` method should simply print a confirmation message to the console.

Note: We'll be implementing actual functionality to the methods `runAudit()` and `sendAuditToState()` later. But for now just make sure that you understand how to add code to those individual methods!
{% endtab %}

{% tab title="Solution Code" %}
```java
public class SchoolRecord implements Auditable {

    public void runAudit() {
        System.out.print("auditing");
    }

    public void sendAuditToState() {
        System.out.print("audit sent");
    }

}
```
{% endtab %}
{% endtabs %}

