# Student Object - Activity

![Student Object](../../../.gitbook/assets/image%20%2837%29.png)

Follow the process utilized to create the Person object to create a Student object.  

{% tabs %}
{% tab title="Student Object Activity" %}
Utilizing the `Person` activity as a guide, create a new `Student` class and the corresponding `App` class. 

* The `Student` class should have a `String` property called `name`, and a `double` property called `gpa`
* This class should have `setName` and `setGpa` methods that allow you to set a value for your properties.
* This class should have a method called `greet()`.

  * When `greet()` is called, it should print "Hello, I am \[name\] and I have a GPA of \[gpa\]."

* Once you have your `Student` class created, create a new class called `App` which has a main method.
* In that main method, create two new `Student` objects, set their `name` and `gpa`, then call the `greet()`method on each.

As always, utilize Google and the prior content to assist you in completing this activity. Try not to review the code until you have given this a solid attempt. 
{% endtab %}

{% tab title="Student Object Code" %}
```java
// Student class with name and gpa
public class Student {
  String name;
  double gpa;

  public void setName(String name) {
    this.name = name;
  }

  public void setGpa(double gpa) {
    this.gpa = gpa;
  }

  public void greet() {
    System.out.println("Hello, I am " + this.name + " and I have a GPA of " + this.gpa + " GPA.");
  }
}

// App with main method
public class App {

  public static void main(String[] args) {

    Student jim = new Student();
    jim.setName("Jim");
    jim.setGpa(2.75);

    Student callie = new Student();
    callie.setName("Callie");
    callie.setGpa(3.9);

    jim.greet();
    callie.greet();
  }
}
```
{% endtab %}
{% endtabs %}

After this activity, check out this video for further explanation!

{% embed url="https://youtu.be/gZNrpRryGJw" %}

