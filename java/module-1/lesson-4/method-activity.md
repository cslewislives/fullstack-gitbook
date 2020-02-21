# Method - Activity

![Method Overloading](../../../.gitbook/assets/image%20%2871%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
1. Create a new IntelliJ Project and add a main method. 
2. Create a method called subtract that takes in two integers and returns an integer.
3. In the same project, create another method called subtract that takes in two doubles and returns a double. 
4. Create a final method called subtract that takes one double and one integer and returns a double. 
5. Call the subtract method with two doubles. Which one is called? 
6. Provide the correct parameters to call the remaining methods.
{% endtab %}

{% tab title="Solution" %}
```java
public class App {
    
    public static void main(String[] args){
        int num1 = 1; 
        int num2 = 2; 
        double num3 = 5;
        double num4 = 7; 
        
        //calls the first method
        subtract(num1, num2);
        
        //calls the second method
        subtract(num3, num4);
        
        //calls the third method
        subtract(num1, num4);
    }
    
    public static int subtract(int a, int b){
        return a - b; 
    } 
    
    public static double subtract(double a, double b){
        return a - b; 
    } 
    
    public static double subtract(int a, double b){
        return a - b; 
    } 
}
```
{% endtab %}
{% endtabs %}

{% hint style="danger" %}
Defining multiple methods with the same name but different parameter lists is called **Method Overloading**. We'll see this again later. 
{% endhint %}

