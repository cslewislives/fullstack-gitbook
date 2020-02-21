# Box Model - Activity

![Box Model](../../../.gitbook/assets/image.png)

Head to [this JSBin link](https://jsbin.com/yudidic/3/edit?html,css,output) and follow the instructions below: 

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

In this activity, we'll take a look at each CSS property associated with the box model.

Open the **jsbin** in your browser. Note how BOX 1 and BOX 2 appear.

* In the CSS add `border: 3px solid #353f4f;` to both `.box1` and `.box2`.

Note the Changes.

* In the CSS add `width: 300px;` to both `.box1` and `.box2`.

Note the Changes.

* In the CSS add `padding: 30px;` to `.box1`.

Note the Changes. What will happen if we add `padding: 50px;` to `.box2`?

* Add `padding: 50px;` to `.box2`.

Note the Changes. Are the widths of the boxes the same? Why or why not?

* Add `box-sizing: border-box;` to both `.box1` and `.box2`.

Note the Changes. Are the widths of the boxes the same? What do you think `box-sizing: border-box` means?

* Add `margin: 20px;` to `.box1` and `margin: 30px;` to `.box2`.

Note the Changes. What does margin do?

**Challenge:**

Google to find how you can set just the padding above an element. How about to the left? How can you individually set the top, right, bottom, and left padding on an element in a single line?

Walk through the solution asking a different student to explain the impact of each property you add.
{% endtab %}

{% tab title="Solution" %}
```css
body {
  background-color: #F2E5D5;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
  margin: 0;
  line-height: 1.5;
  text-transform: uppercase;
}

.box1 {
  background: #57B8FF;
  color: #353f4f;
  border: 3px solid #353f4f;
  width: 300px;
  padding: 30px;
  margin: 20px;
  box-sizing: border-box;
}


.box2 {
  background: #2176AE;
  color: #bbd2e4;
  border: 3px solid #353f4f;
  width: 300px;
  padding: 50px;
  margin: 30px;
  box-sizing: border-box;
}
```

`border-box` allows us to include padding and border in the set `height` and `width`.

There is no way to include `margin` in the set height or width. `box-sizing` only has two possible values - `content-box` \(the default\) and `border-box`.
{% endtab %}
{% endtabs %}

