# Operator - Activity

![Arithmetic and Comparison Operators](../../../.gitbook/assets/image%20%2811%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
1. Create a new IntelliJ Project and add a main method. 
2. Create a variable that holds the number of typos you've made today. 
3. Create a new variable that holds the number of things you've learned today. 
4. Create a new variable that holds the quotient of the variable from step 2 and the variable step 3. 
5. Print whether this new number is greater than 5. 
{% endtab %}

{% tab title="Solution" %}
```java
public class App {
    public static void main(String[] args){
        // typos you've made today 
        int typos = 27;
        
        // things you've learned today 
        int learnedThings = 6;
        
        //quotient of the variables 
        int quotient = typos/learnedThings;
        
        //Print whether this new number is greater than 5.
        System.out.println(quotient > 5); 
    }
}
```
{% endtab %}
{% endtabs %}

