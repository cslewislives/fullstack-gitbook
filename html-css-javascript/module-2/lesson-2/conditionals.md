# Conditionals

Thus far our programs have run every line of code in order from top to bottom, but often we will want to add more sophisticated logic. There are times when we want to run some lines of code _only if_ a certain condition is met. 

For example, we may want to alert `'You win'` if a user's score is greater than 500.

As our code gets more complex, it's essential that you start relying on your flowcharting skills. Remember to flowchart during every activity. 

![](../../../.gitbook/assets/conditional.png)

Note how we are controlling the flow in our program. Now look at the code below and notice how it maps to the above flowchart

```javascript
// Prompt the user for their age, store the value in the variable `age`
const age = prompt('How old are you?');

if (age > 21) {

  // If age is greater than 21, alert 'Sake for you'
    alert('Sake for you');
}
else {

  // Otherwise, alert 'Sake for you'
    alert('Soda for you');
}

```

If the user inputs `15` what does `age > 21` evaluates to?

**Answer:** false.

If the expression in the parenthesis evaluates to false, the block of code immediately following will not be executed and instead the block of code following the `else` statement will execute.

What would alert if the user input `32`?

**Answer:** "Sake for you"

No matter what we place between the parentheses after `if`, it will be evaluated as a boolean.

