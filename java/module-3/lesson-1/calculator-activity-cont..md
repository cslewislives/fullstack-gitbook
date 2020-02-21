# Calculator - Activity Cont.

![Calculator Cont.](../../../.gitbook/assets/image%20%2856%29.png)

Follow the instructions below to the best of your ability before taking a look at the solutions. If you have any questions feel free to post them in Slack! 

{% tabs %}
{% tab title="Instructions" %}
**Goals:** 

* In your Calculator project:
* Add failing tests for a `sumArrays` method. `sumArrays` should take two arrays and sum all the numbers in both arrays. 
* Add a failing test for `arrayify`. `arrayify` should take in two integers. It should create an array the length of the first integer that contains consecutive integers starting at the second integer. For example, `arrayify(3,5)` returns `[5,6,7]`. 
* Once you have failing tests with a sufficient number of equivalence classes, write code to pass the tests. 

**Hint:** You'll need to use `assertArrayEquals` to compare arrays.
{% endtab %}

{% tab title="Solution" %}
`CalculatorTest` class:

```java
@Test
public void shouldSumArrays() {

    int[] testArr1 = {1,2,3,4};
    int[] testArr2 = {5};
    int[] testArr3 = {0, 24, -3, 50, 104, -35};

    assertEquals(15, calc.sumArrays(testArr1, testArr2));
    assertEquals(145, calc.sumArrays(testArr2, testArr3));
    assertEquals(150, calc.sumArrays(testArr1, testArr3));
}

@Test
public void shouldArrayify() {
    int[] output1 = {5,6,7};
    int[] output2 = {-2, -1, 0, 1, 2, 3};
    int[] output3 = {104};

    assertArrayEquals(output1, calc.arrayify(3,5));
    assertArrayEquals(output2, calc.arrayify(6,-2));
    assertArrayEquals(output3, calc.arrayify(1,104));

}
```

`Calculator` class:

```java
public int sumArrays(int[] arr1, int[] arr2) {
    int sum = 0;

    for(int num : arr1) {
        sum += num;
    }

    for(int num : arr2) {
        sum += num;
    }

    return sum;
}

public int[] arrayify(int size, int start) {
    int[] out = new int[size];

    for(int i = 0; i < size; i++) {
        out[i] = start + i;
    }

    return out;
}
```
{% endtab %}
{% endtabs %}

 

