# First Function

A function is a block of code designed to perform a specific task. Functions allow us to do the same action over and over, and even across projects \(like `prompt` and `console.log`\), without rewriting all of the code.

First we must **define** a function. We define a function by first creating a variable using `const`. We then give our `const` a **name** and assign its value to a function. The name can be anything you want but should be descriptive.

Open the Chrome console or jsbin and enter the following:

```javascript
const multiply = function () {
  console.log('Our First Function!');
};

multiply();
```

* We assign our new variable the value of a function using the keyword `function` followed by a set of parentheses `()` and curly braces `{}`.
* The code that we want to execute when the function is called goes inside the curly braces.
* Finally, we are able to **call** the function by referring to the name of the function, followed by parenthesis.
* Then, alter the multiply function by adding in a parameter and console logging that parameter.

```javascript
const multiply = function (num1) {
  console.log(num1);
};

multiply(3);
```

* `num1` is a **parameter**, 
  * An empty box waiting to catch the data passed in to the function.
* The `3` within the parenthesis of the function call is an **argument**,
  * Data that we want to pass to the function.
* The values passed in during the function call are assigned to the parameter variables created in the function definition.

Behind the scenes, when we call `multiply(3)`, the JavaScript engine is creating a variable called `num1` and assigning it the value we pass in.

