# Composition - Activity

![Gift Card](../../../.gitbook/assets/image%20%2868%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
Solve the following problem:

* We want to add a gift card to our `Account` class. Implement a solution.
* Some prompts to think about:
  * What kind of information do we need about a gift card?
  * How will this relate to the `Account` class?
{% endtab %}

{% tab title="Solution Code" %}
* Note that the original amount is a read-only property and does not have a setter
* Some examples of additional properties:
  * Purchase Date
  * Expiration Date
* In our account class, we add a GiftCard property and a getter/setter just like with our Address properties

```java
package com.company.composition;

public class GiftCard {

    private String cardNumber;
    private float originalAmount;
    private float currentBalance;

    public GiftCard(String cardNumber, float originalAmount) {
        this.cardNumber = cardNumber;
        this.originalAmount = originalAmount;
        this.currentBalance = originalAmount;
    }

    public String getCardNumber() {
        return cardNumber;
    }

    public float getOriginalAmount() {
        return originalAmount;
    }

    public float getCurrentBalance() {
        return currentBalance;
    }

    public void setCurrentBalance(float currentBalance) {
        this.currentBalance = currentBalance;
    }
}

// ============================================
package com.company.composition;

public class BetterAccount {

    private String firstName;
    private String lastName;
    private String username;

    private Address homeAddress;
    private Address shippingAddress;
    
    private GiftCard giftCard;

    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public Address getHomeAddress() {
        return homeAddress;
    }

    public void setHomeAddress(Address homeAddress) {
        this.homeAddress = homeAddress;
    }

    public Address getShippingAddress() {
        return shippingAddress;
    }

    public void setShippingAddress(Address shippingAddress) {
        this.shippingAddress = shippingAddress;
    }

    public GiftCard getGiftCard() {
        return giftCard;
    }

    public void setGiftCard(GiftCard giftCard) {
        this.giftCard = giftCard;
    }
}
```
{% endtab %}
{% endtabs %}

