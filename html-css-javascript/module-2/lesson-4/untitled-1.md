# DOM Manipulation

### Static Websites

The difference between what you have been building so far in class and a website/web application like YouTube, Instagram, Gmail, Google Sheets, or Reddit is your websites have been completely static!

A **static website** is one that displays the same thing to every user and never really changes unless the developer or maintainer actively alters the HTML. Basically, there is no web programming involved.

We need to combine our HTML, CSS, and JavaScript to get data from the server to the client dynamically. 

### The DOM

The **DOM** \(Document Object Model\) is a data representation of the HTML that is rendered to the page. Often represented using a tree.

![](../../../.gitbook/assets/image%20%2834%29.png)

We can observe a visual representation of the DOM when we open the **Elements** tab in Chrome Devtools.

### DOM Manipulation

**DOM Manipulation** refers to dynamically altering what appears on the page using JavaScript. This allows us to create dynamic, interactive websites that respond to user clicks and inputs.

Check out the following code. Make sure you switch between both so you can see what the JavaScript is referencing.

{% tabs %}
{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>DOM</title>
</head>

<body>
  <h1 id="movie"></h1>
  <h2>Characters</h2>
  <ul id="character-list">
  </ul>
  
  <script src="index.js" type="text/javascript"></script>
</body>

</html>
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
// Get references to the #movie and #character-list elements
const movieH1 = document.querySelector('#movie');
const characterListUL = document.querySelector('#character-list');

// Set the inner text of the #movie element
movieH1.innerText = 'The Matrix';

// Define an array of characters to loop over
const characters = ['Neo', 'Trinity', 'Morpheus', 'Mr. Smith'];

// Define a placeholder for our character HTML list
let characterHTML = '';

// For each character, add an li element string to the characterHTML string
for (let i = 0; i < characters.length; i++) {
    const character = characters[i];
    characterHTML += `<li>${character}</li>`;
}

// Set the inner HTML of the character list to the characterHTML string
characterListUL.innerHTML = characterHTML;
```
{% endtab %}
{% endtabs %}

#### `document` Object

`document` is an object that is built-in to JavaScript that contains properties and methods for modifying the DOM.

The `document` object has a `querySelector` method that can be used to obtain a reference to an element in the DOM. It expects one string argument: the selector of the element it should look for.

The "selectors" we'd use to query an element in the DOM using JavaScript are the same as the ones we'd use to apply CSS styles \(`#id`, `.class`, etc\).

`document.querySelector` is a method that returns a DOM element which is another JavaScript object, much like the ones we've created and worked with so far. These DOM objects come with predefined properties and methods that we can use to modify how they are rendered to the page.

#### `innerText`

**Notice** how we're setting the inner text of the element with a selector of `#movie`.

`innerText` is a property available on all DOM objects and is used for setting the text inside of an element.

You can see this in action by modifying the text and refreshing your browser.

#### `innerHTML`

Notice how the list is being rendered:

* We're building a string containing the HTML to be inserted inside of the element with a selector of `#character-list`.
* We're setting the `innerHTML` property, rather than the `innerText` property in this case.
* `innerHTML` differs from `innerText` in that it can be used to update all of the content inside of an element, text and HTML tags as strings.

### `querySelectorAll`

Notice that `querySelector()` retrieves a single element, but sometimes we want to perform an operation on _all_ the elements with a certain class or _all_ the `p` elements.

{% tabs %}
{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
    <body>

        <div id="content"></div>
        <div class="example"></div>
        <div class="example"></div>
        <div class="example"></div>
        <div class="example"></div>
        <div class="example"></div>

    <script src="index.js" type="text/javascript"> </script>

</body>
</html>
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
document.querySelector('#content').textContent = 'hey';

const exampleList = document.querySelectorAll('.example');
console.dir(exampleList);

for (let i = 0; i < exampleList.length; i++){
    exampleList[i].innerText = 'All';
}
```
{% endtab %}
{% endtabs %}

The `querySelectorAll()` method returns a NodeList with all the relevant DOM elements. 

A NodeList is a special object that can be iterated through with a for loop, just like an array! Although NodeLists share a lot of properties with arrays, they aren't arrays and some array methods won't work on them.

