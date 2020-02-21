# CSS Specificity

### What is specificity?

* Sometimes an element can have conflicting CSS properties, the browser must then decide which is most relevant to the element.
* You can think of CSS specificity as a hierarchy! 
* Your CSS properties will overlap based on those hierarchies.

{% tabs %}
{% tab title="HTML" %}
```markup
<body>
  <div>
    <h1 class="new-text">Specificity!<h1>
    <h2>This is an h2</h2>
    <h3>This is an h3</h3>
    <h4>This is an h4</h4>
    <h5>This is an h5</h5>
    <h6>This is an h6</h6>
  </div>
</body>
```
{% endtab %}

{% tab title="CSS" %}
```css
.new-text {
    color: red;
}

h1 {
    color: blue;
}
```
{% endtab %}

{% tab title="Browser" %}
Due to the specificity of the class the browser will render this:

![](../../../.gitbook/assets/image%20%2876%29.png)
{% endtab %}
{% endtabs %}

{% hint style="info" %}
For more info [check out this link!](https://www.w3schools.com/css/css_specificity.asp)
{% endhint %}

