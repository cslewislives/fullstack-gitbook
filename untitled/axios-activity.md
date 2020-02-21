# Axios - Activity

![Axios](../.gitbook/assets/image%20%28103%29.png)

As always attempt the activity yourself before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
* Operating under the assumption that you are using the books databse from before write the JavaScript code that would render the first and last name of each author to the page.
* This code will not be functional as we do not have a database or backend to connect to, however this is great practice for when you will.
{% endtab %}

{% tab title="JS Solution" %}
```javascript
axios.get('/authors')
	.then(function (response) {
		// handle success
		const data = response.data;
		
		document.getElementById("root").innerHTML = data.map(author => `<p>${author.firstName} ${author.lastName}`).join('');
	})
	.catch(function (error) {
		// handle error
		console.log(error)
	})
	.finally(function () {
		// always executed
	});
```
{% endtab %}
{% endtabs %}

