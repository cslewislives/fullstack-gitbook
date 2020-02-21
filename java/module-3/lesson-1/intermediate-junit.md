# Intermediate JUnit



After looking through the JUnit docs on your own here are a few useful annotations and methods that JUnit offers. We will be using these in the future. 

* `@Before` - Code to run before each test. Generally set up, variable creation, constructor calls, etc.
* `@BeforeClass` - Code to run once before all tests.
* `@AfterClass` - Code to run after all tests. Generally used to close DB connections, kill stubs, delete files created in testing, etc.
* `AssertArrayEquals` - Checks the equivalence of values and order in an array.
* `AssertEquals(double expected, double actual, double delta)` - Checks the equality of 2 doubles to within a defined margin of error
* `AssertThat`- Extends the functionality of JUnit considerably. We will have further reading on this later.

### TDD Practice Activity

Follow the instructions below to the best of your ability before taking a look at the solutions.

{% tabs %}
{% tab title="Instructions" %}
Goals:

* Write tests to satisfy the requirements below.
* Then implement the code to pass the tests.

Your requirements state that you need a Physics library with the following functionality

* All numbers are doubles
* `calculateForce` which returns the product of mass and acceleration
* `calculateVelocity` which returns `distance2` minus `distance1` divided by `time2` minus `time1`.
* `calculateMass` which returns weight divided by gravity
* `calculateAcceleration` which returns `velocity2` minus `velocity1` divided by `time2` minus `time1`.
{% endtab %}

{% tab title="Solution" %}

{% endtab %}
{% endtabs %}

