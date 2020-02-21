# Unit Tests

The focus of this lesson will be on **Unit Tests.** Writing tests takes time and you may be tempted to skip it but we really can't stress enough how important it is, testing can save you in so many ways. 

### JUnit 

For this course we will be using JUnit as our Unit testing framework. We will need to add the dependency to our projects moving forward.

Open a New Project in IntelliJ called **Calculator** and add the following dependency to the POM file:

```markup
<dependencies>
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.12</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

### Calculator

In that project under the main java folder create a class called `Calculator` and add the following code:

```java
public class Calculator{
    public int add(int a, int b){
          return 0;
    }
}
```

Next under the **test** java folder create a class called `CalculatorTest` and add the following code:

{% hint style="info" %}
Make sure that the path to the test class is the exact same as the path to your `Calculator` class. Ex: `com.company.Calculator` and `com.company.CalculatorTest`
{% endhint %}

```java
public class CalculatorTest{
    @Test
    public void shouldAddTwoIntegers() {
        Calculator calc = new Calculator();
        assertEquals(3, calc.add(1, 2));
    }
}
```

**Notice:** the annotation we used to denote that this class is a test. It's as easy as `@Test`! Otherwise this is a method like any other.

Once you have added the above code go ahead and run this test. You should see the following:

![](../../../.gitbook/assets/image%20%2814%29.png)

This means that the test failed. We can see that we expected a return value of `3` but instead we received `0`. Just through running our test we are able to see what is happening in our code right away.

So how can we fix our code from before? Notice in our `Calculator` class the `return 0;`. If our class is a calculator it's not very helpful if it only returns `0`! Let's refactor it and try the test again.

```java
public class Calculator{
    public int add(int a, int b){
          return a + b;
    }
}
```

We should now see the following:

![](../../../.gitbook/assets/image%20%2899%29.png)

We now see that our test has passed and our code works the way we want!

### Testing for Multiple Inputs

Despite the fact that our test passed we are not done. The issue is that we are only testing for **one** type of input, positive integers, but the way our class is set up we can take any integer. Therefore, we need to test for both.

Tests should be as concise as possible, if we test too many things inside of one test method and something breaks, it is much harder to find the cause. **Remember** to break things down as much as possible.

After we add the new case our code should look like the following:

```java
public class CalculatorTest{
   @Test
    public void shouldAddTwoPositiveIntegers() {
        Calculator calc = new Calculator();
        assertEquals(3, calc.add(1, 2));
    }
    
    @Test
    public void shouldAddTwoNegativeIntegers() {
        Calculator calc = new Calculator();
        assertEquals(-5 ,calc.add(-1, -4));
    }
}
```

{% hint style="info" %}
**Notice:** Our original test case has been renamed. Test method names should be as descriptive as possible.
{% endhint %}

After running our test we should see:

![](../../../.gitbook/assets/image%20%2875%29.png)

Both of our tests have passed! We now know that our calculator works for each type of input.

### @Before

When writing multiple tests we can make our them more DRY \(Don't Repeat Yourself\) be adding the `@Before` annotation. This will allow us to do some setup **before** our tests run.

After adding the `@Before` annotation our code should now look like this:

```java
public class CalculatorTest{
    Calculator calc;
    @Before
    public void setUp() {
        calc = new Calculator();
    }

    @Test
    public void shouldAddTwoPositiveIntegers() {
        assertEquals(3, calc.add(1, 2));
    }

    @Test
    public void shouldAddTwoNegativeIntegers() {
        assertEquals(-5, calc.add(-1, -4));
    }
}
```

Much cleaner!

