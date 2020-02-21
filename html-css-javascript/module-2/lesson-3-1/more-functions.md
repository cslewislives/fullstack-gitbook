# More Functions

Because functions are a fundamental part of JavaScript and programming in general, we'll be getting into the weeds of some of the intricacies of functions and going over:

* Different ways to write functions
* More arguments and logic practice
* The `return` statement. 

You'll be using functions for as long as you continue to program. Not only will you learn more about functions, but gain additional practice using them for various scenarios.

Any time you want to do something with multiple inputs into a function, you'll be doing this.

We're going to pause for a moment and explore different ways to define functions. We want to make sure we go over some of these as you'll no doubt see references when looking up guides or documentation. The differences can be pretty subtle.

### Declaring Functions

There are multiple ways to write functions. In fact, as you look through documentation or Google questions, you'll more than likely see functions being defined in various ways.

* **Function Declarations** 
  * Start by using the keyword `function`. 
  * Load _before_ any code is executed.

```javascript
function example() {

};
```

* **Function Expressions** 
  * Start by using the keyword `const`, `let`, or `var`. 
  * Load _when_ the interpreter reaches that line of code.

```javascript
const example = function() {

};
```

* **Arrow Functions** 
  * Simply a different syntax when writing function expressions. 
  * They utilize a new token, `=>` 
  * Remove the need to use the `function` keyword or curly brackets \(though you'll see curly brackets being used in many arrow function examples\). 
  * There are some additional benefits to using arrow functions beyond syntactic simplicity but we won't focus on those right now

```javascript
const example = () => console.log('this is an arrow function!');

**or**

const example = () => {
  console.log('this is an arrow function!')
};
```

### Multiple Parameters

So far, we have been creating functions that take only one argument. But functions can have multiple parameters when defining them.

Open the Chrome console or jsbin and enter the following:

```javascript
const multiply = function (num1, num2) {
	console.log(num1);
	console.log(num2);
};

multiply(1, 2);
```

We can define the function above, passing in multiple parameters separated by commas. We'll then have access to those parameters within the function block.

We can also write logic within the function code block:

```javascript
const multiply = function (num1, num2) {
	console.log(num1 * num2);
};

multiply(1, 2);
```

After running the code above, notice that we've created a multiplication function that takes in two numbers, and multiplies them.

We can do this with strings as well:

```javascript
const stringFunc = function (string1, string2) {
  console.log(`${string1} ${string2}`);
};
```

What do you think will happen when we write:

```javascript
  stringFunc('Tomato, potato,', 'I drive a Winnebago');
```

{% hint style="info" %}
**Reminder:** The parameters of our function can be named ANYTHING the writer wants.
{% endhint %}

The fact that parameters can be named anything is an important point that learners often get lost on. Try changing the parameter names in the above function a few times. Try `string` and `otherString`, `word` and `phrase`, `banana` and `peanuts`.

After we define our function, when we are ready to execute the code inside the curly braces, we **call** our function using the following syntax — `name(param1, param2);`

Call the above function with a few different parameters:

```javascript
stringFunc('Hello', 'world');
stringFunc('How are', 'you?');
```

The strings we input in our call BECOME the value of the parameters we had declared in our function definition.

* `string1` = `'Hello'`
* `string2` = `'world'`

### `return` Keyword

Adjust the code to match the code below.

```javascript
const stringFunc = function (string1, string2) {
  return `${string1} ${string2}`;
};

stringFunc('Hey,', 'Friends!');
```

The **return** keyword means that the call site will evaluate to the returned value.

The function call-site \(that is where we write the function name followed by parenthesis\) is an expression that evaluates to the value following the `return` keyword inside the function.

See this in action using the code below:

```javascript
const stringFunc = function (string1, string2) {
  return `${string1} ${string2}`;
};

const output = stringFunc('Whatcha', 'eating?');

console.log('output:', output);
```

