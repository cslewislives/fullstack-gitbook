# TDD

Earlier we discussed that writing tests first was a powerful way to plan and think through your code before you write, which leads to higher quality code. This style of coding is known as **Test Driven Development** **\(TDD\).** 

TDD is a highly encouraged way to code, and for this course moving forward it is **required**. 

{% hint style="warning" %}
From this point on, you **MUST** write your tests first
{% endhint %}

### Best Practice

When it comes to TDD there are some best practices involved, as with all coding. In this course we will be using the **Red Green Refactor** method when writing our tests.

![](../../../.gitbook/assets/image%20%2891%29.png)

#### Red Green Refactor

* Begin by writing failing tests
  * Think carefully through equivalence classes as you design your tests. 
* Write the code to pass all tests
* Refactor the code and tests
  * **NOT AT THE SAME TIME**
* Rinse and repeat as needed

### TV Example

Let's put this into action! In IntelliJ create a new project called TV. Create the following `TVTest` class:

```java
public class TVTest{

  TV tele;
  @Before
  public void setUp() {
      tele = new TV(15);
  }
    
  @Test
  public void shouldTurnOn() {
    tele.on();
    assertTrue(tele.isOn());
  }

  @Test
  public void shouldTurnOff() {
    tele.off();
    assertFalse(tele.isOn());
  }

  @Test
  public void shouldChangeChannel() {
    tele.increaseChannel();
    tele.increaseChannel();
    assertEquals(17, tele.getChannel());
  }
}
```

**Notice:** We haven't coded anything other than this test class. Yet we know that we want to have a TV object that should Turn On, Turn Off, and Change Channel. Doesn't this now make it easy to write what we need?

Of course when we run this these tests will fail, and they **should**. Now go ahead and write in enough code to make these tests pass. While you're at it can you come up with other test cases for a TV?

