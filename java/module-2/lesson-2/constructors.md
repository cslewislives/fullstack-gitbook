---
description: A method for constructing new objects.
---

# Constructors

A constructor is a special method that is called when you instantiate a class \(remember that **an instantiated class is an object**—we can't emphasize this point enough\).

Constructors are used to initialize \(that is set the initial state of\) the object being created from the class.

There are some restrictions on constructors \(i.e., they are not general-purpose methods\):

* A constructor must have the same name as the class that contains it. For example, if we have a class called `Lion`, the constructor must be called `Lion()`.
* Like general-purpose methods, constructors can have zero or more parameters.
* Unlike general-purpose methods, constructors have no return type \(not even void!\).
* A class can have more than one constructor \(we'll cover this when we get to method overloading\).
* If you don't supply a constructor for your class, the compiler will supply one \(called the default constructor\). This default constructor has no parameters and contains no code in its body.

You can see constructors in action below in the `Lion` class.

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public Lion(String nameIn, int speedIn, int weightIn) {
        this.name = nameIn;
        this.speed = speedIn;
        this.weight = weightIn;
    }
    
    public int getSpeed(){
        return this.speed;
    }
}
```

```java
public class App {
    public static void main(String[] args){
        Lion carl = new Lion("Carlsberg", 40, 200);
        System.out.println(carl.getSpeed());
    }
}
```

{% embed url="https://youtu.be/vb\_SMYIGSOg" %}

