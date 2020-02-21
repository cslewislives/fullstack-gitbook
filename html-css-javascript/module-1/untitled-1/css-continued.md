# CSS Combinators

### Combinators

In the previous lesson, we used two types of selectors - elements \(like `h1` and `body`\) and classes \(like `.dark` and `.big`\).

Sometimes we want to be more specific than this. Maybe we want to make every paragraph that's in a `div` blue, but _only_ paragraphs inside `div`s, not all paragraphs.

We can do this by including a combinator in between selectors to target a more specific subset of elements.

There are four different combinators in CSS:

* Descendant Selector
* Child Selector
* Adjacent Sibling Selector
* General Sibling Selector

#### **Descendant selector \( space \)**

Descendant selectors selects elements that are descendants of the specified elements

```css
div p {
  background: teal;
}
/* this will make the background of all p tags that are descendants of div tags teal */
```

#### **Child selector \( &gt; \)**

Child selectors select elements that are IMMEDIATE children of the specified element

```css
div > p {
  background: teal;
}
/* this makes the background of all p tags that are immediate children of a div tag teal */
```

Child selectors and descendant selectors are similar, but not quite the same. A good analogy here would be that my daughter is my child and my descendant. My granddaughter is not my child, but she is my descendant

#### **Adjacent sibling selector \( + \)**

Adjacent sibling selectors selects elements that are placed immediately after the specified element

```css
div + p {
  background: teal;
}
/* this makes the background of all p tags that are immediately after a div tag teal */
```

#### **General sibling selector \( ~ \)**

General sibling selectors selects ALL elements that are siblings of a specified element

```css
div ~ p {
  background: teal;
}
/* this makes the background of all p tags that are the same level as a div tag teal */
```

#### **Grouping \( , \)**

You can write groups of selectors separated by commas to apply the same rule to multiple elements

```css
h1, section {
  background: teal;
}
/* this makes the background of all h1 tags AND section tags teal */
```

#### Chaining Combinators

Multiple combinators can be chained together as well

```css
h1 > div > p {
  style properties for the child p tag of the child div tag of the h1 tag
}
```

### Complete Example of Selectors

{% tabs %}
{% tab title="CSS" %}
```css
Uncomment the different selectors to see them in action
/* ---Descendent Selector--- */
/* div p {
    color: red;
} */


/* ---Child Selector--- */
/* div > p {
    color: red;
} */


/* ---Adjacent Selector--- */
/* div + p {
    background-color: yellow;
} */


/* ---General Sibling Selector--- */
/* div ~ p {
    background-color: yellow;
} */
```
{% endtab %}

{% tab title="HTML" %}
```markup
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>CSS Combinators</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" type="text/css" media="screen" href="style.css" />
</head>

<body>

  <div>
    <h1>Header</h1>
  </div>

  <p>Paragraph 1</p>
  <p>Paragraph 2</p>
  <div>
    <p>Paragraph 3</p>
    <section>
      <p> Paragraph 4 </p>
    </section>
  </div>

</body>

</html>
```
{% endtab %}

{% tab title="Browser" %}
Descendant Selector:

![](../../../.gitbook/assets/image%20%2886%29.png)

 Child Selector:

![](../../../.gitbook/assets/image%20%2893%29.png)

Adjacent Sibling Selector:

![](../../../.gitbook/assets/image%20%2825%29.png)

General Sibling Selector:

![](../../../.gitbook/assets/image%20%2818%29.png)
{% endtab %}
{% endtabs %}

