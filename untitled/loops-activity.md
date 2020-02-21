# Loops - Activity

![Loops](../.gitbook/assets/image%20%2892%29.png)

Make sure you attempt the following activity before checking the solution code. 

{% tabs %}
{% tab title="Instructions" %}
Using either [JSFiddle.net](https://jsfiddle.net/) or [JSBin.com](www.JSBin.com) complete the following:

1. Create an array of your 5 best friend’s names.
2. Loop through the array and print all the names.
3. Create an array of your 5 favorite numbers.
4. Loop through the array and increment each by one then print the array.
{% endtab %}

{% tab title="Solution" %}
```javascript
const bestFriendsList = ['Natatlie', 'Delphine', 'George', 'Tim', 'Kyle']

for (let i = 0; i < 5; i++) {
    console.log(bestFriendsList[i]);
}

const favNumList = [5, 7, 10, 18, 21]

for (let j = 0; j < 5; j++) {
   favNumList[j]++;
}

console.log(favNumList);
```
{% endtab %}
{% endtabs %}

