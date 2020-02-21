# Variables

### What and Why

Variables are the nouns of JavaScript. They are named containers that we can refer to by name to access the stored data inside.

Using variables keeps us from having to retype data over and over. Instead, we can just refer back to the variable containing the data. It keeps our code clean, readable, and easier to debug.

Let's say you wanted to store pi to 50 decimal places. Later on, you'll want to refer to pi in 50 decimal places but instead of retyping or even copying and pasting, you could store the data in a variable and just refer to that variable name.

### Writing Variables

We've seen values of type `number` like `4`, `7.2`, and `9` and values of type `String` like `'This is a string'` and `'potato'`, and also values of type `boolean` like `true` or `false`, and we can enter these into the console and combine them with operators to make expressions that evaluate to some new value like `2 * 4` which evaluates to `8`.

We will often want to store values to use later in our code. We store them using **variables**.

Type the following in the console:

```javascript
const num = 9;
```

On the next line type:

```javascript
num;
```

And hit enter. **Notice** that `num` now evaluates to 9.

When we use the `const` keyword we are creating a variable. A variable is just a way to store a value by a name of our choosing for later use. In this case, we named our variable `num`. So now we can use the word `num` to refer to the value `9`

Type the following and guess what it will evaluate to before you hit enter:

```javascript
num + 4;
```

It should evaluate to `13`.

Type the following in the same console:

```javascript
const num2 = 5;

num + num2;
```

Since `num` is `9` and `num2` is `5`, `num + num2` evaluates to `14`

Variables are initially created using the `const`, `let`, or`var` keyword, but are later accessed just using their names. We won't go too in-depth regarding the differences here. Just know that you'll see references to these keywords while looking at examples or documentation.

An analogy that may help you visualize variables:

> "Imagine you have a brand new attic goblin. That's right a goblin that lives in your attic. He's very very tidy and insists you clean using his particular rules. You have to store everything you want to keep in a labeled box. Everything else gets tossed out. Any time you need something that you stored in a box, you can tell the goblin the name of the box, and he'll bring you what's inside. You can store new items in the attic anytime but you must put them in a box and label them or the goblin will immediately throw them away."

> "Writing `const num1 = 2` is like making a box and labeling it `num1` and then storing the number 2 in it. Writing `num1` later in our code is like asking the goblin to find the `num1` box and give us what's inside."

In this analogy, "boxes" are variables, and the "items" are their values and the goblin is the JavaScript engine.

![Attic Goblin](../../../.gitbook/assets/attic.png)

_Why_ might we want to store a value in a variable?

Imagine that we needed to use the number `3.14159265358979323846` over and over in our code. It would be awful to type that 100 times. Instead we could store it as a variable called `PI`. 

Or perhaps we want to prompt the user for some information and store that information for use later in a variable called `input`.

Lastly, write the following code in your console:

```javascript
const sum = num + num2;

sum;
```

Before you press enter guess what value is stored in `sum`. 

Press enter and notice that it's `14`. The expression on the **right-hand side** of the equals sign is evaluated **first**. It evaluates to `14`. That value `14` is then stored in the variable `sum` on the left-hand side of the equals sign. We always evaluate the expression on the right-hand side first.

