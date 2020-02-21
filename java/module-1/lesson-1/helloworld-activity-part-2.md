---
description: Create and run your first Java program.
---

# HelloWorld! - Activity Part 2

## Writing the Program

Now that the IntelliJ project has been created, we are going to write the code to generate the program. 

Watch the second part of the instructional video and then follow along using the steps listed below. 

{% embed url="https://www.youtube.com/watch?time\_continue=12&v=rGEl64cjMlA" %}

### Create the Hello Class

Java is a **high-ceremony language**. It will take a lot of work to get "Hello World!" to display on the screen. We will start by by creating the **Hello** class. 

Inside the IntelliJ projected that you created:

* Navigate to the `src/main/java` file  in the Project pane. 
* Right-click on the `java` folder and select `New` and then `Java Class`. 
* Inside the Name textbox of the Create New Class pane, type  `com.company.Hello`.   
  * In this case, 'com' and 'company' are packages that help to organize the file structure of your code. 
  * It is  customary for the base package to be the reverse of your organization's main domain name. 
* Click Ok.

Note that the `public class Hello{}` was created. Classes are containers \(code blocks\). Note that all code blocks begin with open curly braces and end with close curly braces. 

One of the things they can contain is methods, specifically the **main** method.

### Create the Main Method

Methods are a different type of container or code block. Methods contain Java code that does work; they're where the action happens in Java.

Inside the {} \(curly braces\) of the Hello class:

* Write out `public static void main (String[] args){}` and the brackets.
  * The `main` method is a special method that is the entry \(or starting\) point for every Java program. The `main` method must be declared exactly as in the example and it must be contained inside a class.
  * Note that the `main` method is similar to the `Hello` class is some respects \(the access modifier public and the {}\), but it also has some additional information \(static, void, String{} and args\). We will get deeper into those differences further along in our lessons.
* Inside the {} \(curly braces\) of the main method type `System.out.println("Hello, World!!!");`.
  * "System.out.println" is the command that tells the computer to 'print' what is inside the \(\) to the screen. 

At this point your screen should look as follows:

```java
package com.company;

public class Hello {
    public static void main(String[] args) {
        
        System.out.println("Hello, World!!!");
    }
}
```

### Reviewing for Errors

IntelliJ is very helpful when it comes to finding errors. Look in your code for any red error messages and go fix them. This type of review should become a regular part of your coding process. 

### Running the Program

Once all of the errors have been cleaned up, it is time to run your program. 

Right-Click on the one of the green arrows located in the left hand gutter of your program pane and choose `Run Hello.main()`.

After a few seconds, you will notice a new pane open at the bottom of your screen. If your program has complied, you will see "Hello, World!!!" printed in the pane.

{% tabs %}
{% tab title="Code" %}
```java
package com.company;

public class Hello {
    public static void main(String[] args) {
        
        System.out.println("Hello, World!!!");
    }
}
```
{% endtab %}

{% tab title="Output" %}
{% endtabs %}

Congratulations! You have just run your first Java program in IntelliJ. 

