# Testing Exceptions - Activity

![Testing Exceptions](../../../.gitbook/assets/image%20%2836%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
Goals:

* Write tests for a method that takes an array of arrays and returns an array with the average of each inner array
* The method should throw an `IllegalArgumentException` if any of the numbers are negative.
* After you have failing tests, implement the method

**Input:** `[ [1,2,3] , [4, 4, 4], [2, 4, 6] ]` **Output:** `[2, 4, 4]`
{% endtab %}

{% tab title="Solution - ArrayFunTest" %}
```java
import org.junit.Before;
import org.junit.Test;

import static org.junit.Assert.assertArrayEquals;

public class ArrayFunTest {

    ArrayFun tester;

    int[][] testArr1;
    int[][] testArr2;
    int[][] testArr3;

    int[][] testArr4;

    @Before
    public void setUp() {
        tester = new ArrayFun();

        testArr1 = new int[][] {
                {1,2,3},
                {4,5,6},
                {7,8,9},
                {10,11,12}
        };

        testArr2 = new int[][] {
                {6, 4, 10, 12},
                {1, 90, 50, 43}
        };

        testArr3 = new int[][] {
                {1},
                {4},
                {0}
        };

        testArr4 = new int[][] {
                {1,2,3},
                {4,5,-6},
                {7,8,9}
        };

    }

    @Test
    public void shouldAverageArrays(){
        assertArrayEquals(new int[] {2,5,8,11}, tester.averageArrays(testArr1));
        assertArrayEquals(new int[] {8,46}, tester.averageArrays(testArr2));
        assertArrayEquals(new int[] {1,4,0}, tester.averageArrays(testArr3));
    }

    @Test(expected= IllegalArgumentException.class)
    public void shouldThrowWithNegative(){
        tester.averageArrays(testArr4);
    }
}
```
{% endtab %}

{% tab title="Solution - ArrayFun" %}
```java
public class ArrayFun {

    public int[] averageArrays(int[][] arr) {
        int[] averages = new int[arr.length];

        for(int i = 0; i < arr.length; i++) {
            int[] inner = arr[i];
            int avg = 0;
            for (int num : inner) {
                if (num < 0) {
                  throw new IllegalArgumentException("Numbers cannot be negative");
                }

                avg += num;
            }
            avg /= inner.length;
            averages[i] = avg;
        }

        return averages;
    }
}
```
{% endtab %}
{% endtabs %}

