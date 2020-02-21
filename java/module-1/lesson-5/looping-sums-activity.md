# Looping Sums - Activity

![Looping Sums](../../../.gitbook/assets/image%20%2880%29.png)

In the following activity, you are going to loop through an array of numbers to determine the sum. You will be doing this using both the traditional and the enhanced for loops. 

{% tabs %}
{% tab title="Looping Sums Activity" %}
Utilizing the following arrays, calculate the sum of each. 

* For array nums1, calculate the sum \(sum1\) utilizing the traditional for loop. As you iterate through the loop, display each of the individual elements of the array as well as the changing sum. 

```java
int[] nums1 = {1, 3, 5, 7, 9, 11};
```

* For array nums2, calculate the sum \(sum2\) utilizing the enhanced for loop.  As above, display each of the individual element os the array as well as the changing sum. 

```text
int[] nums2 = {2, -4, 6, -8, 10, -12};
```

You should only need to create one new IntelliJ project to complete this activity. 

As always, you can utilize Google and the prior material to assist. 
{% endtab %}

{% tab title="Looping Sums Solution Code" %}
```java
package com.company;


public class LoopingSums {

    public static void main(String[] args) {

        // Summing using the traditional for loop:


        int[] nums1 = {1, 3, 5, 7, 9, 11};
        int sum1 = 0;

        for (int  i = 0; i < nums1.length; i++) {
            System.out.println("num index position " + i + " is " + nums1[i]);
            sum1 = sum1 + nums1[i];
            System.out.println("The current value of sum1 is: " + sum1);
        }

        System.out.println("The total value of sum1 is: " + sum1);
        System.out.println("=================");

        // Summing using the enhanced for loop:

        int[] nums2 = {2, -4, 6, -8, 10, -12};
        int sum2 = 0;

        for (int num : nums2) {
            System.out.println("The current number being added is: " + num);
            sum2 = sum2 + num;
            System.out.println("The current value of sum2 is: " + sum2);
        }

        System.out.println("The total value of sum2 is: " + sum2);
    }
}
```
{% endtab %}
{% endtabs %}

