# Boolean Coercion

In JavaScript, we can convert or **coerce** a value from one type to another, like numbers to Strings and booleans to numbers. Explain that any type can be coerced to any other type. 

Sometimes you're not just checking what the value inside of a user input is. You're checking to see if there is a value at all! 

There might be an error in the input, but you can start by understanding if there's an input. How do you do that? truthiness, falsiness, and boolean conversion! But you should start by seeing IF there's an input at all

Open the Chrome console and type:

```javascript
!!0;
```

There are several ways to see what a value would evaluate to if it were coerced to a boolean but the easiest is to use the double bang `!!`.

What will the above code will return?

**Answer:** `false`

0 is what is called a **falsey** value which means when coerced to a boolean it will always evaluate to false.

Try the following one line at a time:

```javascript
!!0;
!!1;
!!3;
!!-422;
!!'';
!!'hey';
```

Any non-zero, non-NaN number will always evaluate to **truthy**.

Similarly, any non-empty string will always be true.

One way to remember this is to remember that a value that represents something that doesn't exist is usually falsey. For example, `''`, `0`, `false`, `null`, `undefined`, `NaN`.

When we use if/else statements in JavaScript, whether the condition inside the parentheses evaluates to `true` or `false` is based on its truthiness or falsiness. For example, the code inside of the following if statement will always run:

```javascript
if ('non empty strings are truthy') {
  console.log('This always runs!');
}
```

Conversely, the following if statement will never run:

```javascript
if (0) {
  console.log('This never runs!');
}
```

