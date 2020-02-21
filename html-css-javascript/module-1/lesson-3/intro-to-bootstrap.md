# Intro to Bootstrap

![](https://lh6.googleusercontent.com/0a-PPKC35sPxR-QLQa4pM2g1gnfiqMkQ6cccOHiiSnCx700xzCvdtHfo9887Q3W1z5TYGKdGaVh-K01_WIXXmCFW2nVj1JlHFITHlZ3_PjPkDUs_BxvhIyQC7i9BvFDmdN8erWzuP4I)

Twitter Bootstrap is a free collection of tools for creating websites and web applications. 

It comes with a pre-built design template for typography, forms, buttons, navigation, UI elements and JavaScript.

You can find the documentation here: [http://getbootstrap.com/](http://getbootstrap.com/)

## Why Bootstrap?

### It’s a UI Kit.

Familiarize yourself with the UI features it offers via the documentation.

Once Bootstrap is active, you can simply copy snippets from the documentation to save yourself major time of creating elements yourself.

![](../../../.gitbook/assets/image%20%2813%29.png)

The above site was created without the developer needing to write a single line of CSS.

Checkout the code used to create it:

```markup
<!-- Reset.css -->
<!-- Bootstrap-Powered HTML -->

<!-- Students:
  1. Where is the HTML document drawing its styles from?
  2. How does our browser know which element to style in which way? (ex: button face or background banner)
-->
<!DOCTYPE html>
<html lang="en-us">

<head>

  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Coding Boot Camp!</title>

  <!-- We link our html to the Bootstrap CDN -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">

</head>

<body>

  <!-- Container Div -->
  <div class="container">

    <!-- Section 1: Navbar-->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">

      <!-- Our brand / logo -->
      <a class="navbar-brand" href="#">The Coding Boot Camp</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

        <!-- Collapsible button -->
      <div class="collapse navbar-collapse" id="navbarNavDropdown">
        <ul class="navbar-nav ml-auto">

          <!-- The links of our navbar -->
          <li class="nav-item active">
            <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
          </li>

          <li class="nav-item">
            <a class="nav-link" href="#">Features</a>
          </li>

          <!-- a Dropdown menu -->
          <li class="nav-item dropdown">

            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              Dropdown
            </a>

            <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
              <a class="dropdown-item" href="#">Action</a>
              <a class="dropdown-item" href="#">Another action</a>
              <a class="dropdown-item" href="#">Something else here</a>
            </div>

          </li>
        </ul>
      </div>
    </nav>

    <!-- Jumbotron element -->
    <div class="jumbotron">

      <!-- centered text -->
      <h1 class="text-center"><strong>Awesome Header</strong></h1>
      <h2 class="text-center">Smaller Awesome Header</h2>
      <h3 class="text-center">Even Smaller Header</h3>

      <!-- button with predefined style rules -->
      <p class="text-center">
        <a class="btn btn-primary btn-lg" href="#" role="button">
          <span class="fa fa-envelope"></span> Learn more</a>
      </p>
    </div>

    <!-- a Bootstrap row with columns -->
    <div class="row">

      <!-- At large+ screens takes up half width (6/12) -->
      <div class="col-lg-6">

        <!-- centered image with thumbnail rules -->
        <img class="img thumbnail center-block" src="http://legacy.nerdywithchildren.com/wp-content/uploads/2013/06/ComfyChildKeyboard.jpg" alt="KidComputer" width="50%">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quis, molestiae modi accusantium animi magnam veniam, impedit asperiores sint consequuntur debitis fugit quibusdam dolor, iusto sed porro ab minus voluptatibus amet.</p>
      </div>

      <!-- At large+ screens takes up half width (6/12) -->
      <div class="col-lg-6">
        <img class="img thumbnail center-block" src="https://images.unsplash.com/photo-1477453559950-e541fa922120" alt="LittleCoder" width="50%">
        <p> Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus, maiores, quos. At, animi, facilis. Alias itaque ab minima rerum, eaque animi nesciunt harum nemo est cumque voluptas, qui reprehenderit atque.</p>
      </div>
    </div>
  </div>

  <!-- jQuery, javascript file for the Bootstrap's javascript file to function -->
  <script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>

  <!-- Bootstrap's javascript file that allows the dropdown menu to work  -->
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js"></script>

</body>

</html>
```

Notice that we do not link to our own stylesheet but rather to a stylesheet located on the web via a CDN \(Content Delivery Network\).

This CSS file has pre-styled "classes" which are styled whenever you call an element that class. This is the case with the Jumbotron for instance.

{% tabs %}
{% tab title="Jumbotron HTML" %}
```markup
<!-- JUMBOTRON ELEMENT -->
<div class="jumbotron">

  <h1 class="text-center"><strong>Awesome Header</strong></h1>
  <h2 class="text-center">Smaller Awesome Header</h2>
  <h3 class="text-center">Even Smaller Header</h3>

  <p class="text-center">
    <a class="btn btn-primary btn-lg" href="#" role="button">
      <span class="fa fa-envelope"></span> Learn more</a>
  </p>
</div>
```
{% endtab %}

{% tab title="Jumbotron Browser" %}
![](../../../.gitbook/assets/image%20%2867%29.png)
{% endtab %}
{% endtabs %}

Visit [https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css](https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css). \(This is the stylesheet that you are linking to when you add it to your HTML.\)

Then do a `ctrl+f` and search for the term `jumbotron`. Notice that the word appears in the stylesheet, meaning that, whenever we create a block called `jumbotron`, we are utilizing CSS we didn't have to write for this block.

#### Predefined Styles

This is a big deal because we are now using predefined CSS styles that someone else made.

Predefined CSS styles mean that a front-end developer has a "starting place" for creating web layouts. Instead of having to create the styles for every element, they can quickly borrow from commonly used elements and build layouts with best practices.

To checkout some of the predefined components checkout: [https://getbootstrap.com/docs/4.0/components](https://getbootstrap.com/docs/4.0/components)

Notice the variety of components. Many websites only require these things. This makes creating a web site incredibly easy and fast.

### Mobile Responsiveness

![](https://lh4.googleusercontent.com/ZRFYFm7Vk5B88A5pOU0UytXmzOAlxgpx6uIveyGojEKgyNcfwWY07mJwxqUgJoID_7rGqLXJ5P20THla2_oxYd86tf0LnMqjYWGFpRNbIXA-Crnqds4MSGrkfJjHOtEN-9tk4ei8BTA)

Bootstrap makes it easy to build mobile-responsive websites. 

This means that your website will look “good” automatically when viewed on screens ranging from monitors to tablets to phones

Bootstrap has these capabilities built in.

