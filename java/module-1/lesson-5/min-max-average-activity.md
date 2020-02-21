# Min, Max, Average - Activity

Min, Max, Average is a code-along activity with the Instructor. Watch and code, pausing the video where necessary.  

{% embed url="https://youtu.be/VrnOesBS-ko" %}

{% tabs %}
{% tab title="Min, Max Average Instructions" %}
The Min, Max, Average activity begins by having the user input 10 numbers into an array. Once the array has been established, write the code to determine the number with the minimum value, the number with the maximum value and then the average value of all of the numbers. 

This activity will incorporate all of the information you have learned in the course  
{% endtab %}

{% tab title="Min Max Average " %}
```java
package com.company;

import java.util.Scanner;

public class App {

    public static void main(String[] args) {

        // Set up the scanner and variables
        Scanner scanner = new Scanner(System.in);
        int[] numbers = new int[10];
        String stringIn;
        int min;
        int max;
        int sum = 0;
        double avg;

        // Read in 10 ints
        for (int i = 0; i < numbers.length; i++) {

            System.out.println("Please enter a number:");
            stringIn = scanner.nextLine();
            numbers[i] = Integer.parseInt(stringIn);
        }

        // Calculate min
        min = numbers[0];
        for (int i = 0; i < numbers.length; i++) {
            if (numbers[i] < min) {
                min = numbers[i];
            }
        }

        // Calculate max
        max = numbers[0];
        for (int i = 0; i < numbers.length; i++) {
            if (numbers[i] > max) {
                max = numbers[i];
            }
        }

        // Calculate average
        for (int i = 0; i < numbers.length; i++) {
            sum += numbers[i];
        }

        avg = sum/(double)numbers.length;

        System.out.println("Minimum value: " + min);
        System.out.println("Maximum value: " + max);
        System.out.println("Sum: " + sum);
        System.out.println("Average: " + avg);
    }

}
```
{% endtab %}
{% endtabs %}

