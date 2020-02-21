---
description: 'Introducing multi-dimensional array, also thought of as an array of arrays.'
---

# Multi-Dimensional Arrays

Multi-dimensional arrays can be thought of as an array of arrays. Data in multi-dimensional arrays are stored in tabular form, similar to that of a spreadsheet. 

Let is being our exploration by looking at a two-dimensional array. 

```java
int [][] twoD_arr = new int [3][3];
```

 The pieces of the code detailed above should look familiar given our earlier work with declaring arrays. 

* We being, as always, with the data type for our arrays.
* The groups of square brackets \(\[ \] \[ \]\) indicate that it is a multi dimensional array. Regardless of the number of dimensions, only 2 sets of brackets is utilized. 
* The variable name of our two-dimensional array is declared with `twoD-arr`.
* We utilize the **new** keyword having the computer save space in memory for our array. 
* We again utilize the keyword`int` to indicate the data type of our arrays.
* Finally, the information in our square brackets indicates the size of our two arrays. 

Using the initializer method, we can create  a three dimensional arrays as follows.

```java
    String[][] multiArr = { 
        {"a", "b", "c"}, {"1", "2", "3"},{"i", "ii", "iii"}
    };
```

We access the above elements by drawing on the fact that these element are a **nested set of indexed positions**. Remember, a multi-dimensional array is an **array of arrays**.

The top level of multiArr has 3 index positions:

* multiArr\[0\] is { "a", "b", "c" }
* multiArr\[1\] is { "1", "2", "3" }
* multiArr\[2\] is { "i", "ii", "iii" }

The nested level of multiArr **also** has 3 index positions:

* multiArr\[0\]\[0\] is "a"
* multiArr\[0\]\[1\] is "b"
* multiArr\[0\]\[2\] is "c"
* multiArr\[1\]\[\]1\] is "2"

Given this information, can you guess the value of multiArr\[2\]\[2\]?

If you answered "iii", you were correct. 

{% embed url="https://youtu.be/gDoHhfGGVXs" %}

With this basic understand of multi-dimensional arrays, let us move on to how we access the values using loops. 

