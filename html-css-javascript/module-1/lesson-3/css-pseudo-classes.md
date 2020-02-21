# CSS Pseudo-Classes

CSS allows you to not only affect "static" properties, but also of ones that are more dynamic in nature!

CSS has keywords that can be added to selectors. These highlight the special states of the selected element.

**Great example:** CSS can hook onto the specific moment when a link is hovered over using the `:hover` pseudo-class. 

A complete list of pseudo-classes can be found here: [https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

```css
a {
  font-size: 64px;
}

a:hover {
  background-color: red;
}

a:focus {
  background-color: orange;
}

a:active {
  background-color: black;
}
```

This is a simple example, but many others build powerful UI based off this principle. 

{% hint style="info" %}
To see these in action [checkout this JSBin](https://jsbin.com/yapices/1/edit?html,css,output)
{% endhint %}

If you are interested in learning more. [http://ianlunn.github.io/Hover/](http://ianlunn.github.io/Hover/).

