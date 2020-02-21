# Functions - Activity

![Functions](../../../.gitbook/assets/image%20%2837%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

Open your editor and create a file named `function.js`.

In this activity we will create 3 functions.

1. Our first function will accept 1 parameter \(a number\) and multiply it by itself and return the new value.
2. Our next function will accept 2 parameters \(both strings: a first name and a last name\) and return the name in the following format: lastName, firstName.
   1. e.g. given the arguments \("Arya", "Stark"\), the function should return "Stark, Arya".
3. Our last function will accept 1 parameter \(number\) and return a boolean: true if the number is even, and false if the number is false.

Be sure to call all of your functions after defining them and log all of your results in the console.
{% endtab %}

{% tab title="Solution" %}
When we define a function, we can specify that it can expect to receive named values known as `parameters`.

After we define our parameters we can use them in the code we want to execute when the function is run.

When calling our function, we can pass in values, called arguments, to take the place of the parameters we described.

```javascript
const selfMultiply = function (num1) {
    return num1 * num1;
}

console.log(selfMultiply(3));

const fullName = function (firstname, lastname) {
    const name = `${lastname}, ${firstname}`;
    return name;
}

console.log(fullName("George", "Yoo"));

const numCheck = function (num) {
    return (num % 2 === 0);
}

console.log(numCheck(2));
console.log(numCheck(3));
```
{% endtab %}
{% endtabs %}

 

