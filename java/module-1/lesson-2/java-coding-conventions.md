---
description: >-
  Practicing good coding styles and naming conventions is vital to your success
  in this course and your future role as a developer.
---

# Java Coding Conventions



### Indentation and Line Breaks

> "Programs should be written for people to read, and only incidentally for machines to execute."
>
> Hal Abelson

What do you think this quote means? 

The average developer spends an astounding 70% of their time reading and maintaining existing code. Another 20% of their time is spent designing projects and only 10% is spent actually coding. This means that the most economic thing you can do as a developer is write easy to read code.  

**The Take Away:** Code should be easy to read. Consistent formatting and styling help make this possible. Click the tabs below to see how proper indentation impacts the legibility of code. 

{% tabs %}
{% tab title="Messy Code" %}
```java
public class HelloWorld { public static void main(String[] args) {
System.out.println("Hello World!");System.out.println("Hi All!");
}
}
```
{% endtab %}

{% tab title="Clean Code" %}
```java
public class HelloWorld {
	public static void main(String[] args) {
		System.out.println("Hello World!");
		System.out.println("Hi All!");
	}
}
```
{% endtab %}
{% endtabs %}

{% embed url="https://youtu.be/HMlvocC9rfs" %}

### Naming Conventions

These naming conventions have been adopted by the Java developer community and are followed by everyone. If you break them the compiler won't let you know, but your fellow developers will \(and not always nicely\). 

You will be expected to follow these conventions in your projects and homework for the remainder of the course. 

* The first letter in variables and method names are lowercase _i.e._ `main()`
* The first letter in a class name is uppercase _i.e_. `class App`
* Java uses camel case for naming _i.e._ `myTeam` or `calculateCustomerTotal`
* Classes and variables are nouns _i.e_. `Dog` or `studentId`
*  Methods are verbs _i.e._ `calculateSum()` or __`updateName()` __
* Booleans names should begin with is, was, has, can, or should _i.e._ `hasId` __or `isValid`
* Names should be descriptive

Let's see some code examples: 

```java
String addressAndCity = "42 Wallaby Way, Sydney Australia";
int littleNumber = 5;
boolean isGoodExample = false;
```

If you're interested and want to read more about naming conventions try the [Java 8 Pocket Guide](https://www.oreilly.com/library/view/java-8-pocket/9781491901083/ch01.html) for a quick reference or [A Short Summary of Java Best Practices](https://medium.com/@rhamedy/a-short-summary-of-java-coding-best-practices-31283d0167d3) for a more comprehensive look at naming conventions. 

Be sure to check out this video as well

{% embed url="https://youtu.be/xHCLXAkBp0Q" %}

### Valid Identifiers and Keywords Restrictions

In addition to the conventions listed about there are some hard and fast rules around naming that the compiler will enforce. 

* Identifiers cannot span multiple lines \(duh\)
* Identifiers can only contain the following characters:
  * Numbers
  * Letters
  * Underscores \(\_\)
  * Dashes \(-\)
  * Dollar signs \($\)
* Identifiers can’t start with numbers. 
* Identifiers cannot contain spaces.

There's also a list of keywords that you CAN NOT use to name variables. You can find a complete list of keywords on [Geeks for Geeks](https://www.geeksforgeeks.org/list-of-all-java-keywords/).

{% hint style="danger" %}
While you _can_ begin a variable with and underscore, dash, or dollar sign, this is not a normal Java convention and should be avoided. Variable and method names should begin with a lowercase letter. 
{% endhint %}

