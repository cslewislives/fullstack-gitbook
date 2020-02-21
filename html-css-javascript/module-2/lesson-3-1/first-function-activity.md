# First Function - Activity

![First Function](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

* Start by creating a new function called `multiplyFunc`.
* `multiplyFunc` should take in one parameter.
* Within the code block, you should simply console log out the parameter.
* Finally, call your function passing in any argument you wish.

**Challenge:**

Re-write the `multiplyFunc` so that it will console log the taken parameter multiplied by `3`.
{% endtab %}

{% tab title="Solution" %}
```javascript
const multiplyFunc = function (num1) {
	console.log(num1);
}

multiplyFunc(3); // Logs 3

multiplyFunc(4); // Logs 4


// Challenge

const multiplyFunc = function (num1) {
	console.log(num1 * 3);
}

multiplyFunc(3); // Logs 9

multiplyFunc(4); // Logs 12

```
{% endtab %}
{% endtabs %}

