---
description: 'Same old name, whole new implementation.'
---

# Method Overloading

Method overloading allows us to have several methods with the same name. 

But why would we want several methods with the same name? We could have a series of `add` methods: one for adding ints, one for adding floats, etc. `System.out` has several `println(...)` methods; we can print booleans, Strings, ints, etc.

This means that each overloaded method will have the same name but a different parameter list. 

```java
public class SimpleAdder {

    public static int add(int a, int b) {
        return a + b;
    }

    public static long add(long a, long b) {
        return a + b;
    }

    public static float add(float a, float b) {
        return a + b;
    }

    public static double add(double a, double b) {
        return a + b;
    }
}
```

```java
public class App {

    public static void main(String[] args) {

        int int1 = 1;
        int int2 = 3;

        long long1 = 4;
        long long2 = -3;

        float float1 = 1.5f;
        float float2 = 2.1f;

        double double1 = 0.7d;
        double double2 = 4.4d;

        System.out.println( SimpleAdder.add(int1, int2) );
        System.out.println( SimpleAdder.add(long1, long2) );
        System.out.println( SimpleAdder.add(float1, float2) );
        System.out.println( SimpleAdder.add(double1, double2) );
    }
}
```

