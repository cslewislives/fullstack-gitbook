---
description: Floats are pretty tricky.
---

# Floats

### Flow

![](../../../.gitbook/assets/image%20%2843%29.png)

Flow is the idea that every single element — text, images, links, sections, etc. — all take up a set amount of space on the screen.  

These elements, by default, won't stack on top of one another so instead they have to find ways to "flow" around one another. A big part of CSS is in managing how elements will fit into this flow.

Unfortunately there is no 'drag-and-drop' in web development just yet, and the tools that exist to do so often produce terrible code. So, as developers, we do NEED to learn this stuff at least at a basic level.

#### Block-Elements

By default, web clients render many HTML elements as block elements. Paragraphs, headers, divs and more receive this treatment.

![](../../../.gitbook/assets/image%20%2888%29.png)

A block element will take up an entire line of space—unless you intervene with CSS properties

#### Block vs. Inline

By using float CSS properties, we can command our website to display multiple HTML elements adjacently. 

![](../../../.gitbook/assets/image%20%289%29.png)

Float ****"forces" elements to the side you specify.

The `float` property can have one of the following values:

* left - The element floats to the left of its container
* right - The element floats to the right of its container
* none - The element does not float \(will be displayed just where it occurs in the text\). **This is default**
* inherit - The element inherits the float value of its parent

In its simplest use, the `float` property can be used to wrap text around images.

#### Clearfix

Floated elements are taken out of the normal flow of the document. This can lead to some unexpected side effects.

![](../../../.gitbook/assets/image%20%2852%29.png)

If an element is taller than the element containing it, and it is floated, it will overflow outside of its container.

Then we can add `overflow: auto;` to the containing element to fix this problem

The `overflow:auto` clearfix works well as long as you are able to keep control of your margins and padding \(else you might see scrollbars\). 

