---
description: A brief explanation of iterators
---

# Iterators

**What tools did we use to visit each element in an array?** 

### The need for iterators

* Sometimes we need to visit all of the elements in a collection.
* Not all collections are ordered like an array \(for example, Sets\). This makes taking the array approach problematic.
* We still need a way to visit/access each element in a collection.
* This is where iterators come in.

### About Iterators

* An iterator is an object that allows us to visit/access each element in a collection one by one.
* Iterators have two methods:
  * `hasNext()`, which returns true if there are one or more elements left to access
  * `next()` which grabs the next element and returns it to us
* Some iterators also have a `remove()` method, but this is not required.
* We have no control over the order in which the elements are returned, but we really don't care. We just care that we are guaranteed to visit/access each element exactly once.
* The pattern is that we keep calling `next()` as long as there is another element to visit \(i.e., `hasNext()` returns true\).
* We'll see this in action when we look at lists later in the lesson.

