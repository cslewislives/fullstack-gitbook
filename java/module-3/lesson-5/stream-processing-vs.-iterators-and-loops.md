---
description: >-
  Explains the difference between stream processing and the previous concepts of
  iterators and loops.
---

# Stream Processing vs. Iterators and Loops

#### Loops Iterators vs. Streams and Aggregate Operations

Processing objects in a collection using loops/iterators and processing them using streams and aggregate operations have a lot in common, but there are some key differences:

* Loops/iterators work directly on objects from the collection, but aggregate operations work on objects from a stream.
* The developer must be in control of how and when objects in the collection are processed when using a loop or an iterator. This is not the case with streams and aggregate operations—all of the iteration and control of how and when objects are acted upon are internal to the operation.
* The parameters for aggregate operations are lambda expressions. 

