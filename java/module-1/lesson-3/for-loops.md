---
description: For loops allow the code to execute a specific number of times.
---

# For Loops

## For Loops

For loops allow for the repetition of code for a **specific** number of times.  

* We **DO** know ahead of time how many of how many times this action will repeat.

In contrast to the While and Do/While loops, For loops do **NOT** depend on a condition to trigger the code execution. 

* Real-world examples:
  * Run 10 laps.
  * Plant 8 flowers.

The code construct and the practical application for a for-loop is as follows. 

```java
   //constuct
   for (initialization; termination; increment) {
	   // repeat a given number of times
   }
   
   //application
  for (int i = 0; i < 4; i++) {
	   System.out.println(i);
   }
   
```

Looking at the application in relation to the construct:

* `int i = 0` is the **initialization**. For this loop, the counter \(i\) will start at 0. 
* `i < 4` is the **termination**. The loop will cease to execute when i is NO LONGER less than 4. 
  * This loop will run 4 times...when i = 0; when i=1; when i=2; and when i=3. 
* `i++` is the **increment**. Every time we cycle through the loop, i will be increased by 1. 
  * `++` is code shorthand for `i = i +1`
  * `--` is code shorthand for `i = i - 1`
  * i  can be incremented by any numerical value. ie `i+=2` will increase i by 2 every loop.

Drop the following code into IntelliJ to see how the for loop works. Adjust the values for the initialization, termination and increment to see how i is effected. 

```java
public class ForLoop {

    public static void main(String[] args) {
    
    for (int i = 0; i < 4; i++) {
	   System.out.println(i);
    }
 }
}
```

{% embed url="https://youtu.be/t\_PQtnyqwu8" %}

