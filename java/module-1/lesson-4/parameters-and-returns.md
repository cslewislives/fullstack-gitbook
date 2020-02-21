---
description: Method input variables.
---

# Parameters & Returns

### Parameters

Parameters are simply variables that are declared in the method declaration that catch the values being passed in. Like any normal variable, they must be declared with a type and name. The name can be any valid variable name and should follow good naming conventions. 

Every time the method is called it executes again. Every execution, has different parameter values based on what was passed in when the method was called.  

```java
public static void main(String args[]) {
    int sum1 = add(1, 2);
    int sum2 = add(3, 7);
    
    System.out.println(sum1);
    System.out.println(sum2); 
}

public static int add(int a, int b) {
    return a + b;    
}
```

Copy the above code into IntelliJ. Run it and see what prints. Note how the values of the variables change each time. 

Check out the code below. The only change is the variable names. Note that this has no impact on how the program executes. You can name parameters whatever you like. 

```java
public static void main(String args[]) {
    int sum1 = add(1, 2);
    int sum2 = add(3, 7);
    
    System.out.println(sum1);
    System.out.println(sum2); 
}

public static int add(int num1, int num2) {
    return num1 + num2;    
}
```

## Return Type

Methods can return values to the caller, but they don’t have to. Even if our method does not have a return value, we must always indicate a return type. The return type for a method that returns no value is void. Otherwise, it is the type of whatever value is returned from the method.

The call-site of the method evaluates to the returned value after execution. In simpler terms, `int sum1 = add(1, 2);` is essentially `int sum1 = 3;` after the method executes because it returns 3. 

Check out the examples below, noting the return type in each:

```java
public static int add(int num1, int num2) {
    return num1 + num2;    
}
```

```java
public static String makeGreeting(String name) {
    return "Hello, I'm " + name;    
}
```

```java
public static void greet(String name) {
    System.out.println("Hello, I'm " + name);    
}
```



