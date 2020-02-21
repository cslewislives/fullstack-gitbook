# Do/While - Activity

![Enter Integer](../../../.gitbook/assets/image%20%2821%29.png)

Using the construct code found in the **While and Do/While Loops** explanation, attempt the EnterInteger activity detailed below. 

{% tabs %}
{% tab title="EnterInteger Instructions" %}
Using a **Do/While** loop, prompt the user to input an integer between 1 and 10 inclusive.  

If the user input is between those values, output a statement that reads \("Great, you chose " + userInt\).

While the user input value is outside the values \(Hint: less than 0 OR greater than 10\), again prompt them to input a value. 

* Remember, all user input is captured as a String. You will need to convert the string into an integer to do correctly evaluate the expression. 
* Like in the Switch statement activity, you will need to initiate a scanner and establish a variable to capture the user input. 

As before, challenge yourself to write as much of the code as you can before reviewing the solution file. 

Feel free to reference the material in this Gitbook or use Google to help you code the solution. 
{% endtab %}

{% tab title="Solution" %}
```java
package com.company;

import java.util.Scanner;

public class EnterInteger {

    public static void main(String[] args) {

        Scanner myScanner = new Scanner(System.in);
        String userInput;
        int userInt;

        do {

            System.out.println("Enter a number between 1 and 10");
            userInput = myScanner.nextLine();
            userInt = Integer.parseInt(userInput);

        } while (userInt < 0 || userInt > 10);

        System.out.println("Great! You chose " + userInt);

    }
}
```
{% endtab %}
{% endtabs %}

