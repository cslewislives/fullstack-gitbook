# Bootstrap Components

We'll spend a few moments showing you how to utilize the simplest of Bootstrap CSS or components.

Head to [https://getbootstrap.com/](https://getbootstrap.com/)

![](../../../.gitbook/assets/6-bootstrapdemo_1.png)

Grab the CSS CDN content

![](../../../.gitbook/assets/6-bootstrapdemo_2.png)

Add the CDN to an HTML file

```markup
<!DOCTYPE html>
<html lang="en-us">

<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Coding Boot Camp!</title>

  <!-- We link our html to the Bootstrap CDN -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">

</head>
```

Head to the Documentation section, then to Components in the left pane.

Scroll down to buttons and notice the basic options for creating buttons.

![](../../../.gitbook/assets/6-bootstrapdemo_4.png)

Scroll to the Examples section and notice the differences between primary, success, danger, etc. buttons

Scroll a bit further and notice the options for sizing

![](../../../.gitbook/assets/6-bootstrapdemo_6.png)

Use the button class names found there as a model for creating a fancier button. Use those classes on the HTML below.

{% tabs %}
{% tab title="HTML" %}
```markup
<body>

  <!-- Regular Buttons -->
  <h1>Here are some non-fancy buttons</h1>
  <button>Boring Button</button>
  <button>Boring Button</button>

</body>
```
{% endtab %}

{% tab title="Browser" %}
![](../../../.gitbook/assets/6-bootstrapdemo_7.png)
{% endtab %}
{% endtabs %}

Then run the html in the browser and take a look at the fancier buttons.

{% tabs %}
{% tab title="HTML" %}
```markup
<body>

  <!-- Regular Buttons -->
  <h1>Here are some non-fancy buttons</h1>
  <button>Boring Button</button>
  <button>Boring Button</button>

  <!-- Bootstrap Enhanced Buttons -->
  <h1>Here are fancy bootstrap buttons</h1>
  <button class="btn btn-primary btn-lg">Fancy Button</button>
  <!-- Note the specific Bootstrap classes -->
  <button class="btn btn-danger btn-lg">Fancy Button</button>
  <!-- Note the specific Bootstrap classes -->

</body>
```
{% endtab %}

{% tab title="Browser" %}
![](../../../.gitbook/assets/6-bootstrapdemo_8.png)
{% endtab %}
{% endtabs %}

