# Variables and Loops

Java is syntactically similar to JavaScript. We’re going to learn some Java fundamentals in this lesson.

Some of this may feel like review, but pay careful attention to the differences between Java and JavaScript. 

## Java vs. JavaScript

JavaScript is used on the client \(along with HTML and CSS\) to send data to and receive data from the server and display it on the screen for users.

Java is used on the backend of applications, i.e. the server, to build an **API** \(Application Programming Interface\) and send data from the database to the client.

### Variables

When it comes to variables in JavaScript you don't need to declare the data type that the variable will contain. Java on the other hand is what is known as a **strongly-typed** language.  Which means that variables are bound to _specific_ data types, and will result in **type** errors if types do not match up as expected in the expression — regardless of when **type** checking occurs.

For example:

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let num = 4 
let num2 = 4.2
let name = "Daisy"
let isCool = true
let numArr = [1, 2, 3, 4]
```
{% endtab %}

{% tab title="Java" %}
```java
int num = 4;
double num2 = 4.2;
String name = "Daisy";
boolean isCool = true;
int[] numArr = {1, 2, 3, 4};
```
{% endtab %}
{% endtabs %}

JavaScript also allows you to change the content of a variable. Java does not.

![](../../.gitbook/assets/image%20%28108%29.png)

JavaScript also has a value that is assigned to all uninitialized variables, `undefined`, Java does not.

![](../../.gitbook/assets/image%20%2870%29.png)

{% hint style="info" %}
`System.out.println()`is used the same as `console.log()`
{% endhint %}

### Loops

For Loops in Java will look very similar to For Loops in JavaScript:

{% tabs %}
{% tab title="JavaScript" %}
```javascript
for (let i = 0; i < 5; i++){
	console.log(i)
}
```
{% endtab %}

{% tab title="Java" %}
```java
for (int i = 0; i < 5; i++){
	System.out.println(i);
}
```
{% endtab %}
{% endtabs %}

**Notice** that the only difference is that our variable `i` must be given a type.

When iterating over an array there are similarities as well:

{% tabs %}
{% tab title="JavaScript" %}
```javascript
let numArr = [1,2,3,4,5,6]

for (let i = 0; i < numArr.length; i++){
	console.log(numArr[i])
}
```
{% endtab %}

{% tab title="Java" %}
```java
int[] numArr = {1,2,3,4,5,6};

for (int i = 0; i < numArr.length; i++){
	System.out.println(numArr[i]);
}
```
{% endtab %}
{% endtabs %}

When declaring an array in Java however, you must declare the data type that the array will hold. A Java array cannot hold more than one type of data.

```java
int[] numbers = {0, 1, 2, 3, 4, 5};
String[] carMakes = {"Porsche", "Tesla", "Honda", "GMC"};
```

