# Object Equality

What does it mean for two objects to be equal?

### Shallow Equality

![](../../../.gitbook/assets/image%20%2847%29.png)

There are 2 definitions of object equality. The first is that the two variables are actually two references to the same object. This is known as **shallow equality.**

```java
Dog fido = new Dog();
Dog rex = fido;
```

### **Deep Equality**

![](../../../.gitbook/assets/image%20%281%29.png)

The second is that two objects share the same value for all of their properties. This is known as **deep equality.** 

```java
Dog fido = new Dog("brown", 2, "frisbee");
Dog rex  = new Dog("brown", 2, "frisbee");
```

### **Checking Deep Equality**

Checking deep equality involves telling the program how to measure the equality of two objects. 

This means we need to implement \(and more technically override\) the equals method. Right click in your class, then select “Generate”.

![](../../../.gitbook/assets/image%20%2840%29.png)

Check the below options, then click “Next” through the next few screens.

![](../../../.gitbook/assets/image%20%28104%29.png)

If using the `Dog` example the returned override would look like this:

```java
@Override
public boolean equals(Object o) {
    if (this == o) return true;
    if (o == null || getClass() != o.getClass()) return false;
    Dog dog = (Dog) o;
    return getAge() == dog.getAge() &&
            Objects.equals(getColor(), dog.getColor()) &&
            Objects.equals(getFavToy(), dog.getFavToy());
}

@Override
public int hashCode() {
    return Objects.hash(getColor(), getAge(), getFavToy());
}
```

This is generated content and you don't need to memorize every part. Just know that this is how you override the equals method to check for deep equality.

