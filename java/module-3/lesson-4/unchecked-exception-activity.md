# Unchecked Exception - Activity

![Unchecked Exception](../../../.gitbook/assets/image%20%2835%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
1. Run the provided code using a numeric input. The program should run successfully.
2. Run the provided code using a non-numeric input \(like your name\). The program should NOT run successfully.
3. Using the try/catch syntax that you saw in the first example, try to figure out how to catch this error and print "You must type in a number"

```java
package com.company.exceptions;

import java.util.Scanner;

public class App3 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String userInput;
        int number;

        do {
            System.out.println("Please enter a number between 1 and 10");
            userInput = scanner.nextLine();
            number = Integer.parseInt(userInput);
        } while(number < 1 || number > 10);

        System.out.println("Thanks for playing - you chose: " + number);
    }
}
```
{% endtab %}

{% tab title="Solution Code" %}
```java
package com.company.exceptions;

import java.util.Scanner;

public class App4 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String userInput = "";
        int number = 0;

        do {
            try {
                System.out.println("Please enter a number between 1 and 10");
                userInput = scanner.nextLine();
                number = Integer.parseInt(userInput);
            } catch (NumberFormatException e) {
                System.out.println("You must type in a number. You typed in: " + userInput);
            }
        } while(number < 1 || number > 10);

        System.out.println("Thanks for playing - you chose: " + number);
    }
}
```
{% endtab %}
{% endtabs %}

{% embed url="https://youtu.be/pfeSHZbNM-o" %}



