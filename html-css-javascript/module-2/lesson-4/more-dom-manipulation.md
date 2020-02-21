# Callbacks and Events

### **What, Why, and When**

Callback functions are functions that are passed as parameters to another function to be invoked later.

Every time you want to run code triggered by an event, a callback function is being used.

Sometimes we want an action to take place only when the user does something, like a drop down that appears when the user clicks a button. 

### Callbacks

Any variable can be passed to a function as a parameter regardless of type. This means we can pass booleans, Strings, arrays, or even _functions_

We often pass a function as a parameter to another function. The function passed in is known as a **callback function**

Why might we want to use a **callback function?**

Sometimes we want to make sure certain things happen before we execute the code in the callback.

Take a look at the following code:

```javascript
const printName = function(name) {
  console.log(name);
};

const greeting = function(name, fn) {
  console.log('Welcome ');
  fn(name);
};

greeting('Sam', printName);
```

* We start by coding a function called `printName` that takes a parameter called `name`.
  * This is just a normal function like every other function we have written.
* Next we write the `greeting` function. 
  * The `greeting` function takes a callback function as a parameter and writes "Welcome" before calling the callback function.
  * Notice how our `greeting` prints in the proper order because we wrote "Welcome" before calling the `printName` function.

You may wonder "why not just make one function that writes `"Welcome ' + name`."

This is a contrived example to demonstrate _how_ a callback function works. Callback functions are used when we need to wait for something to happen before our callback function runs. 

For example, we may want to wait for a user to click on a button before we log them in.

### Event Listeners

Now that you've covered callbacks, it'll be a lot easier to understand **event listeners**.

Look at the following code:

{% tabs %}
{% tab title="Event1" %}
```markup
<!DOCTYPE html>
<html>
<head>
	<title>Event 1</title>
</head>
<body>

<script type="text/javascript">

	const myFunction = function () {
		console.log('you pushed a button');
	}

	document.addEventListener('keyup', myFunction);
</script>
</body>
</html>
```
{% endtab %}

{% tab title="Event2" %}
```markup
<!DOCTYPE html>
<html>
<head>
	<title>Event 2</title>
</head>
<body>

<script type="text/javascript">

	const myFunction = function (event) {
		console.log(event);
	}

	document.addEventListener('keyup', myFunction);
</script>
</body>
</html>
```
{% endtab %}

{% tab title="Event3" %}
```markup
<!DOCTYPE html>
<html>
<head>
	<title>Event 3</title>
</head>
<body>

<script type="text/javascript">

	const myFunction = function (event) {
		console.log(event.key);
	}

	document.addEventListener('keyup', myFunction);
</script>
</body>
</html>
```
{% endtab %}

{% tab title="Event4" %}
```markup
<!DOCTYPE html>
<html>
<head>
	<title>Event 4</title>
</head>
<body>

<script type="text/javascript">

	const myFunction = function (event) {
		const key = event.key;
		if (key === 'r') {
			document.write('You pressed R');
		}
		else {
			document.write('You pressed the wrong button');
		}
	}
	
	document.addEventListener('keyup', myFunction);
</script>
</body>
</html>
```
{% endtab %}
{% endtabs %}

* In `event1.html`, we are adding an **event listener** to the document that listens for a key to be pressed and invokes the callback function when a key is pressed.
* In `event2.html`, we use the `event` object. Run this file and open the console, notice that an object called `event` was created for us automatically. 
  * This will be true every time an event listener fires.
* In `event3.html`, we log just the `key` property of the event object.
* In `event4.html`, we added logic in the callback function.

