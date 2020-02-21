# Method Recap

Methods are simply a tool that allows developers to package together an action \(like adding, concatenating, doing some complex method, or validating user authentication\) and perform that action repeatedly with different inputs. 

In essence, methods can take four forms. 

* No return value, no parameters
* Return value, no parameters
* No return value, one or more parameters
* Return value, one or more parameters 

These are patterns that you will see over and over. You need to memorize these and practice recognizing them. This will become second nature very quickly.

#### No return value, no parameters:

```java
public static void calcArea() {
        int height = 10;
        int width = 15;
        int area = height * width;
        System.out.println(area);
}
```

#### Return value, no parameters:

```java
public static int calcArea() {
        int height = 10;
        int width = 15;
        int area = height * width;
        return area;
}
```

#### No return value, one or more parameters:

We now have parameters. Note how they are declared: just like declaring a variable, you need a data type and a name. There is no return value for this example.

```java
public static void calcArea(int height, int width) {
        int area = height * width;
        System.out.println(area);
}
```

#### Return value, one or more parameters:

This is similar to the last one, but it has a return value.

```java
public static int calcArea(int height, int width) {

        int area = height * width;
        return area;
    }
```

{% embed url="https://youtu.be/QOVgaIpASNU" %}

