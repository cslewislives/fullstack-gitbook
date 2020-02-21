# CSS Custom Fonts

You can not only modify basic CSS properties, but also incorporate totally custom font-faces.

Many sources \(like Google\) offer font-faces online for free that can be incorporated into their HTML/CSS.

### How to Add Custom Fonts 

* Navigate to the [Google Fonts](https://www.google.com/fonts) web page and find a font-face students like.
* Hit the "Quick Use" button.

![](../../../.gitbook/assets/2-googlefonts_1.png)

* Select a few font-weights

![](../../../.gitbook/assets/2-googlefonts_2.png)

* Scroll down the page and notice how Google offers two links you need: one for the HTML page and one for the CSS file. Grab both of these links.

![](../../../.gitbook/assets/2-googlefonts_3.png)

* Open an HTML and add in the HTML reference link provided by Google

```markup
<link href="https://fonts.googleapis.com/css?family=Roboto+Condensed:400,700" rel="stylesheet" type="text/css">
```

* Then add in the CSS style provided by Google. Apply the font-face to `h1, h2, h3, h4`.

```css
h1,
h2,
h3,
h4 { 
    font-family: "Roboto Condensed", sans-serif; 
}
```

* Refresh the page in the browser and point out the custom fonts.

