# Inheritance with Interfaces - Activity

![Implement SecureStorable](../../../.gitbook/assets/image%20%2842%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt. 

{% tabs %}
{% tab title="Instructions" %}
1. Create a new class called `SensitiveDataFile` which use the `SecureStorable` interface.
2. Implement all necessary methods.

{% hint style="info" %}
Reference the following code from for a list of methods.
{% endhint %}

```java
package com.company.interfaces;

public interface Storable {

    public void storeData();

    public void retrieveData();

    public default void sillyMethod () {
        // code here
    }
}

// =================================

package com.company.interfaces;

public interface SecureStorable extends Storable {

    public void encryptData();

    public void decryptData();
}
```
{% endtab %}

{% tab title="Solution Code" %}
```java
package com.company.interfaces;

public class SensitiveDataFile implements SecureStorable {


    public void encryptData() {
        // code here
    }

    public void decryptData() {
        // code here
    }

    public void storeData() {
        // code here
    }

    public void retrieveData() {
        // code here
    }
}
```

* Since the interface `SecureStorable` inherited the methods from `Storable` , all the methods from `Storable` and `SecureStorable` must be implemented.
* Remember we **don't** have to provide an implementation for the default method in `Storable`.
{% endtab %}
{% endtabs %}

