---
description: Safely accessing properties from outside the class.
---

# Getters & Setters

When we create public properties \(a.k.a. variables\) in our class, we're allowing any other class to create an object of that type and directly manipulate the properties. Take a moment and think about why this might be bad? 

Let's go back to our video game. Each lion has a speed. Suppose lions get faster the longer they live, but you want to enforce a maximum speed so that the game doesn't become unbeatable at some point due to lions flying around at the speed of light. 

If you make speed public, every other class in your application can manipulate a lion's speed directly and it becomes very difficult to enforce the maximum speed limit. So let's agree, that it's safer to make speed private. The `private` keyword ensures that the speed for a lion can only be accessed directly from inside the Lion class. 

Using the code below, try to create a new Lion in your main method and set its speed. 

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
}
```

Did you find a way to set the speed from the main method? You can't! The `private` keyword locks down access to the Lion properties. 

Now that we've locked down access to `speed`, we need to create a way to safely set speed from another class - this is where getters and setters come in. Create an App and Lion class and run the code below to get an idea of how getters and setters work. 

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public void setSpeed(int speed){
        this.speed = speed;
    }
    
    public int getSpeed(){
        return this.speed;
    }
}
```

```java
public class App {
    public static void main(String[] args){
        Lion carl = new Lion();
        carl.setSpeed(5);
        System.out.println(carl.getSpeed());
    }
}
```

Let's cover a few key points: 

* getters and setters are just public methods in a class that allow controlled access to private variables. 
* the `this` keyword is used to differentiate between the speed variable created at the class-level and the one locally created by the parameter. `this.speed = speed` means, this Lion's speed should be assigned the value of the `speed` parameter. 
* Naming conventions dictate that getters begin with the word `get` and setters begin with the word `set` followed by the variable name. 

{% tabs %}
{% tab title="Activity " %}
We used getters and setters to create controlled access to the speed variable, but we haven't implemented any control. The whole idea was to manage how high the lion speed could be set, but we haven't done that yet. 

Alter the `setSpeed` method below to create a maximum speed of 55. If the method is passed in a speed equal to or below 55, set the lion's speed to the passed in speed. If the method is passed a speed  above 55, set the speed to 55. 

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public void setSpeed(int speed){
        this.speed = speed;
    }
    
    public int getSpeed(){
        return this.speed;
    }
}
```
{% endtab %}

{% tab title="Solution" %}
```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public void setSpeed(int speed){
        if (speed > 55 ){
            this.speed = 55;
        } else {
            this.speed = speed;
        }   
    }
    
    public int getSpeed(){
        return this.speed;
    }
}
```

```java
public class App {
    public static void main(String[] args){
        Lion carl = new Lion();
        carl.setSpeed(65);
        System.out.println(carl.getSpeed());
    }
}
```
{% endtab %}
{% endtabs %}

{% embed url="https://youtu.be/X78EDpbI26w" %}

