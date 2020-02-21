---
description: partial
---

# JS Crash Course

In JavaScript you can declare a variable in a variety of ways. 

```javascript
var num = 4;
let num2 = 5;
const num3 = 6;
```

`var`, `let`, and `const` can all be used to declare any type of variable in JavaScript. 

`var` and `let` are similar with two key exceptions: 

* `var` is function scoped and `let` is block scoped
  * Scope determines the visibility or accessibility of a variable or other resource in the area of your code.
  * **Function Scope**
    * Whenever you declare a variable in a function, the variable is visible only within the function.
    * You can't access it outside the function.

```javascript
function foo(){
    var fruit ='apple';
    console.log('inside function: ',fruit);
}

foo();                    //inside function: apple
console.log(fruit);       //error: fruit is not defined 
```

* **Block Scope**
  *  A block scope is the area within **if**, **switch** conditions or **for** and **while** loops. 
  * Generally speaking, whenever you see **{curly brackets}**, it is a block. 
  * In ES6, **`const`** and **`let`** keywords allow developers to declare variables in the block scope, which means those variables exist only within the corresponding block.

```javascript
function foo(){
    if(true){
        var fruit1 = 'apple';        //exist in function scope
        const fruit2 = 'banana';     //exist in block scope
        let fruit3 = 'strawberry';   //exist in block scope
    }
    console.log(fruit1);
    console.log(fruit2);
    console.log(fruit3);
}

foo();
//result:
//apple
//error: fruit2 is not defined
//error: fruit3 is not defined
```

{% hint style="info" %}
For more info [check out this article!](https://dev.to/sandy8111112004/javascript-introduction-to-scope-function-scope-block-scope-d11)
{% endhint %}

* `var` is hoisted. `let` is not. 
  *  In JavaScript, a variable can be declared after it has been used.
  * Variables and constants declared with `let` or `const` are not hoisted!

```javascript
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element

var x; // Declare x
```

`let` and `const` are similar except that once you assign a `const` a value, it cannot be reassigned.

![](../.gitbook/assets/image%20%2854%29.png)

### Truthy/Falsy

Welcome to the world of truthy and falsy. JavaScript will happily make a boolean of any value in a conditional. 

The following values are **always falsy**:

* `false`
* `0` \(zero\)
* `''` or `""` \(empty string\)
* `null`
* `undefined`
* `NaN`

Everything else is **truthy**. That includes:

* `'0'` \(a string containing a single zero\)
* `'false'` \(a string containing the text “false”\)
* `[]` \(an empty array\)
* `{}` \(an empty object\)
* `function(){}` \(an “empty” function\)

How could you use the concept of truthy and falsy to check to see if a variable was initialized and assign a default value if not?

### Functions

* Function Declaration
  * Closest in syntax to a Java Method
* Function Expression
  * Creating a variable and assigning a function to it.
* Arrow Function
  * Similar to Java Lambdas

{% tabs %}
{% tab title="Java" %}
```java
public int add(int num1, int num2){
	return num1 + num2;
}
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
//Function Declaration
function add(num1, num2){
	return num1 + num2
}

//Function Expression
const add = function(num1, num2){
	return num1 + num2
}

//Arrow Function
const add = (num1, num2) => num1 + num2
```
{% endtab %}
{% endtabs %}

**Notice** that there are no access modifiers in JS. **Everything is public.**

The way you create functions often comes down to preference. There are a few differences between each version but we won't worry about that at the moment.

### Objects

Fairly recently \(as of ES6\) in JavaScript you can create a class very similarly to Java. Remember that JS is fairly loose, and everything is public.

{% tabs %}
{% tab title="Java" %}
```java
class Person {
	private String name;
	private int age; 

	public Person(String name, int age){
	  this.name = name;
	  this.age = age;
	}

//getters and setters omitted for brevity

	public void greet(String hi){
	  System.out.println(hi + this.name);
	}
}
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
class Person{
	
	constructor (name, age){
		this.name = name;
		this.age = age;
	}
	
	greet(hi){
	  console.log(hi + this.name);
	}
	//there is no need for getters and setters because you can access each element directly
}
```
{% endtab %}
{% endtabs %}

However you will probably still encounter this way in many JS files:

{% tabs %}
{% tab title="Java" %}
```java
class Person {
	private String name;
	private int age; 

	public Person(String name, int age){
	  this.name = name;
	  this.age = age;
	}

//getters and setters omitted for brevity

	public void greet(String hi){
	  System.out.println(hi + this.name);
	}
}
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
function Person(name, age){
	this.name = name;
	this.age = age;
	this.greet = function(hi){
	  console.log(hi + this.name);
	}
}
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
This means the exact same thing as using Class.
{% endhint %}

Then to create a new object is very similar.

{% tabs %}
{% tab title="Java" %}
```java
Person page = new Person("Page", 12);

String pName = page.getName();
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
const page = new Person("Page", 12)

const pName = page.name
```
{% endtab %}
{% endtabs %}

**Notice** that in the JS we can access `name` directly by using dot notation: `page.name`.

This is where things get tricky. In JavaScript you don't have to create a class or constructor in order to instantiate an object. You can create objects directly in JavaScript:

```javascript
const page = {
	name: "Page",
	age: 12,
	greet: function(hi){
	  console.log(hi + this.name)
	}
}
```

