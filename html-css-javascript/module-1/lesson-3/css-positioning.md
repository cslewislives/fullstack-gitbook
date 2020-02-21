---
description: Various Position Types
---

# CSS Positioning

Within CSS there are a few ways to position your content on the screen. They are:

* **Static**
  * Default positioning, i.e. no positioning given 

{% tabs %}
{% tab title="CSS" %}
```css
/**
 * Static: Default positioning
 **/

 .box-set {
  height: 400px;
  background: darkgray;
}

.box {
  width: 150px;
  height: 150px;
  background: #2db34a;
  border: 2px solid black;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Static CSS:

![](../../../.gitbook/assets/image%20%28100%29.png)
{% endtab %}
{% endtabs %}

* **Relative**
  * Positions elements relative to their static location in the document. 
  * These elements behave with and interact with other elements the same way they would as if they were positioned statically, except that you can use the top/right/bottom/left properties to move the elements after they have been placed into the document flow.

{% tabs %}
{% tab title="CSS" %}
```css
/**
 * Relative Position: sets boxes relative to its original location
 * (i.e. below or left of where the element would normally be)
 **/

.box-set {
  position: relative;
  height: 400px;
  background: darkgray;
}

.box {
  /* relative positioning */
  background: #2db34a;
  height: 150px;
  width: 150px;
  position: relative;
  border: 2px solid black;
}

.box-1 {
  top: 20px;
}

.box-2 {
  left: 40px;
}

.box-3 {
  bottom: -10px;
  right: 20px;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Relative CSS:

![](../../../.gitbook/assets/image%20%28106%29.png)
{% endtab %}
{% endtabs %}

* **Absolute**
  * Positions elements relative to the nearest positioned ancestor \(non-static\). 
  * They are taken out of the flow of the document, taking up no space when placing other elements.
  * These elements will move in the viewport as you scroll \(unlike fixed\).

{% tabs %}
{% tab title="CSS" %}
```css
/**
 * Absolute Position: anchors element to the first element (overall box)
 **/

.box-set {
  height: 400px;
  background: darkgray;
  position: relative;
}

.box {
  /* Absolute Position */
  position: absolute;
  width: 150px;
  height: 150px;
  background: #2db34a;
  border: 2px solid black;
}

/* Box rules: percentages define anchors (i.e. position of each box relative to enclosing box) */

.box-1 {
  top: 6%;
  left: 2%;
}

.box-2 {
  top: 0;
  right: -40px;
}

.box-3 {
  bottom: -10px;
  right: 20px;
}

.box-4 {
  bottom: 0;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Absolute CSS:

![](../../../.gitbook/assets/image%20%2863%29.png)
{% endtab %}
{% endtabs %}

* **Fixed**
  * Positions elements relative to the top left of the browser window. 
  * Similar to absolute, except the containing block is the whole viewport. 
  * These elements will remain in the same place in the viewport as you scroll.

{% tabs %}
{% tab title="CSS" %}
```css
/**
 * Fixed Position: Anchors element to the browser
 **/

.box-set {
  position: relative;
  height: 400px;
  background: darkgray;
}

.box {
  background: #2db34a;
  border: 2px solid black;
  width: 150px;
  position: fixed;
  height: 150px;
}

/* Box rules: percentages define anchors (i.e. position of each box relative to browser window) */

.box-1 {
  top: 6%;
  left: 2%;
}

.box-2 {
  top: 0;
  right: -40px;
}

.box-3 {
  bottom: -10px;
  right: 20px;
}

.box-4 {
  bottom: 0;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Fixed CSS:

![](../../../.gitbook/assets/image%20%2815%29.png)
{% endtab %}
{% endtabs %}

* **Z-Index**
  * Allows us to position elements on top of one another.

{% tabs %}
{% tab title="CSS" %}
```css
/**
 * Z-Index: let's us position elements on top of each other (the z-axis controls depth position)
 **/

.box-set {
  position: relative;
  height: 400px;
  background: darkgray;
}

.box {
  position: absolute;
  width: 150px;
  height: 150px;
  background: #2db34a;
  border: 2px solid black;
}

.box-1 {
  top: 10px;
  left: 10px;
}

.box-2 {
  bottom: 10px;
  left: 70px;
  z-index: 3;
}

.box-3 {
  top: 10px;
  left: 130px;
  z-index: 2;
}

.box-4 {
  bottom: 10px;
  left: 190px;
  z-index: 1;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Z-index CSS:

![](../../../.gitbook/assets/image%20%2858%29.png)
{% endtab %}
{% endtabs %}

* **Display: none**
  * Allows us to hide specific elements from the view. 
  * Useful because it can activate and deactivate elements. \(Compare with `visibility: hidden;`, which also hides elements but not the space they take up.\)

{% tabs %}
{% tab title="CSS" %}
```css
.box-set {
  position: relative;
  height: 400px;
  background: darkgray;
}

.box {
  position: relative;
  width: 150px;
  height: 150px;
  background: #2db34a;
  border: 2px solid black;
}

.box-1 {
  top: 20px;

  /* Hides element as if it's not there (compare with "visibility: hidden;"). */
  display: none;
}

.box-2 {
  left: 40px;
}

.box-3 {
  right: 20px;
  bottom: -10px;
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Positioning Demo</title>
  <link rel="stylesheet" href="reset.css">
  <link rel="stylesheet" href="assets/style.css">
</head>

<body>
  <div class="box-set">
    <figure class="box box-1">Box 1</figure>
    <figure class="box box-2">Box 2</figure>
    <figure class="box box-3">Box 3</figure>
    <figure class="box box-4">Box 4</figure>
  </div>
</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Display: none CSS:

![](../../../.gitbook/assets/image%20%2841%29.png)

Visibility: hidden;

![](../../../.gitbook/assets/image%20%2873%29.png)
{% endtab %}
{% endtabs %}



