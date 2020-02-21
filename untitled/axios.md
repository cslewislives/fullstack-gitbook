# Axios

### HTTP Requests

HTTP is the protocol that we use to send requests to the server.

The most **popular** types of requests are:

* GET
* POST
* PUT
* DELETE

**Axios** is one of many possible packages that can be used to make these requests.

In order to access the tools given to us by the Axios package we need to connect to it in our HTML just like Bootstrap or our own JavaScript files.

You can add the following to your HTML:

```markup
<script src="https://unpkg.com/axios/dist/axios.min.js"></script>
```

Now you can reference the tools you need and JS knows what you are talking about.

Let's say you had a database of books in a bookstore and you wanted to get information about the authors in the database. We would use the following code in our JS to retrieve that information:

```javascript
axios.get('/authors')
	.then(function (response) {
		// handle success
		console.log(response)
	})
	.catch(function (error) {
		// handle error
		console.log(error)
	})
	.finally(function () {
		// always executed
	})
```

Using `axios` JS knows to connect to the database using the route `/authors`. We built the `/authors` route on the backend in our Java so we know what we are getting when we use that route. We then `console.log` the response so that we can view our information.

The response will have a status code, data and a lot of other information. So if we wanted to drill down to very specific information we can use **dot notation** to get to the information we really want.

```javascript
axios.get('/authors')
	.then(function (response) {
		// handle success
		const data = response.data;
		console.log(data[0].books[0].publishYear);
	})
```

As you can see we are able to get to very specific pieces of data this way. In this example we are printing the `publishYear` of the first book of the first author we received using our HTTP request.

### More Examples

Read through the following code and see if you understand what is going on, then watch the following video to see it in action:

```javascript
axios.get('/authors')
	.then(function (response) {
		// handle success
		console.log(response)
		const data = response.data;
		
		document.getElementById("root").innerHTML += `<p>${data[1].books[1].publishYear}</p>`
		document.getElementById("root").innerHTML += `<p>${data[2].books[0].title}</p>`
		document.getElementById("root").innerHTML += `<p>${data[3].lastName}</p>`
	})
	.catch(function (error) {
		// handle error
		console.log(error)
	})
	.finally(function () {
		// always executed
	})
```



