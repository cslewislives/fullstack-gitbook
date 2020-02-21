# Introduction to Functions

### **What, Why, and When**

A **function** is a set of defined steps or procedures that can be executed at will by calling the function followed by arguments \(optional\).

Functions are important to modularize your code, making it easier to debug and read, and reduces the amount of code required to write.

You'll use functions when you want repeatable blocks of code. 

### DRY \(Don't Repeat Yourself\)

Functions in programming allows us, the developers, to write blocks of code that can be reused.

When we want to do the same thing repeatedly one right after another, we use a loop. But what if we want to do the same thing repeatedly but not necessarily consecutively? 

For this we use functions. But to really emphasize the importance of functions, we'll do things the long way around, then show you how to condense your code using functions.

#### Example:

* Loop through each array and render the sum.
* You will need to create a new loop for each array.

```javascript
const numList1 = [1, 4, 5, 6, 2, 3, 1, 7, 6, 8];
const numList2 = [10, 9, 77, 9, 2, 1, 0, 82, 2];
const numList3 = [1, 14, 66, 543, 2, 1, 5, 674];
const numList4 = [9, 6, 3, 2, 1, 6, 7, 8, 8, 7];
const numList5 = [4.2, 5.1, 3, 0, 0, 453, 2.43];

let sum = 0;

for (let i = 0; i < numList1.length; i++){
  sum = sum + numList1[i];
}

console.log(sum);

sum = 0;

for (let i = 0; i < numList2.length; i++){
  sum = sum + numList2[i];
}

console.log(sum);

sum = 0;

for (let i = 0; i < numList3.length; i++){
  sum = sum + numList3[i];
}

console.log(sum);

sum = 0;

for (let i = 0; i < numList4.length; i++){
  sum = sum + numList4[i];
}

console.log(sum);

sum = 0;

for (let i = 0; i < numList5.length; i++){
  sum = sum + numList5[i];
}

console.log(sum);
```

 **Notice:** We have a lot of repetition in our code. Think about alternatives so that we don't have to keep retyping all of this code.

True we can simply copy and paste. But what if there was actually an easier solution than even that? One that is more dynamic as well. 

The answer is functions.

