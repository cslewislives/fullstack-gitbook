---
description: A brief description of lambdas and a list of some aggregate operations.
---

# Lambdas and Aggregate Operations

#### Lambda Features

* So far, all of our parameters to methods have been data of some kind: either primitives or objects.
* Lambdas allow us to pass in methods as parameters, which is a really powerful feature that allow us to pass in or define functionality on the fly.
* This allows us to easily create code to process objects in collections. Each aggregate operation takes a lambdas expression as a parameter. 

#### Aggregate Operations

* `filter`—An intermediate operation that filters the object in a stream based on the logic in the given lambda expression.
* `forEach`—A terminal operations that acts on each object in a stream according to the logic in the given lambda expression.
* `collect`—A terminal operation that returns a collection of objects according to its parameter.
* `average`—A terminal operation that returns the average of the given input stream. The average is returned as an `OptionalDouble`.
* `mapToXxx`—A family of intermediate operations that map an input stream of one type into a stream of another type based on the logic in the given lambda expression. For example, `mapToInt` would map an incoming steam of object to a stream of integers.
* `getAsXxx`—This is a family of operations that take an `OptionalXxx` type as input and then return the value as an `Xxx`. For example \(from above\), the average aggregate operation returns an `OptionalDouble`, so we would use `getAsDboule` to convert the `OptionalDouble` to `Double`.

We'll see examples of these operations in action later.

