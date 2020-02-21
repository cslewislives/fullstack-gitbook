# Short Circuit

In this section, we will build on your knowledge of conditionals by demonstrating the short-circuit evaluation. It may not be immediately apparent why this is important, but it's a fundamental part of control flows in JavaScript.

While we've covered the arithmetic and comparator operators in JavaScript, there are two **logical** operators we need to know about.

### OR Operator

Type the following into the console: 

```javascript
true || false;
```

Notice the double pipes \(`||`\). This is known as the **logical OR operator**.

The OR operator `||` means that the expression will evaluate to `true` if the value on the left side **OR** the value on the right side of the double pipe, or both, evaluate to `true`.

Why is `true` logged when you press enter?

**Answer:** Because one side of the operator is true.

Type the following into the console:

```javascript
false || true;
```

What should be printed in the second statement?

If the value on the left hand side of the logical OR operator is `true`, the value on the right will not be evaluated because we only need one value to be true. But if the value on the left hand side is `false`, the expression on the right hand side of the logical OR operator is evaluated.

`true` should be printed again. Since the value on the left hand side of the logical OR is `false`, it uses the value on the right side instead.

Run the code to see that in action.

### AND Operator

Type the following into the console:

```javascript
true && false;
```

The double ampersand \(`&&`\) is the logical **AND** operator.

An expression with `&&` requires **both** the value on the left AND the right to be true in order for the whole expression to evaluate to true.

If the value on the left hand side of the operator is `false`, then it is used. Otherwise if the value on the left hand side of the operator is `true`, then the second value is used.

Logical AND wants to check both values, but doesn't bother if the first value is `false`, it just uses that. Whereas logical OR wants to use the first `true` value it finds — wherever that is — but settles for the last value if there is none.

If logical AND wants to check both values, but stops at the first `false` value, what does the statement above evaluate to?

**Answer:** `false`! Since the first value was `true`, it continued to check the second value and used that.

Type the following into the console:

```javascript
false && true;
```

What logs here? Remember that logical AND wants to check both values, but stops at the first `false` value it finds.

**Answer:** `false`! It stopped at the first `false` value it found and didn't bother to check the second value.

Type the following into the console one at a time:

```javascript
true || false && true;
true && false || false || true;
```

Before pressing enter, walk through what happens in each example. What do you expect the output to be before you run it?

_Why_ might we use logical operators? 

**Answer:**

Imagine we are building a contact form for a customers website and we want to make sure that users can only submit the form **if** the user fills out the email field **AND** types a message in the message area. We would use the `&&` operator to write this logic.

**or:**

Imagine that we are building an e-commerce site that has a special savings code available to gold and platinum level members but not standard members and non-members. When a user logs in we would check to see if their membership type was gold **OR** platinum, and if so, we would display the special code. For this we would use the `||` operator.

