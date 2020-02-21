---
description: Order Matters!
---

# Multiple CSS/Reset CSS

### Multiple CSS

Within HTML you can link multiple stylesheets like so:

```markup
<link  rel="stylesheet" type="text\css" href="style.css">
<link  rel="stylesheet" type="text\css" href="style2.css">
<link  rel="stylesheet" type="text\css" href="style3.css">
```

Important to note that whichever stylesheet is linked **last** will take precedence over the earlier stylesheets if they reference the same element.

### Reset CSS

In front end development, it is important to understand that:

* Each browser determines for itself how things like headers, paragraphs and tables should look
* The font and thickness is all pre-set by the browser
* The website will look different depending on the browser that is used
* Cross browser compatibility is important especially when creating an app with millions of users
* The `reset.css` file resets any default styling that the browser adds

Basic HTML without `reset.css` would print to Chrome like this:

![](../../../.gitbook/assets/image%20%2890%29.png)

Whereas the same HTML **with** `reset.css` would print like this in Chrome:

![](../../../.gitbook/assets/image%20%288%29.png)

By providing a `reset.css` you are able to control how your HTML is styled across **any** browser.

You can find a basic `reset.css` here: [https://meyerweb.com/eric/tools/css/reset/reset.css](https://meyerweb.com/eric/tools/css/reset/reset.css)

