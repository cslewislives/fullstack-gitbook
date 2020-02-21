---
description: Still Making it Pretty
---

# Intro to CSS Cont.

### Specifying Selectors

* Id’s can be used to give an HTML element a unique identifier that you can use to stylize that specific element

{% tabs %}
{% tab title="HTML" %}
```markup
<body>
  <div>
    <h1 id="fancy">This an h1</h1>
    <h2>This is an h2</h2>
    <h3>This is an h3</h3>
    <h4 id="ugly">This is an h4</h4>
    <h5>This is an h5</h5>
    <h6>This is an h6</h6>
  </div>
</body>
```
{% endtab %}

{% tab title="CSS" %}
```css
/* use the following notation to point to the id: fancy */
#fancy {
  font-family: "Brush Script MT", "Brush Script Std", cursive;
  color: deeppink;
}

#ugly {
  font-family: "Comic Sans MS";
  color: olive; 
}
```
{% endtab %}

{% tab title="Browser" %}
It should look like this:

![](../../../.gitbook/assets/image%20%2881%29.png)
{% endtab %}
{% endtabs %}

* Classes can be used to assign HTML elements to a group. 
  * CSS can use these classes as a selector to style the elements of the group.

{% tabs %}
{% tab title="HTML" %}
```markup
<body>
  <div>
    <h1>This an h1</h1>
    <h2>This is an h2</h2>
    <h3 class="orange">This is an h3</h3>
    <h4 class="orange">This is an h4</h4>
    <h5>This is an h5</h5>
    <h6>This is an h6</h6>
  </div>
</body>
```
{% endtab %}

{% tab title="CSS" %}
```css
/* Use this notation to call on classes with the name orange */
.orange {
  color: darkorange;
}
```
{% endtab %}

{% tab title="Browser" %}
This is what it looks like:

![](../../../.gitbook/assets/image%20%2832%29.png)
{% endtab %}
{% endtabs %}



