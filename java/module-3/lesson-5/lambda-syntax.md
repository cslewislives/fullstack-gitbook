---
description: An example of lambda syntax.
---

# Lambda Syntax

Lambda syntax has a lot of great "syntactic candy" that allow for very concise code. This is really convenient once you understand what is going on, but it can be quite confusing at first. In addition to that, defining a standalone method inline is a little weird, especially for new developers. Here we'll go through a simple example starting with syntax that looks almost like a regular method declaration and then using syntactic shortcuts to transform it into a more concise format. 

#### Traditional Method Declaration:

```java
boolean filterByMake(Motorcycle moto) {
  return moto.getMake().equals("Suzuki");
}
```

#### Verbose Lambda Declaration:

* This format can be used no matter what.
* We can take some more shortcuts under certain circumstances.

```java
(Motorcycle moto) -> {
  return moto.getMake().equals("Suzuki");
}
```

#### More Concise Lambda Declaration:

* If we have only one parameter, we can lose the parentheses.
* We can also lose the parameter type—the compiler will use inference.
* We can take further shortcuts under certain conditions.

```java
moto -> {
  return moto.getMake().equals("Suzuki");
}
```

#### Even More Concise Lambda Declaration:

* This particular method declaration works with the `filter` aggregate operation \(which, as you can infer, expects a boolean return\).
* In this case, we don't have to use the `return` keyword. The compiler will infer that the last statement in the method should be returned.
* If there is only one statement in the body of the method, we don't need to use curly braces.
* Developers generally try to use the most concise form they can.
* We'll see several examples of different formats later.

```java
moto -> moto.getMake().equals("Suzuki");
```

{% embed url="https://youtu.be/HOz62xsKNTQ" %}

