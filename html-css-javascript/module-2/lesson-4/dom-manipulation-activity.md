# DOM Manipulation - Activity

![DOM Manipulation](../../../.gitbook/assets/image%20%2896%29.png)

As always attempt the activity yourself before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
{% file src="../../../.gitbook/assets/dom\_manipulation.zip" caption="DOM Manipulation Files" %}

**Instructions:**

* Open `index.html` in your code editor and take a moment to study the code.
* Then open the file in your web browser and notice how you are prompted for various pieces of information that correspond to the incomplete HTML being rendered to the page.
* Use the values collected by each prompt to update their corresponding element, e.g. the `name` collected from the prompt should update the element with an id of `#name`.
* The `#name`, `#color`, and `#season` elements should be updated with the `innerText` property.

**Challenge:**

The `#interests` element should be updated with the `innerHTML` property. For this element, use the array of interests collected and a `for-loop` to insert one `li` tag for each interest inside of the `#interest` element.

**Hints:**

* Have your console open ready to check for errors.
* If you are unsure about the value of a variable, print it to the console!
* Be careful about how you name your variables! It's common for code not to work due to a typo, casing matters!
* Refer to the previous example if you get stuck!
{% endtab %}

{% tab title="JS Solution" %}
```javascript
// Prompt the user for some information
const name = prompt('What is your name?');
const color = prompt('What is your favorite color?');
const season = prompt('What is your favorite season?');
let interests = prompt('What are you interested in?\nSeperate interests with a comma.\ne.g. hiking, fishing golf, etc.');

// Split is a built-in method that turns a string into an array of smaller strings, splitting them by a specified seperator (', in this case')

interests = interests.split(',');

// Getting references to the DOM elements we'll need
let nameSpan = document.querySelector('#name');
let colorSpan = document.querySelector('#color');
let seasonSpan = document.querySelector('#season')
let interestUL = document.querySelector('#interests');

// Setting the innerText of the name, color and season span elements
nameSpan.innerText = name;
colorSpan.innerText = color;
seasonSpan.innerText = season;

// Creating a string to hold the HTML we'll insert into the list
let interestHTML = '';

// Loop over the array of interests, add an li element containing the interest to the interestHTML string
for (let i = 0; i < interests.length; i++) {
  const interest = interests[i];
  interestHTML += `<li>${interest}</li>`;
}

// Set the inner HTML of the interestUL to the interestHTML string
interestUL.innerHTML = interestHTML;

```
{% endtab %}
{% endtabs %}

