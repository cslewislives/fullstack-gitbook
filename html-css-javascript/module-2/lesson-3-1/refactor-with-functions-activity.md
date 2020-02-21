# Refactor with Functions - Activity

![Refactor with Functions](../../../.gitbook/assets/image%20%2837%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

You'll now do what's called **refactoring** which means to restructure existing code.

Open up `index.js` and create a new function that will accept an array as a parameter.

What this function will do is take the parameter passed in and loop over it.

As it looks through the numbers, it will add up all of the numbers in the array, and return the sum of all of the numbers.

After you finish, call the new function 5 times, passing in a different array each time.
{% endtab %}

{% tab title="Solution" %}
```javascript
const numList1 = [1, 4, 5, 6, 2, 3, 1, 7, 6, 8];
const numList2 = [10, 9, 77, 9, 2, 1, 0, 82, 2];
const numList3 = [1, 14, 66, 543, 2, 1, 5, 674];
const numList4 = [9, 6, 3, 2, 1, 6, 7, 8, 8, 7];
const numList5 = [4.2, 5.1, 3, 0, 0, 453, 2.43];

const sumFunc = function (arr) {

  let sum = 0

  for ( let i = 0; i < arr.length; i++ ) {
    sum = sum + arr[i];
  }
  console.log(sum);
}

sumFunc(numList1);
sumFunc(numList2);
sumFunc(numList3);
sumFunc(numList4);
sumFunc(numList5);
```
{% endtab %}
{% endtabs %}

 

