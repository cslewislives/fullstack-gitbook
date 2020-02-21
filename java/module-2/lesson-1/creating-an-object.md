# Creating an Object



Now that we have discussed some of the characteristics of an object, let us create one. 

## Person Object

{% tabs %}
{% tab title="Person Object Creation Steps" %}
Steps to create a Person object:  


* Create a new IntelliJ project called PersonObject. Use com.company as the GroupID and PersonObject as the ArtifactID.
* Inside the com.company package, create a Java class called Person
* Add property with data type `String` and variable name `name`
* Create a method with a `public` access modifier; no return value;   the method name of `setName`, taking in the parameter `String name` and finally, in the body of the method, setting `this.name = name`. 
* Create a method with a `public` access modifier; no return value;   the method name of `sayHello` and, inside the method body, a  print line that reads \`\("Hello, I am " + this.name\);
{% endtab %}

{% tab title="Person Object Code" %}
```java
public class Person {
  String name;

  public void setName(String name) {
    this.name = name;
  }

  public void sayHello() {
    System.out.println("Hello, I am " + this.name);
  }
}
```
{% endtab %}
{% endtabs %}

With the Person object created, we will create an `App` class with a `main` method to instantiate and use the object. 

{% hint style="warning" %}
Remember, the `main` method is the entry point of any Java application. It is the point where out code starts its execution. 
{% endhint %}

{% tabs %}
{% tab title="App Class Creation Steps" %}
* In the same package as above, create an App java class with a `main` method. 
* Inside the main method, instantiate a **new** instance of the Person class created above. 
  * The `Person` on the left side of the equation is the data type associated with the object `jim`. The data type is Person. It is an object. 
  * The `new` keyword is telling the computer to make space for a new object.
  * The new object is going to be an instance of the `Person` object created above.
  * Call the `setName` method from the Person object to set the name

```java
Person jim = new Person();
jim.setName("Jim");
```

* Create a second instance of a Person called `callie`. Set the name appropriately.
* Call the Person object's `sayHello` method by calling the object name and the  method. 

```java
jim.sayHello();
callie.sayHello();
```

* Run the `main` method and examine the output. 
{% endtab %}

{% tab title="App Class Code" %}
```java
public class App {

  public static void main(String[] args) {

    Person jim = new Person();
    jim.setName("Jim");

    Person callie = new Person();
    callie.setName("Callie");

    jim.sayHello();
    callie.sayHello();
  }
}
```
{% endtab %}
{% endtabs %}

