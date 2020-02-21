# Intro to JavaScript II

### **Strings**

Strings in JavaScript allow us to store a series of characters within double quotes `"` or single quotes `'`.

If you choose double or single quotes, continue using one or the other for consistency in your code.

We will mostly be using single quotes `'` ourselves.

Type the following into your console and hit Enter after each line

```javascript
'This is a string!'

'You type any characters you want in here'

'You can even do something called Concatenation! Let´s talk about that.'
```

In addition to being used for mathematical operations on numbers, the `+` operator can can be used to concatenate — that is, to combine — strings together.

By using `+` when typing a string, we can combine our string with other strings or other types like numbers. This is called **concatenation**.

Run the following code in your console

```javascript
'I can take a string ' + 'and another string ' + 'and combine it with a third!'
```

When we hit enter the strings are concatenated \(combined\) and the expression evaluates to a single string.

We add a space to the end of each string so that it reads normally. Run the following code to see this in action:

```javascript
'I can take a string' + 'and another string' + 'and combine it with a third!'
```

Although the above code works and they need to be familiar with it, there is a newer way of doing this that is generally preferred, but we need to learn about variables first to understand that way.

_Why_ might we want to concatenate strings?

We might want to do that for things like: The user inputs their name and we want to combine it with the string `'Welcome '` to say something like `'Welcome Diane'`, etc.

### **Booleans**

A **boolean** is a data type representing one of two values: `true` or `false`.

Type the following into the console, pressing Enter after each line:

```javascript
1 === 1;

1 === '1';

'hi' === 'hi';

1 === 2;

'hi' === 'hello';
```

These expressions evaluate to a `boolean` value, which is to say that they evaluate to `true` or `false`.

We use **three** equals signs `===` to mean "is equal to".

Line 1 is evaluating whether 1 "is equal to" 1, etc.

Why does `1 === '1'` evaluate to false?

That is because `1` is a number and `'1'` is a string, so even though they have the same value, they have different **types**. To evaluate to `true` the things being compared with `===` must be equal in value _and_ type.

{% hint style="info" %}
In JavaScript there are a few ways to compare elements, for now we will stick with `===` but feel free to do your own research on the topic.
{% endhint %}

