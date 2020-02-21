---
description: A look at a simple interface declaration.
---

# Interface Declaration

Like a class, an interface must be declared. Interface declaration looks a lot like class declaration:

```java
public interface Storable {
    public void storeData();
    public void retrieveData();
}
```

* To create this interface in IntelliJ, we would follow the same steps as creating a class. 
  * We would right-click the Java folder and click create new class. 
  * In the next menu we would type in com.company.interfaces.Storable \(this puts the interface in the com.company.interfaces package\) for the name and select interface from the drop down menu below. 
* The code above represents our Storable interface. Classes that implement this interface must have both a storeData\(\) and retrieveData\(\) method.
* Instead of the class keyword, we use the interface keyword.
* Methods declared in the interface do not have a body; we just follow the definition with a semicolon.
* This declaration defines the "contract".

{% embed url="https://youtu.be/XIUrl9eRxkI" %}

