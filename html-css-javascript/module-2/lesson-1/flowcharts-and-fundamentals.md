# Flowcharts and Fundamentals

### What and Why

JavaScript is the only major language supported by browsers. That means all front-end developers use JavaScript. Learning JavaScript is like learning any language, it takes time to get the syntax down. 

Before we worry about syntax, we'll focus on developing our programmatic thinking. That's where flowcharts come in handy.

Flowcharts help you to visualize the various components needed to create your project. They will help you write cleaner more organized and less error prone code.

For every single project, you should flowchart _first_ before you start writing your code. It's a great habit that will make you a better developer. Start the habit now while problems are simple and you'll have all the habits in place to make you successful when you tackle more complex problems in the future.

Regardless of your experience level, you will benefit from practicing flowcharting. It's a great way to learn fundamentals for the first time or revisit them.

Programming takes a while to learn, but we'll be breaking it down into bite sized chunks. We'll first learn about storing numbers and performing basic arithmetic operations like addition and subtraction.

When flowcharting you can use a whiteboard, a screen annotation tool, or an online tool like [draw.io](https://www.draw.io/) to do so.

### Components of JavaScript

Programming is simply storing and manipulating data in an organized manner. To learn to program, we need to learn each of those components - storing data, manipulating data, and organizing the order in which our program runs. This last part is often called _controlling the flow of our program_.

#### Storing Data

Let's start with storing data. In programming, we store data in something called a **variable**. You can think of a variable as a box with a name that holds something for you to use later. In programming, if I have a friend named 'Laticia' and I want to remember her name later, I have to store it in a box \(variable\) and give that box a descriptive name like `friendName`.

In JavaScript we can store a few different types of data. The first type we'll look at is `numbers`. In our flowchart if we want to store a number in a box named `num1` we denote this by creating a rectangle with the notation `number:num1`. The first part reminds us that this box should store a number and the second part is the boxes name."

![num1](../../../.gitbook/assets/num1.png)

A variable can switch from holding a number to holding a word or another type of value. However this is a bad practice, so it's good to get into the habit of noting which type of value each variable should hold when they are designing their programs with flowcharts.

#### Manipulating Data

Next let's look at manipulating data. We can manipulate number data using all your basic arithmetic operators `+`, `-`, `*`, `/`. There are a few more, but these are the major four. Arithmetic operators do exactly as you would expect. They add, subtract, multiply, and divide numbers! 

There is also the assignment operator `=`. The assignment operator allows us to put values into the box \(variable\) that we've created. **Remember** we need a variable-box to hold any data that we don't want to immediately lose.

![num1 Assignment](../../../.gitbook/assets/num1_assign.png)

The first program above stores the number 4 in a variable called `num1`.

![num2 Assignment](../../../.gitbook/assets/num2_assign.png)

The next program shown above stores the number 4 in a variable called `num1` and the number 6 in a variable called `num2`. The arrows indicate the order in which the operations take place.

![sum Program](../../../.gitbook/assets/sum.png)

The last program stores the number 4 in a variable called `num1`, the number 6 in a variable called `num2` and the sum of those two numbers in a variable called `sum`.

What value is being stored in the variable `sum`? 

If you answered `10` then you are correct!

#### Making it Useful

The above program is pretty useless. The purpose of most applications is to provide some service to the user, but the user can't even see the sum in this program.

![render](../../../.gitbook/assets/render.png)

The above image represents a program that adds 2 numbers and displays that sum.

Now the program is kind of useful but pretty boring. It just starts, stores two numbers, adds them, displays the sum, and ends. That doesn't do us much good. We've learned how to store and manipulate data. Let's take a look at the last part of programming - controlling the flow.

#### Controlling the Flow

Typically, we don't want a program that just runs straight from top to bottom. We want a program that waits for user input and _then_ performs some operations. 

For example, let's say we want to write a program that waits for a user to input their username and password. Once the user performs the **action** of clicking the `login` button, the program checks to see if they are a valid user. 

Or maybe we want to build an employee directory that adds an employee to the database only when a user inputs new employee information and clicks the `add` button.

![Event Listener](../../../.gitbook/assets/listener.png)

The above image represents a program that stores the number `4` as a variable called `num1`. It then waits for the user to click a button. The right arrow indicates that the logic to the right will only run once the user clicks the button.

When the button is clicked, the user input is stored in a variable named `num2`. The `sum` of `num1` and `num2` is then stored as `sum` and subsequently rendered to the page.

Cool! We just designed a simple calculator that adds `4` to whatever number you input!

#### Other Values

We can, of course, store values other than numbers. Two other primitive types of data we can store are **strings** and **booleans**:

* Strings are collections of characters like letters, words, and sentences.
* Booleans can only store one of two values `true` or `false`. 
  * Booleans are like a light switch. They are on or off. There is no in-between.

For now we'll focus on strings. The primary way we manipulate strings is with **concatenation**. That is adding two or more strings together. 

![Concatenation](../../../.gitbook/assets/concat.png)

The above program stores the string 'Hey' in a variable called `greeting` and the string 'Casey' in a variable called `name`, it then concatenates the two strings and stores the resulting string in a variable called `message`. The `message` is then displayed.

What do you think the message will display?

If you answered `'Hey Casey'` you are correct!

