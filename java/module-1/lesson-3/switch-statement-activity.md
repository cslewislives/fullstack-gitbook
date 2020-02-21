# Switch Statement - Activity

![Days of the Week](../../../.gitbook/assets/image%20%2821%29.png)

Using the construct code found in the **Switch Statement** explanation, attempt the DaysOfTheWeek activity detailed below. 

{% tabs %}
{% tab title="DayOfTheWeek Instructions" %}
In this activity you will be prompting the user to input an integer between 1 and 7 inclusive. You will be evaluating this input against the case values in a switch statement to output the day of the week that corresponds to that value. For this activity, the number 1 will equate to Monday. The default statement will advise the user that they did not input a correct value. 

* Initiate a project with the package `com.company` and a Java class called `Weekday`. 
* Inside your main method, initiate a scanner that takes in an integer from 1 to 7 inclusive. 
* You will need to ask the user to input the value you are expecting to evaluate.

{% hint style="info" %}
The user input will need to be stored in a variable that will then be used as the **expression** in your switch statement. 
{% endhint %}

* Create your switch statement to evaluate the user-input variable \(the **expression**\) against the **case** values. 
  * As stated above, expression 1 will equal an output of "Monday". The rest of the days can be built out from here. 
* The default statement will inform the user to input a valid number. 

This activity involves a lot of the information you have learned on day 2 and this early part of day 3. Challenge yourself to write as much of the code as you can before reviewing the solution file. 

Feel free to reference the material in this Gitbook or use Google to help you code the solution. 
{% endtab %}

{% tab title="Solution" %}
```java
package com.company;

import java.util.Scanner;

public class Weekday {

    public static void main(String[] args) {

        Scanner myScanner = new Scanner(System.in);

        System.out.println("Please enter a number between 1 and 7 inclusive: ");
        String userInput = myScanner.nextLine();

        // Convert userInput into an int
        int userDay = Integer.parseInt(userInput);

        // Conver userDay into a day of the week and print it out to the screen
        switch (userDay) {
            case 1:
                System.out.println("Monday");
                break;
            case 2:
                System.out.println("Tuesday");
                break;
            case 3:
                System.out.println("Wednesday");
                break;
            case 4:
                System.out.println("Thursday");
                break;
            case 5:
                System.out.println("Friday");
                break;
            case 6:
                System.out.println("Saturday");
                break;
            case 7:
                System.out.println("Sunday");
                break;
            default:
                System.out.println("You entered an incorrect number!!!");
        }
    }
}
```
{% endtab %}
{% endtabs %}

