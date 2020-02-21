# Responsive Design

### Media Queries

Media Queries define how CSS styles are applied in relation to the characteristics of the device viewport.

Through media queries we can change the way a web page is displayed based on width, height, orientation, and even media type \(screen, paper, braille, etc\). 

Media queries effectively create "conditional css". If a particular width of the screen is met, then the CSS within that media query will be triggered. Otherwise it will be ignored.

These are what allow Bootstrap CSS to have a fully mobile responsive website. But it's important to be familiar with media queries so you can roll out your own custom mobile responsive designs in the future.

And always remember that Media queries must be declared **last.**

For example:

{% tabs %}
{% tab title="CSS" %}
```css
 /**
 * Media Query Demo (note the commented rules)
 **/

 * {
  box-sizing: border-box;
}

/*
  The background color will be #ccc
  at browser widths above 768px
*/
body {
  /* Typography */
  font-size: 18px;
  line-height: 27px;

  /* Visual */
  background-color: #ccc;
}

/*
  The width of the wrapper will be 1024px
  at browser widths above 768px
*/
.wrapper {
  /* Box-model */
  width: 1024px;

  /* Positioning */
  margin: 40px auto;
}

#main-content,
#sidebar {
  /* Box-model */
  width: 500px;
  padding: 30px;
}

#main-content {
  /* Positioning */
  float: left;

  /* Visual */
  background: #fff;
}

#sidebar {
  /* Positioning */
  float: right;

  /* Visual */
  background: #eee;
}

/*
  These rules take effect when the browser's width
  is either 768px or less.
*/
@media screen and (max-width: 768px) {
  /* The body's bg color will be #333 */
  body {
    background-color: #333;
  }

  /* The wrapper's width will be 600px */
  .wrapper {
    width: 600px;
  }
}
```
{% endtab %}

{% tab title="HTML" %}
```markup
<!-- Media Query Demo (check the CSS page) -->
<!doctype html>
<html lang="en-us">

<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>HTML</title>

  <link rel="stylesheet" type="text/css" href="reset.css">
  <link rel="stylesheet" type="text/css" href="style.css">

</head>

<body>

  <div class="wrapper">

    <section id="main-content">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi ut tellus sed felis consectetur auctor eget non justo. Nunc in laoreet nunc. Quisque accumsan tincidunt neque, at dictum turpis. In hac habitasse platea dictumst. </p>
    </section>

    <section id="sidebar">
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi ut tellus sed felis consectetur auctor eget non justo. Nunc in laoreet nunc. Quisque accumsan tincidunt neque, at dictum turpis. In hac habitasse platea dictumst. </p>
    </section>

  </div>

</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Full size view:

![](../../../.gitbook/assets/image%20%2877%29.png)

Resized view:

![](../../../.gitbook/assets/image%20%2810%29.png)
{% endtab %}
{% endtabs %}

The `@media screen` section means that it has particular styling that kicks in when the page is less than **768px** wide.

**Remember** that like HTML, CSS is read from top to bottom. You should always start with larger screen width thresholds on top, and work your way down.

{% hint style="info" %}
To see this code in action [checkout this video!](https://www.youtube.com/watch?v=x_wlcp-W27c)
{% endhint %}

### Viewport

Viewport refers to the display being used to view the website.

By default, mobile devices with small screen, high resolution viewports may render content at a typical desktop screen ratio \(scaled down at the smaller screen size\).

![No Viewport Content Scaling](https://lh5.googleusercontent.com/CqAyzXLKQF9af2PAJyMp33YMs-kFMguPkPt9bkUopBqHGiYqM51ZKy1gEbI-soh6pf0VNP-9q4F7TcWxHePqu0NDPgrHMD0MHglBpUVlU2UjvAJadRoy8wgfhztt7fF7gQTsxB9Wd0s)



![Yes Viewport Content Scaling](https://lh3.googleusercontent.com/_blDAuZFvshXiTWzTramvOy9t3fU5SNwCMNByfBalhcnbjOh4K8Axcf7xkB9W8O-YMKfSl3cFhZ8JQ52dQDR20VVYQEJI0HphZThuuu_EU514WPM5CGOcjFNN1ffn30veZcm0jTaqX0)

To fix this Just include this line in the head of your HTML:

```markup
<meta name="viewport" content="width=device-width, initial-scale-1">
```

Then include media queries for various sized screens in the CSS:

```css
@media screen and (max-width: 768px)
@media screen and (max-width: 480px)
```

{% hint style="info" %}
To learn more [check out this link!](http://www.w3schools.com/css/css_rwd_viewport.asp.)
{% endhint %}

