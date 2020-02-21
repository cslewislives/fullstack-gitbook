# Reusable Class - Activity

![Address Class](../../../.gitbook/assets/image%20%2892%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt.

{% tabs %}
{% tab title="Instructions" %}
Create a new class called `Address` which has the following properties, along with the associated getters and setters.

* `String street`
* `String city`
* `String state`
* `String zipcode`
{% endtab %}

{% tab title="Solution Code" %}
```java
package com.company.composition;

public class Address {

    private String street;
    private String city;
    private String state;
    private String zipcode;

    public String getStreet() {
        return street;
    }

    public void setStreet(String street) {
        this.street = street;
    }

    public String getCity() {
        return city;
    }

    public void setCity(String city) {
        this.city = city;
    }

    public String getState() {
        return state;
    }

    public void setState(String state) {
        this.state = state;
    }

    public String getZipcode() {
        return zipcode;
    }

    public void setZipcode(String zipcode) {
        this.zipcode = zipcode;
    }
}
```
{% endtab %}
{% endtabs %}

