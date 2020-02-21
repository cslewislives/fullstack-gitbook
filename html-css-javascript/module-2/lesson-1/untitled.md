# Intro to JavaScript

Now that you understand the basics of tackling a problem programmatically, it's time to start learning actual JavaScript.

Like HTML and CSS, we don’t need anything other than a web browser to begin writing JavaScript code.

If you open your Chrome Devtools and open the Console Tab \(CMD + Option + J\) on a Mac or \(Control + Shift + J\) on PC you can type JavaScript straight into the console.

We’ll be using the Chrome console frequently as it will inform us of errors in our JavaScript code. It should be the first place we check if our code isn't working as expected.

Type the following into your console and hit Enter 

```javascript
'Hello'
```

In addition to being a powerful debugging tool, the **Console** serves a similar purpose to the **Elements** tab in Chrome: it allows us to interact with JavaScript code being run by a website, as well as inject some of our own.

We should see the word “Hello” printed right below where we’ve typed it.

By entering the text "Hello" in the console, we're telling Chrome that we want to evaluate this as JavaScript code.

JavaScript understands the concept of Strings, i.e. a sequence of characters.

JavaScript also understands the concept of numbers

Type the following \(or any number\) in your console:

```javascript
4.815162342;
```

**Notice** the console prints the value back at us, but in a different color.

This blue color signifies that the type of data we’re working with is different from the string `'Hello'` we typed earlier. It’s a number!

So far the values we’ve typed into the console have been printed back at us. Why do you think this is happening? What does it mean?

The console prints back whatever it is we type in.

Have the following ready to type into the console

```javascript
2 + 7;
```

What do you think will happen here? What will get printed back from the console? Will it print `2 + 7` or something else?

Hit the Enter key. The output should be `9`.

The console prints back the value that the last expression we typed in **evaluates** to.

An expression can be a single value, such as a string or a number, or a combination of values and operators. All expressions resolve to a single value in JavaScript.

What do you expect to happen when we type the following into the Chrome Console?

```javascript
10 + 5 4 + 9
```

We get an error! `Uncaught SyntaxError: Unexpected number`

Unlike HTML and CSS, JavaScript will let us know if we've done something wrong in the form of error messages.

Which number do you think is the unexpected one?

The number `4` is unexpected. The same way a calculator wouldn’t know what to do with this, JavaScript doesn’t either.

What we really want here are two separate expressions: `10 + 5` and then `4 + 9` on the next line.

Typing the following and hitting Enter:

```javascript
10 + 5;
```

And then doing this:

```javascript
4 + 9;
```

Would work without any issues.

But so would this:

```javascript
10 + 5; 4 + 9;
```

The Chrome Console should print back `13`, the value of the _last_ expression we typed in.

Semicolons in JavaScript signify the end of a statement. So by adding one between the two statements, we can write them both on the same line and not confuse our browser.

When we start writing complete JavaScript applications, we’ll generally write one statement, or instruction _per line_ and throw one semicolon at the end.

Now that we know that JavaScript understands math, we can use it as a calculator!

