---
description: Paints the big picture of exceptions in Java
---

# Java Exception Overview

The main points are:

* Errors occur in all programs.
* Every programming language has a way to handle errors.
* Exceptions are the approach that Java takes. 

#### Definition

According to Oracle, the definition of "exception" is: "An exceptional event which occurs in the normal execution of a program that disrupts the normal flow of the program's instructions."

#### Handling Exceptions

There are two ways to address code that might throw an exception:

* We can handle them; we call this "catching the exception."
* We can pass the buck by marking that our code might throw an exception, leaving it to other code to catch the exception.
  * This is what we did when we first encountered exceptions in the Simple File I/O lesson.
* We'll see details on catching exceptions below.

#### Types of Exceptions

There are two main categories of exceptions in Java:

* **Checked**: We are required to either catch these or specify that our code might throw one of these. The compiler will enforce this requirement.
* **Unchecked**: We do not have catch or specify these, but we can catch them if we want to.
  * Unchecked exceptions are generally errors that we can't or don't want to recover from, but that is certainly not always the case \(as we'll see later in this lesson\).

### Try/Catch/Finally

The language construct used to handle exceptions is try/catch/finally. It looks like this:

```java
try {
  // some code that might throw and exception
} catch (an-exception-type identifier) {
  // some code to handle or recover from the exception
} finally {
  // some code that runs whether there was an exception or not
}
```

