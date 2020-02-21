# Methods and Classes

### Methods

In Java the closest thing to a function is called a **method.** Let's take a look at what a method is:

* Methods are named blocks of code that we can call \(or invoke\) to do work for us.
* Methods are one good way to achieve code reuse
  * We write the method once but we call it over and over.
* Methods can have zero or more parameters. 
  * Parameters are values that we pass into the method. The method uses these values when doing its work.
  * Example: An add method takes in two numbers. The method adds those two numbers together to calculate the sum. The two numbers are the parameters. 
* A method may or may not return a value.
  * Example: That add method we mentioned before may return the sum of the two numbers passed in. But an alternate implementation of the add method may not return the sum; instead, it may just print the sum out to the console.

When writing a method the syntax is very similar to a JavaScript Function declaration: 

{% tabs %}
{% tab title="JavaScript" %}
```javascript
//Function Declaration
function add(num1, num2){
	return num1 + num2
}
```
{% endtab %}

{% tab title="Java" %}
```java
public int add(int num1, int num2){
	return num1 + num2;
}
```
{% endtab %}
{% endtabs %}

**Notice** that there a few new things in the Java method**.** We won't get too deep here as you will be taught this in class but you should be aware of it.

`public` **-** public is an **ACCESS MODIFIER**. Your access modifier can be public, private, or protected. This controls which parts of your application have access to this method. Just use public for now; we'll talk about the others in class.

`int` - This is the **RETURN TYPE**. Methods are like a box - data can only be passed in through parameters and can only escape the curly braces through the return keyword. For now, just know that we have to declare what type of variable will come back out of the function. `void` means that nothing is returned where as `int` would indicate that an integer will be returned. 

`add` - This is the **METHOD NAME**. The method name can be literally anything \(barring keywords and names that contain illegal characters, [https://www.geeksforgeeks.org/list-of-all-java-keywords/](https://www.geeksforgeeks.org/list-of-all-java-keywords/)\). It's like a variable name and it's how you'll use, or call, the method later. By convention, method names should begin with a verb. 

`int num1, int num2` - These are **PARAMETERS**. Parameters always appear inside parentheses and are how data get passed into the function. The data type of the parameter must be declared.

### Classes

In Java they do have objects \(it is an object oriented programming language\) **BUT** they are not the same as JavaScript Objects.

The closest thing to JS Objects are Java **Classes**.

{% tabs %}
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
{% endtabs %}

These may look completely different but they are doing very similar things. We will learn a lot more about this in class. 

{% hint style="info" %}
The biggest takeaway is that in Java, object means something different and Class is the closest thing to JS objects.
{% endhint %}

Then to create a new class is very similar to creating a new object in JS.

{% tabs %}
{% tab title="JavaScript" %}
```javascript
const page = new Person("Page", 12)

const pName = page.name
```
{% endtab %}

{% tab title="Java" %}
```java
Person page = new Person("Page", 12);

String pName = page.getName();
```
{% endtab %}
{% endtabs %}

**Notice** that in Java we declare the type of the new class as the class itself.

Again this may seem very confusing but you will be learning a lot about this in class. The biggest thing from this section is that there are similarities between the two languages but Java is much more strict, and uses a few different words for similar pieces of code.

