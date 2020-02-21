# Interface Declaration - Activity

![Interface Declaration](../../../.gitbook/assets/image%20%2896%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
Now it's your turn to create an interface!

1. Ceate a new interface called `Auditable`.
2. The `Auditable` interface should define a method called `runAudit()` that takes no parameters and returns nothing.
3. The `Auditable` interface should also define another method called `sendAuditToState()` that takes no parameters and returns nothing.

If you're having an issues with this activity at all, reference [https://www.w3schools.com/java/java\_interface.asp](https://www.w3schools.com/java/java_interface.asp).
{% endtab %}

{% tab title="Solution" %}
```java
public interface Auditable {
    public void runAudit();
    public void sendAuditToState();
}
```
{% endtab %}
{% endtabs %}

