---
description: Visual representation of the state and behaviors of our classes
---

# UML Diagrams

Before we start creating classes \(or objects\) en mass, it will be helpful to to have some sort of outline for the state and behaviors of our classes. 

One way to visually represent our classes is through the creation of a **UML Diagram.**

Navigate to the website [draw.io](https://about.draw.io/uml-class-diagrams-in-draw-io/)**.** 

* Scroll down to the 'UML class diagram notation `section, and more specifically, 'Classes`. 

![](../../../.gitbook/assets/image%20%2849%29.png)

Tying the text back to the box located on the right side of the image, notice the following:

* The Class name is the type of the new class \(ie Habit\).
* Attributes are the same as properties.
  * They are located in the upper portion of the box.
  * The `+` indicates that they have a public access modifier. A private access modifier is designated with a `-`.
* Operations are the same as behaviors and are expressed as methods.
  * They are located on the bottom half of the box. 
  * Operations, or class **methods** a followed by a \(\). Anything inside the \(\), is a parameter that accompanies that method. 
  * The value to the right of the method colon indicates  a value returned by the method. 

To create a UML Diagram, navigate to this page in [draw.io](https://www.draw.io/) .

* Choose **Device** storage. 
* Click on **Create New Diagram** 
* Type a Filename in the upper textbox. \(ie Student.drawio\)
* Click Create. 
* Select the **UML** palette from the left-hand navigation pane.
* Choose the **Class** diagram \(the 3rd image ****\) and drag it onto the main canvas.
* You can add as many fields \(properties\) as necessitated by the object. 

### Create a UML Diagram

Using draw.io, practice creating a UML diagram using the construct discussed above.

Before beginning the diagram, read the instructions and then think about how the attributes and methods outlined here work together to create the 'Instructor' object \(or class\). 

{% tabs %}
{% tab title="Create a UML Diagram" %}
Using draw.io and the instructions that follow, create a UML diagram. 

* Navigate to [draw.io](https://www.draw.io/)
* Choose **Device** storage. 
* Click on **Create New Diagram** 
* Type a Filename in the upper textbox. \(ie Instructor.drawio\)
* Click Create. 
* Select the **UML** palette from the left-hand navigation pane.
* Choose the **Class** diagram \(the 3rd image ****\) and drag it onto the main canvas.
* Create a UML Diagram for a class called `Instructor`
* This  `Instructor` class has the following properties:
  * `String name`
  * `String subject`
  * `String yearsTenure`
* Additionally, this class the following methods:
  * `increaseTenure` which returns nothing and has no parameters
  * `changeSubject` which returns nothing and has one `String` parameter

You can review the solution image for this diagram on the following tab. 
{% endtab %}

{% tab title="UML Image" %}
![](../../../.gitbook/assets/image%20%2885%29.png)
{% endtab %}
{% endtabs %}





