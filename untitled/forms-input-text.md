# Forms - Input Text

Now that we know about event listeners, let's walk through how to capture user input in a text field!

```javascript
document.getElementById("root").innerHTML = `
	<button id="btn">click</button>
	<input id="searchTxt" />
`
document.addEventListener("click",function(e){ 
	if(e.target && e.target.id == "btn"){ 
		console.log(document.getElementById("searchTxt").value)
	} 
})
```

We start by creating an input field using the `input` HTML tag and give it an id of `searchTxt`. **Notice** that `input` is a self-closing tag.

Next, we create our event listener like before. We then use `console.log` to print out the value of what the user types into our new input field. And we do this using `getElementById("searchTxt").value`. The `value` method allows us to grab whatever was typed into the `input` field with the id of `searchTxt`. 

