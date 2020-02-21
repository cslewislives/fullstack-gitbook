# Callbacks and Events - Activity

![Callbacks and Events](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
{% file src="../../../.gitbook/assets/callbacks-and-events.zip" %}

**Instructions**

Open `main.js` and add your code into this file.

1. Use `document.querySelector()` to obtain a reference to the `#test` element.
2. Add an event listener that triggers `myFunction` when the mouse enters the `#test` element.

Be sure to open your console to see the display of your event listener.

**Challenge**

Add an element in your HTML with an id of `display` and update this element's text when the event listener is triggered.

**HINT**

Check out [W3School's list of DOM Events](https://www.w3schools.com/jsref/dom_obj_event.asp) to find the appropriate event to listen for.
{% endtab %}

{% tab title="JS Solution" %}
```javascript
const myFunction = function(event) {
  console.log('Hooray!!')

  // Challenge
  document.querySelector('#display').innerText = 'I did it!';
}

// Use `document.querySelector()` to obtain a reference to the `#test` element.
const testElement = document.querySelector('#test');

// Add an event listener that triggers `myFunction` when the mouse enters the `#test` element.
testElement.addEventListener('mouseenter', myFunction);
```
{% endtab %}

{% tab title="HTML Solution" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Callbacks and Events</title>
  <link rel='stylesheet' href='main.css'>
</head>

<body>
  <h2 id="test">Move Your Mouse Over Me</h2>
  <div id="display"></div>

  <script src="main.js"></script>
</body>
</html>
```
{% endtab %}
{% endtabs %}

 

