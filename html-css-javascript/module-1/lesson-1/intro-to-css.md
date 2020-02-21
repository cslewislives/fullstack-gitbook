---
description: Making it Pretty
---

# Intro to CSS

### CSS Basics

* CSS stands for Cascading Style Sheets
* CSS, in addition to HTML, is read from top-to-bottom
* CSS describes how HTML elements are to be displayed on screen, paper, or in other media
* CSS saves a lot of work. It can control the layout of multiple web pages all at once
* External **stylesheets** are stored in CSS files 

![CSS property](https://lh5.googleusercontent.com/KOiTs8PtvT82KvnNTxdVAC5sn8uBNzco2cPkrHu8JBFIkIokCAZkWbKRMqvSqeJFdDoQpttOTPxqwMId4md9Ro1DUcmoc-9MoJFcTR0h8StxZPnezV6ey-4nnCJyGkgGDQQW49FlHH0)

* CSS works by hooking onto selectors added into HTML using classes and identifiers.
* Once hooked, we apply styles to those HTML elements using CSS.

### Frequently Used CSS

* **Font / Color:**
  * `color:`
    * Sets color of text.
  * `font-size:`
    * Sets size of the font.
  * `font-style:`
    * Sets italics.
  * `font-weight:`
    * Sets bold.
* **Background:** 
  * `background-color:`
    * Sets background color.
  * `background-image:`
    * Sets background image.
* **Alignment / Spacing:**
  * `padding:` \(top/right/bottom/left\)
    * Adds space between element and its own border.
  * `margin` \(top/right/bottom/left\):
    * Adds space between element and surrounding elements.
  * `float:`
    * Forces elements to the sides, centers, or tops.

{% hint style="info" %}
There are a **lot** of CSS properties. Feel free to [check out this link](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) to see more and play around with them!
{% endhint %}

### Example CSS sheet

Apply the following CSS and link to it in your HTML. Make sure your CSS file and your HTML file are in the same folder.

{% tabs %}
{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Example</title>
  <!-- Link to your CSS below -->
  <link rel="stylesheet" type="text/css" href="index.css" />
</head>
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
</html>
```
{% endtab %}

{% tab title="CSS" %}
```css
body {
  background-color: #F5DEB3;
  font-family: Arial, Helvetica, sans-serif;
}

h1 {
  text-align: center;
  color: maroon;
  font-size: 48px;
  text-decoration: underline;
}

p {
  color: limegreen;
}
```
{% endtab %}

{% tab title="Browser" %}
The web page now looks like this:

![](../../../.gitbook/assets/image%20%28105%29.png)
{% endtab %}
{% endtabs %}



