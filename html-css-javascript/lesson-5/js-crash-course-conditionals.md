# Conditionals

### Conditionals

When writing If/Else statements in Java once again it will look fairly identical to JS:

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let x = 4

if (x > 5) {
	console.log("High")
} else {
	console.log("Low")
}
```
{% endtab %}

{% tab title="Java" %}
```java
int x = 4;

if (x > 5) {
	System.out.println("High");
} else {
	System.out.println("Low");
}
```
{% endtab %}
{% endtabs %}

#### Truthy/Falsy

Java however, does not have truthy/falsy. The below code will throw an error in Java:

```java
int x = 4

if (x) {
	System.out.println("High");
} else {
	System.out.println("Low");
}

//result will throw an error
```

In Java you must declare what the condition is in order for the conditional to work properly.



