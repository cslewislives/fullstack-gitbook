# I/O - Activity

![Input/Output](../../../.gitbook/assets/image%20%2827%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.  

{% tabs %}
{% tab title="Instructions" %}
1. Prompt the user to input their least favorite food. 
2. Store the input value in a variable called `leastFavFood`.
3. Print \`You hate \[insert leastFavFood here\].

For example, if the user types in `pizza` print `You hate pizza`.
{% endtab %}

{% tab title="Solution Code" %}
```java
public class App {
    public static void main(String args[]){
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter your least favorite food");
        String input = scanner.nextLine();
        
        System.out.println("You hate " + input);
    }
}
```
{% endtab %}
{% endtabs %}

