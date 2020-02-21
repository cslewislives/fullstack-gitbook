# Variable - Activity

![Variables](../../../.gitbook/assets/image.png)

Make sure you attempt the activity on your own before looking at the solution.

{% tabs %}
{% tab title="Instructions" %}
### Instructions:

In your console write code to answer these questions: 

* How do you create a variable that holds the string 'Joe Smith'?
* How do you create a variable that holds my favorite number, 9?
* How do you create a new variable called `goodNumber` that holds the value `0`?
* How do you create a new variable and assign it the value of `favNumber` plus `4`?
* How do you reassign sum to be `favNumber` + `9`?! An error! Explain that `const` stands for constant and indicates that the variable can't be reassigned.
* How would you create a variable called product that holds the value one?
* What needs to change if I want to reassign `product` to `favNumber` times two on the next line?
* How can I set product equal to its current value times 4?
{% endtab %}

{% tab title="Solutions" %}
### Instructions:

In your console write code to answer these questions:

> "How do you create a variable that holds the string 'Joe Smith'?"

```javascript
const name = 'Joe Smith';
```

> "How do you create a variable that holds my favorite number, 9?"

```javascript
const favNumber = 9;
```

> "How do you create a new variable called `goodNumber` that holds the value `0`?"

```javascript
const goodNumber = 0;
```

> "How do you create a new variable and assign it the value of `favNumber` plus `4`?"

```javascript
const sum = favNumber + 4;
```

> "How do you reassign sum to be `favNumber` + `9`.

This will error

```javascript
sum = favNumber + 9;
```

Uh-oh! An error! `const` stands for **constant** and indicates that the variable can't be reassigned.

We should always use `const` when we can, but if we need to reassign a variable, we should use `let`.

```javascript
let bestNum = 0;
bestNum = 4;
bestNum = 3;
```

> "How would you create a variable called product that holds the value one?"

```javascript
const product = 1;
```

> "What needs to change if I want to reassign `product` to `favNumber` times two on the next line?"

```javascript
let product = 1;
product = favNumber * 2;
```

> "How can I set product equal to its current value times 4?"

```javascript
product = product * 4;
```

`product` on the right-hand side of the assignment operator refers to the value inside the `product` box. `product` on the left-hand side of the assignment operator tells the engine which box to store the new value in.
{% endtab %}
{% endtabs %}

