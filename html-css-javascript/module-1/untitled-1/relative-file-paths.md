---
description: Relative file paths connects a file with other files in its working directory.
---

# Relative File Paths

### Style.css

You'll notice that we have been referencing external stylesheets using the following code:

```markup
<link rel="stylesheet" type="text/css" href="style.css">
```

Remember that an external stylesheet is a separate file that holds the code for all of our styling.

Look at the following code and what it creates: 

{% tabs %}
{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html lang="en-us">

<head>
  <meta charset="UTF-8">
  <title>CSS Stylesheets With Relative Paths</title>

  <!-- This line is money! It points your HTML to the CSS file. -->
  <link rel="stylesheet" type="text/css" href="style.css">

<body>
  <header>
    <h1>Student Bio</h1>
  </header>

  <div class="container">

    <section id="main-bio">

      <h2>Your Name</h2>

      <img id="bio-image" src="https://placehold.it/200x200" alt="Your Name">

      <p>Write a short paragraph or two about yourself, or use placeholder text from <a href="http://www.lipsum.com/">www.lipsum.com</a></p>
    </section>

    <section id="contact-info">
      <h2>Contact Info</h2>
      <ul>
        <li><strong>Email:</strong> <a href="#">someplace@gmail.com</a></li>
        <li><strong>Github:</strong> <a href="#">sampleName</a></li>
        <li><strong>Portfolio:</strong> <a href="#">coming soon</a></li>
      </ul>
    </section>
  </div>

</body>

</html>
```
{% endtab %}

{% tab title="CSS" %}
```css
/*
Each of these CSS elements is associated with an HTML Element, Class, or ID.
Flip between this CSS file and the HTML to see how things line up.
*/

body {
    padding: 0;
    margin: 0;
    font-family: Georgia, "Times New Roman", Times, serif;
    font-size: 18px;
    line-height: 150%;
    color: #333;
    background: #efeee7;
  }
  
  header {
    background: #d21034;
  }
  
  h1 {
    padding: 20px 0;
    margin: 0;
    margin-bottom: 20px;
    font-size: 28px;
    color: #eee;
    text-align: center;
    background: #333;
  }
  
  h2 {
    font-size: 24px;
  }
  
  a {
    color: #d21034;
  }
  
  .container {
    width: 1024px;
    margin: 0 auto;
  }
  
  #main-bio,
  #contact-info,
  #bio-image {
    float: left;
  }
  
  #main-bio {
    width: 70%;
  }
  
  #contact-info {
    width: 30%;
  }
  
  #bio-image {
    width: 200px;
    height: 200px;
    margin-right: 20px;
  }
  
```
{% endtab %}

{% tab title="Browser" %}
It creates this in the browser:

![](../../../.gitbook/assets/image%20%2859%29.png)
{% endtab %}
{% endtabs %}

Remember that the `href` needs to be able to "see" the CSS file. The `href` is like our "map" to where the file is. if we move the CSS file into a folder called `assets` we must update the `href` so that the HTML file can find it.

The link should now look like this:

```markup
<link rel="stylesheet" type="text/css" href="assets/style.css">
```

Both versions of the `href` are known as Relative File paths. They look for files _relative_ to the current page.

![](../../../.gitbook/assets/image%20%2844%29.png)

In the above image you'll notice that the `style.css` and the `index.html` files are in separate folders. to reference the `assets` folder from inside the `pages` folder you must us the `../` command. This means to go up one level in the folder structure.

All together the link should look like:

```markup
<link rel="stylesheet" type="text/css" href="../assets/style.css">
```

There may be other instances in which we'll need to use relative paths to direct our computer to resources—it may be images, PDFs, JavaScript files, etc. So it's important to get a handle on how relative paths work.

{% hint style="danger" %}
The opposite of Relative File Paths are **Absolute** File Paths. **DO NOT USE THESE**. They won't make any sense on the web.

ex: `C:/Users/Jlewis/Desktop/html/index.html`
{% endhint %}

For more info check out: [https://css-tricks.com/quick-reminder-about-file-paths/](https://css-tricks.com/quick-reminder-about-file-paths/)

