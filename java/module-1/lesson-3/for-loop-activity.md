# For Loop Activity

![Print Evens &amp; Print Odds](../../../.gitbook/assets/image%20%2851%29.png)

Using the construct code found in the **For Loops** explanation, attempt the PrintEven activity detailed below.

{% tabs %}
{% tab title="PrintEven & PrintOdds Activities" %}
* Using a **For loop**, create a PrintEven class that outputs all of the even integers between 0 and 20.
* Use any combination of the initialization, termination or increment values to accomplish this task.  
* With that task completed, create a PrintOdd class that outputs all of the odd values within the same integer range. 
* As before, challenge yourself to write as much of the code as you can before reviewing the solution file. 
* Feel free to reference the material in this Gitbook or use Google to help you code the solution. 
{% endtab %}

{% tab title="PrintEven Solution Code" %}
```java
package com.company;

public class PrintEven {

    public static void main(String[] args) {

        for (int i = 0; i < 21; i+=2) {

            System.out.println(i);

        }
    }
}
```
{% endtab %}

{% tab title="PrintOdd Solution Code" %}
```java
package com.company;

public class PrintOdd {

        public static void main(String[] args) {

            for (int i = 1; i < 20; i+=2) {

                System.out.println(i);

            }
        }
    }
```
{% endtab %}
{% endtabs %}

