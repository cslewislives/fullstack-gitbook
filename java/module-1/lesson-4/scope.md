---
description: Where can I use this thing?
---

# Scope

The scope of a variable basically means where it can be used. Java variables are block-scoped. A block is a set of curly braces. This means each variable is available only within the nearest set of curly braces in which it was defined with one exception noted with an asterisk below.

**Class-level variables.**

These variables are declared inside of a class \(yet outside of any method\) and can be accessed anywhere inside the class.

\*Depending on their access modifier, these variables may be accessible in the entire class and some other classes. We'll save this discussion for another day - just file this tidbit away for now. 

**Method-level variables**

These variables are declared inside a method and are not usable outside of it.

**Loop variables**

These variables are declared inside a set of curly braces like a loop or a conditional and are not usable outside of it.

Go ahead and try to run the 2 sets of code below in IntelliJ:

```java
public class App {
    static int classLevel = 9; 
    
    public static void main(String[] args){
        sampleMethod();
        System.out.println(classLevel); 
    }
    
    public static void sampleMethod(){
        System.out.println(classLevel);
    } 
}
```

```java
public class App {
    
    public static void main(String[] args){
        sampleMethod();
        System.out.println(classLevel); 
    }
    
    public static void sampleMethod(){
        int classLevel = 9; 
        System.out.println(classLevel);
    } 
}
```

Now, before we move onto an activity, let's quickly recap what we've covered so far in this lesson:

{% embed url="https://youtu.be/Ajil99dntsg" %}



