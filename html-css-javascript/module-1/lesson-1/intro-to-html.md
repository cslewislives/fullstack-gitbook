---
description: Getting Stuff on the Page
---

# Intro to HTML

### HTML Facts

* HTML is used to make every website.
* HTML is the language that determines what appears on web pages.
* HTML is made up of opening and closing tags.
* HTML is the skeleton of the web page, we use elements to dictate where everything needs to be.

### Anatomy of HTML Elements

```markup
<p> Some text here. </p>
```

* The code above is an example of an HTML element.
* `<p>` is the opening tag
* `Some text here` is the content
* `</p>` is the closing tag

```markup
<img src="sample.png" />
```

* A few tags are self-closing.
* HTML elements can have attributes. 
* Attributes provide additional info about an element. 
* They come in name/value pairs: `name = “value”`.
* `/>` is the self closing tag

### Other HTML Elements

We’ve seen demonstrations of the &lt;p&gt; and &lt;img&gt; elements, but what other elements do we have at our disposal?

* `<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` are used to display headings
* `<ul>` is an unordered list
  * Such as bullet points
* `<ol>` is an ordered list
  * Such as numbered lists
* `<li>` is used to display list items
* `<div>` is used to create divisions in the page
* `<a>` is used as a link

### Examples

Copy and paste the following code into your editor [\(or JSBin\)](http://www.jsbin.com) and display it in your browser.

{% tabs %}
{% tab title="HTML" %}
```markup
<body>
  <div>
    <h1>This an h1</h1>
    <h2>This is an h2</h2>
    <h3>This is an h3</h3>
    <h4>This is an h4</h4>
    <h5>This is an h5</h5>
    <h6>This is an h6</h6>

    <p>Meanwhile, this is a p element</p>

    <ul>
      <li>This is what an</li>
      <li>item in an unordered list</li>
      <li>will look like!</li>
    </ul>
  </div>
  <div>
    <p>This is part of a separate div!</p>
    <ol>
      <li>Alternatively, this is what</li>
      <li>an ordered list<li>
      <li>will look like</li>
      <li>We can even link to <a href="https://www.google.com">Google!</a></li>
    </ol>
  </div>
</body>
```
{% endtab %}

{% tab title="Browser" %}
It should look like this in your browser:

![](../../../.gitbook/assets/image%20%2883%29.png)
{% endtab %}
{% endtabs %}

