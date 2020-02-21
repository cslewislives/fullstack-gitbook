# Linking JS to HTML

Now that we have some exposure working with expressions and variables in the console, we're going to start tying this all together with our HTML knowledge and write some JavaScript in our HTML file.

But first let's quickly go through how to link JavaScript documents to our HTML documents.

If your first guess is to use a link tag like we do when linking our CSS stylesheets to HTML documents, you’re pretty close!

In HTML, all JavaScript is contained inside of a `<script>` tag. 

```markup
<script></script>
```

The `<script>` tag can go either in the `<head>` or `<body>` tags, depending on where you want the JavaScript to load.

It’s generally a good idea to leave the `<script>` tag in the body at the bottom. This is because HTML is read from top to bottom and you'll want to make sure that HTML is rendered first _before_ JavaScript logic is applied.

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
	<script></script>
</body>
</html>
```

Now all we have to do is tell our `<script>` tag where our JavaScript file exists using the `src` attribute.

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
	<script src="js/index.js"></script>
</body>
</html>
```

**Notice** that we are using **relative** paths to link to our JavaScript as well.

You can also write JS inside the script tags themselves such as:

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
	<script>
    const greeting = prompt('enter your name');
    alert('Hello ' + greeting);
	</script>
</body>
</html>
```

**However,** depending on the length of the code this can create very large files, so it is best practice to separate them like CSS files.

