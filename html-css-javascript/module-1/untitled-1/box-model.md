# Box Model

In CSS, every element can be considered to fit within a series of boxes. Each box can be individually adjusted to provide spacing between elements or to fill in elements with colors.

The box model applies to all elements whether they are text, images, div sections, etc.

![The Box Model](../../../.gitbook/assets/image%20%2862%29.png)

### Calculate Size 

Using the image below, calculate the size of the Blue Box:

{% tabs %}
{% tab title="Question" %}
Make sure you calculate the size both ways, including margins and not including margins.

![](../../../.gitbook/assets/image%20%2895%29.png)
{% endtab %}

{% tab title="Answer" %}
![](../../../.gitbook/assets/image%20%2839%29.png)
{% endtab %}
{% endtabs %}

Notice that the padding, border, and margin need to be counted **twice** in the calculation because there is padding on the left **AND** right, there is a margin on the left **AND** right, and there is a border on the left **AND** right.

We are calculating the actual height and width that this element takes up on the page. This is **NOT** the same as the `width` and `height` CSS properties.

CSS `width` and `height` set the width or height of the content area only. Padding, border, and margins added will increase actual space the element takes up.

