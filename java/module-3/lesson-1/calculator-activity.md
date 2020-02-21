# Calculator - Activity

![Calculator](../../../.gitbook/assets/image%20%2850%29.png)

Follow the instructions below to the best of your ability before taking a look at the solutions. If you have any questions feel free to post them in Slack! 

{% tabs %}
{% tab title="Instructions" %}
Goals:

* Create a class called Calculator.
* In the class create a method called divide that takes two integers.
* Divide should return the integer that results from dividing the 2 integers.
* It should return 0 if the numerator or denominator is 0\*
* Write unit tests to test your divide method

_\*Yes, this is bad math, but clients ask for weird things._
{% endtab %}

{% tab title="Solution" %}
`Calculator` class:

```java
public class Calculator {

    public int divide(int a, int b) {
        if ( b == 0 ) {
            return 0;
        }

        return a/b;
    }
}
```

`CalculatorTest` class:

```java
import org.junit.Before;
import org.junit.Test;

import static org.junit.Assert.assertEquals;

public class CalculatorTest {
    Calculator calc;

    @Before
    public void setUp() {
        calc = new Calculator();
    }

    @Test
    public void shouldDividePositives() {

        assertEquals(3, calc.divide(6,2));
        assertEquals(2, calc.divide(80, 39));
        assertEquals(1, calc.divide(105, 100));
    }

    @Test
    public void shouldDivideNegatives() {

        assertEquals(3, calc.divide(-6,-2));
        assertEquals(2, calc.divide(-80, -39));
        assertEquals(1, calc.divide(-105, -100));
    }

    @Test
    public void shouldDivideBothPosAndNeg() {
        assertEquals(-3, calc.divide(6,-2));
        assertEquals(-2, calc.divide(-80, 39));
        assertEquals(-1, calc.divide(105, -100));
    }

    @Test
    public void shouldReturnZero() {
        assertEquals(0, calc.divide(0,0));
        assertEquals(0, calc.divide(0, 1));
        assertEquals(0, calc.divide(105, 0));
    }
}
```
{% endtab %}
{% endtabs %}

 

