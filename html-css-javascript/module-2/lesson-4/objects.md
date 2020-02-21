# Objects

### What, When, and Why

Objects store information in key/value pairs - kind of like an array, but instead of indices like 0,1,2,3... We have keys like `name`, `age`, `height`, etc. 

Objects are the backbone of JavaScript. They are used to store related information.

You'll see tons of objects throughout your career as a developer. Remember `console.log`? `console` is actually an object. Arrays are actually a special kind of object too. Objects are everywhere in JavaScript.

### New Type

So far we've seen four types of values \(booleans, Strings, numbers, and arrays\) and 3 programming tools \(conditionals, loops, and functions\). There's really only 2 more concepts that make up the core of programming: 

* Objects
* Event listeners

Once we know these, we can make virtually anything. It's just a matter of using our flowcharting skills to figure out how to arrange the pieces."

Let's tick one more off the list and learn about objects. **Objects** — like arrays — are containers for multiple values. Unlike arrays though, objects have a **property** and a **property value**. 

Where arrays are like a list, objects are like a dictionary with key/value pairs.

Take a look at the code below:

```javascript
// We store our `object` in a variable
const carObject = {
  // For readability we can use the following formatting of `property`: `property value` 
  // followed by a comma
  make: "Jeep",
  model: "Wrangler",
  tires: 4,
  mileage: 110000
};
```

**Object properties** can be accessed in 2 ways: **dot notation** or **bracket notation**.

Dot notation is generally preferable, but bracket notation has 2 common uses:

* When the name of the property being accessed is stored in a variable
* When the name of the property being accessed has special characters

Look through the code below, taking note of when bracket notation and dot notation are used:

```javascript
const player1 = {
  name: 'Link',
  health: 55,
  strength: 332,
  isAlive: true,
  points: 5000
};

//dot notation
console.log(player.name);
console.log(player.isAlive);

//bracket notation
const propName = 'health';
console.log(player1[propName]);

//we can use these same techniques to add or set property values
player1.speed = 5;
console.log(player1);

player1.points = 5300;
console.log(player1);
```

