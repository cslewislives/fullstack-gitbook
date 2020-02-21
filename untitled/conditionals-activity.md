# Conditionals - Activity

![Conditionals](../.gitbook/assets/image%20%2892%29.png)

Make sure you attempt the following activity before checking out the solution code. 

{% tabs %}
{% tab title="Instrcutions" %}
Using either [JSFiddle.net](www.jsfiddle.net) or [JSBin.com](www.JSBin.com) complete the following:

* Write a conditional, as concisely as possible, that prints “invalid number” if a number is zero or undefined
* How would you change the program if you were looking for numbers that were undefined but not zero?
{% endtab %}

{% tab title="Solution" %}
```javascript
let num;

if (!num) {
    console.log('Invalid Number');
}


if (!num && num !== 0) {
    console.log('Undefined but not 0');
}
```
{% endtab %}
{% endtabs %}

