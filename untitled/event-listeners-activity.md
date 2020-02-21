# Event Listeners - Activity

![Event Listeners](../.gitbook/assets/image%20%2892%29.png)

As always attempt the activity yourself before checking out the solution.

Head to [this JSBin link](https://jsbin.com/gipakab/2/edit?html,js,output) and follow the instructions below, remember to incorporate everything you've learned up till this point:

{% tabs %}
{% tab title="Instructions" %}
1. Add 2 buttons to the page dynamically - each with a name of your favorite celebrity, or a friend of yours. 
2. When the proper button is clicked, display a short bio about that person. 
3. Take your time and try to do this with only one event listener and then with two - which seems better?
{% endtab %}

{% tab title="JS Solution" %}
As with all code there are many ways to achieve the same result. If your code works and performs as instructed, great job! Here is an example of one way you could achieve the desired result:

```javascript
const name1 = "Katie";
const name2 = "Gabe";

const bio1 = "Katie is a dancer. She does not like long walks or other physical activities that isn't dancing";
const bio2 = "Gabe is an aspiring architect. He enjoys long walks on the beach and playing guitars."

htmlString = "";

htmlString += `<button class="btn btn-primary btn-lg" id="partner1">${name1}</button>`

htmlString += `<button class="btn btn-primary btn-lg" id="partner2">${name2}</button>`

htmlString += `<p id="bio"></p>`


document.getElementById("root").innerHTML = htmlString;

document.addEventListener("click",function(e){
    if(e.target && e.target.id == "partner1"){ 
        document.getElementById("bio").innerText = bio1
    } else if(e.target && e.target.id == "partner2") {
        document.getElementById("bio").innerText = bio2
    }
});
```
{% endtab %}
{% endtabs %}



