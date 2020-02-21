# Classes and Objects - Activity

![Classes and Objects Activity](../../../.gitbook/assets/image%20%28101%29.png)

{% tabs %}
{% tab title="Instructions" %}
1. Using the code below as a starter, create getters and setters for name and weight. 
2. Create a class called `App` and in it create a `main` method. 
3. Inside the `main` method create a lion object and set it's weight and name. 
4. Print the name and weight using the getters.  

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public Lion(String name, int speed, int weight){
        this.name = name; 
        this.speed = speed; 
        this.weight = weight; 
    }
    
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
public class App {
    public static void main(String[] args){
        Lion carl = new Lion("carl", 5, 55);
        carl.setWeight(550);
        carl.setName("Beau");
        System.out.println(carl.getName() + " weighs " + carl.getWeight());
    }
}
```

```java
public class Lion {
    private String name;
    private int speed;
    private int weight; 
    
    public Lion(String name, int speed, int weight){
        this.name = name; 
        this.speed = speed; 
        this.weight = weight; 
    }
    
    public void setSpeed(int speed){
        this.speed = speed;
    }
    
    public int getSpeed(){
        return this.speed;
    }
    
    public void setWeight(int weight){
        this.weight = weight;
    }
    
    public int getWeight(){
        return this.weight;
    }
    
    public void setName(String name){
        this.name = name;
    }
    
    public String getName(){
        return this.name;
    }
}
```
{% endtab %}
{% endtabs %}

