# Rendering Arrays - Activity

![Rendering Arrays](../.gitbook/assets/image%20%2892%29.png)

As always attempt the activity yourself before checking out the solution.

Head to [this JSBin link](https://jsbin.com/vivufom/2/edit?html,js,output) and follow the instructions below, remember to incorporate everything you've learned up till this point:

{% tabs %}
{% tab title="Instructions" %}
1. Create an array of names
2. Combine your knowledge of filter and map to render each student whose name is more than 5 characters.
{% endtab %}

{% tab title="JS Solution" %}
As with all code there are many ways to achieve the same result. If your code works and performs as instructed, great job! Here is an example of one way you could achieve the desired result:

```javascript
const classmates = ["George", "Sherri", "Cj", "Daniel", "Tim"];

document.getElementById("root").innerHTML = 
	classmates.filter(mate => mate.length > 5).map(name => `<p>${name}</p>`).join('');
```
{% endtab %}
{% endtabs %}

 

