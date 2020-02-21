# Prompt/Alert

Take a look at the JS code you saw at the end of the previous page:

```javascript
const greeting = prompt('enter your name');
alert('Hello ' + greeting);
```

What do you think will happen when we run this code? 

After spending a few minutes brainstorming what the code _might_ do, go ahead and open the HTML file in your web browser.

`prompt` is a **function** built into JavaScript.

A function is just a named section of pre-written code that we can run whenever we want just by writing the function's name followed by parentheses: `prompt()`.

We can also pass values to the function that we want it to use. The values that we "pass" to a function are called **arguments**. In the example above, `const greeting = prompt('enter your name');` the argument is `'enter your name'`. Our arguments always appear inside the parenthesis.

> "Functions are a more advanced concept, and it's important that we get the fundamentals down first before we dive into functions too deeply. It's completely okay if all this terminology doesn't make sense right now.

> "The important thing to understand is that the `prompt` function opens a pop-up dialogue in the web browser and prompts the user for some input. The string we pass in as an argument is used inside of the pop-up dialogue."

What do you think happens to the value we type into the prompt window? Does it get stored anywhere?

If you answered that it gets stored in the variable `greeting` you are correct!

Functions can accept some input \(the arguments we pass between the parentheses\). And they can also output \(or **return**\) a value as well.

In the case of the `prompt` function, it takes the text to be displayed as input, and produces the value typed in by the user as output.

Take a look at the following piece of the code:

```javascript
const greeting = prompt('enter your name');
```

It prompts the user for a name, and returns the value they type in. The value that is returned is then assigned to the variable `greeting`.

Now look over this next section of code:

```javascript
alert('Hello ' + greeting);
```

The `alert` function is similar to `prompt`. `alert` throws up a pop-up dialogue but doesn't take any user input — it just displays the message we pass in.

**Notice** that we used String concatenation with `+`. But there is a newer way and we'll be using that from here on out.

Switch out the code above with:

```javascript
alert(`Hello ${greeting}`);
```

We put `${}` around any variable names or other expressions and the value that expression evaluates to will be injected into the string.

Here are a few quick examples:

```javascript
const num1 = 4;
const num2 = 2;
alert(`I can add ${num1} and ${num2}! See... it's ${num1 + num2}`);

alert(`I can 
span
multiple
lines. See?!`);
```

