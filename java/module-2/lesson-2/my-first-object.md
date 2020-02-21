---
description: Let's instantiate these beasts!!
---

# My First Object

It's time for a concrete example. Let's suppose you are building a video game. In this game a brave monkey is battling a seemingly endless army of lions. The poor monkey evades the lions, pummels them with bananas, and fools them into running into deep holes, but the darn lions keep coming. 

As a game developer, you're going to need to create A LOT of lions. The first step is to create a class \(or blueprint\) from which individual lions can be created. Each lion needs a name, a weight, and speed. At different levels of the game, the weight and speed of the lion will differ. 

```java
public class Lion {
    public String name;
    public int speed;
    public int weight; 
}
```

We can now create lions easily! 

```java
public class App {
    public static void main(String[] args){
        Lion carl = new Lion();
    }
}
```

The `new` key word creates a new lion.

{% tabs %}
{% tab title="Question" %}
What do you think the type of the variable `carl` is?
{% endtab %}

{% tab title="Answer" %}
The type is `Lion`. That's right - `Lion` is now a type! Java has pre-built types like `int`, `boolean`, `String`, and `double` plus a lot of extras from the libraries you import, like `Scanner`. You can define as many new types as you can imagine. Every new class is a new type of variable you can create. 
{% endtab %}
{% endtabs %}

We can access public properties on our `carl` object using the dot operator.

```java
public class App {
    public static void main(String[] args){
        Lion carl = new Lion();
        carl.name = "Carl Lionly Jr";
        System.out.println(carl.name);
    }
}
```

{% hint style="danger" %}
It is generally a bad idea to make all the properties on your class public. In this article, we did this simply for demonstration purposes. We'll explore this more in the next article. 
{% endhint %}

