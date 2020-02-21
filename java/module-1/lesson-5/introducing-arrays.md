---
description: >-
  An array is a data structure that contains a fixed number of elements of a
  specific data type.
---

# Introducing Arrays

Up to now, we have been dealing with variables that hold a **single** value of a **particular** type. This is fine for simple programs, but it will become necessary to keep track and manipulate more complex sets of related data as we build more sophisticated programs. 

**Arrays** allow for the tracking and manipulation of more than one value of a particular type.

## Key aspects of an Array

We will use the following 'fruits' array as we discuss the key aspects of this new data structure. 

```java
String[] fruits = {"apples", "oranges", "bananas"};
```

* An array is a **data structure** that can hold a **fixed number** of values of the **same data type**. 
  * Fixed number - the number of elements in the 'fruits' array is 3. 
    * Once you specify the length of the array \(i.e., the number of values it can hold\), it cannot be changed.
  * Same data type - all elements of the 'fruits' array are strings. The data type is declared at the beginning of the array and declared with square brackets \(ie **String\[ \]**\)
    * You must specify what data type the array can hold when you declare the array. This cannot be changed.
* Data values in the array are called **elements**.
* The elements in the array are **ordered**.  The location of each element is indicated by an index. The index numbering **starts at zero** and is sequential.
  * Example: An array with three elements will have index numbers of 0, 1, 2,.
  * In the fruits array, "apples" is in index position 0; "oranges" is in index position 1, and "bananas" holds index position 2. 

Additional examples of arrays are:

```java
int[] numbers = {0, 1, 2, 3, 4, 5};
String[] carMakes = {"Porsche", "Tesla", "Honda", "GMC"};
```

