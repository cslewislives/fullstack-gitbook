# Build Media Query - Activity

{% file src="../../../.gitbook/assets/06-stu\_media-queries.zip" caption="Media Queries Activity" %}

Open the file `media_solved.html` in chrome. Don't do anything other than run it. Widen and shrink the page and notice that whereas your previous version of the code stacked the two boxes on top of each other, this version creates a nice degree of padding for separation and then stacks the two boxes on top of each other below a `max-width` of 768px.

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

Now in the `unsolved` folder follow these instructions

Add more styling to the media query provided in `css/style.css` to create padding and margins for the two boxes when the page is below a `max-width` of 768px.

**Note:** This isn't easy. Just give it your best shot. Even if you don't get the exact solution, but are able to better understand how media queries work, that's a solid takeaway.

**Challenge:**

Add more styling to the CSS file such that the `@media screen` code adjusts the padding and width for the two boxes when the page is below a `max-width` of 980px.

**Hint:** Because CSS files are read from top to bottom, you want to make sure that your _larger_ media query widths are first, and _smaller_ media query widths come after.
{% endtab %}

{% tab title="Solution Code" %}
```css
@media screen and (max-width: 768px) {
  body {
    background-color: #333;
  }

  .wrapper {
    /* Box-model */
    width: 100%;
    padding: 20px;
  }

  #main-content,
  #sidebar {
    width: 100%;
  }

  #sidebar {
    margin-top: 40px;
  }
}
```
{% endtab %}
{% endtabs %}

