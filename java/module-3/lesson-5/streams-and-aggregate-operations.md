---
description: An overview of streams and aggregate operations.
---

# Streams and Aggregate Operations

This section introduces the concepts of streams and aggregate operations. We take a top-down approach to presenting these topics, so here we just introduce the big picture.

In following sections, we look at putting several operations together in a pipeline, comparing stream processing with iterators and loops, and using lambda expressions with aggregate operations. 

#### About Streams and Aggregate Operations

* Lambdas, streams, and aggregate operations are relatively new to Java. They were introduced in Java 8.

**Two Types of Aggregate Operations**

* **Aggregate operations** come in two types \(we'll discuss this more in the next section on pipelines\):
  * **Intermediate operations**: accept a stream and produce a stream.
    * Some intermediate operations accept a stream of one type and produce a stream of another type \(for example, a stream of motorcycles might be converted into a stream of ints that are the displacements for each motorcycle\).
  * **Terminal operations**: accept a stream and produce a non-stream result \(which could be null\).

**Streams and Aggregate Operations Used with Lambdas**

* Lambdas got a lot of the attention when the features of Java 8 were announced because they introduced functional programming to Java.
* The real power for everyday tasks is when streams and aggregate operations are used with lambdas. This combination gives developers some great options for processing collections of data. For example:
  * Get all the motorcycles made by a particular manufacturer
  * Get all the motorcycles with power under 100 horsepower
  * Get all the motorcycles made by a particular manufacturer under 100 horsepower
  * Calculate the average displacement of the motorcycles in the collection
  * Return the value of the highest horsepower in the collection
  * Group the motorcycles by manufacturer and return them in a map where the key is the name of the manufacturer and the value is a list of motorcycles from that manufacturer

