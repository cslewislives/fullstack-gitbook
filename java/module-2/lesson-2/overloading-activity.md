# Overloading - Activity

![Overloading](../../../.gitbook/assets/image%20%2879%29.png)

{% tabs %}
{% tab title="Instructions" %}
1. Create a class called `Main` with a `main` method. 
2. In the `Main` class, create 3 methods called `greet` with no return value. 
3. The first `greet` method should take no parameters and print out `"Hello!"`.
4. The second  `greet` method should take a `String` parameter and print out `"Hello <parameter>!"`. 
5. The third `greet` method should take an `int` parameter and print out `"Hello!"` the number of times indicated by the parameter. 
6. Call each of the greet methods.  
{% endtab %}

{% tab title="Solution" %}
```java
public class Main {
    public static void main(String[] args){
        greet();
        greet("Paola");
        greet(4);
    }
    
    public static void greet(){
        System.out.println("Hello!");
    }
    
    public static void greet(String name){
        System.out.println("Hello " + name + "!");
    }
    
    public static void greet(int times){
        for (int i = 0; i < times; i++){
            System.out.println("Hello!");
        }
    }
}
```
{% endtab %}
{% endtabs %}

