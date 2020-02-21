# Testing Exceptions

* In Java, good API design includes making decisions about Exceptions
* This includes deciding what Exceptions should be thrown in what scenario
* Since throwing an Exception can be defined as expected behavior, f.ex. expecting to throw an Exception when we divide by zero, we need to be able to test for these Exceptions.

You can test for an exception using the expected value in the `@Test` annotation. 

```java
import org.junit.Before;
import org.junit.Test;

import static org.junit.Assert.assertEquals;

public class TestSimpleCalc {

    SimpleCalc calc;

    @Before
    public void setUp() {
        calc = new SimpleCalc();
    }

    @Test
    public void shouldPerformSimpleIntegerDivision() {
        assertEquals(3, calc.divide(15,5));
        assertEquals(-2, calc.divide(9,-4));
        assertEquals(-5, calc.divide(-11,2));
        assertEquals(4, calc.divide(-31,-7));
    }

    @Test(expected = IllegalArgumentException.class)
    public void shouldThrowWithZeroDenominator() {
        calc.divide(10, 0);
    }
}
```

With the tests written, write the code to pass the tests.

```java
public class SimpleCalc {
    public int divide(int numerator, int denominator) {
        if(denominator == 0) {
            throw new IllegalArgumentException("Denominator cannot be zero");
        }

        return numerator / denominator;
    }
}
```

