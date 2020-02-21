# Loops II

### Arrays and Loops

Now let's see how to iterate through an array of items using a for loop. Because we are iterating through an array that we'll want to refer to each data element of the array by its index.

```javascript
const studentList = ['justin', 'maryam', 'sterling', 'pawan', 'ben'];

for (let i = 0; i < studentList.length; i++){
  const student = studentList[i];
  console.log(student);
}
```

{% hint style="info" %}
**Notice** the use of `.length`. This allows us to create a loop with a set number of iterations without knowing that number ourselves.
{% endhint %}

Let's do something cool and change the data elements of an array while looping through it.

```javascript
const exampleList = ['George', 'Tim', 'Cj', 'Lisa', 'Daniel'];

for (let i = 0; i < exampleList.length; i++) {
  exampleList[i] = i;
}

console.log(exampleList); //exampleList should now contain [0,1,2,3,4]
```

Although using the `const` keyword makes it impossible to reassign a variable, we can still alter elements in the array.

> "Imagine each variable is like a box. The `const` keyword means you can't take the item stored in a box out and replace it with a new item. You can't take box storing 4 and change it to store 5.

> "Storing an array is like storing a sheet of paper with a list of data elements scribbled on it. We can't take the sheet of paper out of the box and replace with a new sheet, but we can erase an data element on the sheet of paper and write over it."

