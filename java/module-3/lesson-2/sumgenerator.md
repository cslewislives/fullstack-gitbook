---
description: sum method walk-through
---

# SumGenerator

We are going to implement a helper class called `SumGenerator`. This class contains the following methods:

* `sum` - which takes in an integer, `n`, and returns the sum from 1 to n, inclusive.
* `evenSum` - which takes in an integer, `n`, and returns the sum of the even integers from 1 to n, inclusive.
* `oddSum` - which takes in an integer, `n`, and returns the sum of the odd integers from 1 to n, inclusive.

We will show you how to write the tests and code out the `sum` method. Then you will complete the `evenSum` and `oddSum` on your own next.

{% hint style="info" %}
Run the following code in IntelliJ to get a better understanding of how this works.
{% endhint %}

{% tabs %}
{% tab title="SumGeneratorTests" %}
```java
public class SumGeneratorTests {

    private SumGenerator sumGen;

    @Before
    public void setUp() {
        sumGen = new SumGenerator();
    }

    @Test
    public void shouldSumFromOneToN() {

        assertEquals(10, sumGen.sum(4));
        assertEquals(0, sumGen.sum(0));
        assertEquals(21, sumGen.sum(6));
    }
}
```
{% endtab %}
{% endtabs %}

