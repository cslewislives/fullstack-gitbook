# Rendering Arrays

A lot of what we'll be doing when it comes to front-end development is taking data, altering it in some way with logic, and displaying it graphically for the user.

A lot of data that we are rendering comes from a server, and a lot of server data comes to us as lists and arrays. One of the most basic tasks is taking an array of items and rendering it to the page.

We have already seen how to do this in the previous lesson, with code that looked like this:

```javascript
const nameList = ["George", "Sue", "Tim", "Lin"]
let output = ""
for (let i = 0; i < nameList.length; i++){
	output += `<p>${nameList[i]}</p>`
}
document.getElementById("root").innerHTML = `<div>${output}</div>`
```

Using for loops and concatenating strings we are able to render names to the page.

### Map

There is a simpler way to render arrays to the page called map. Map essentially is a one word method that acts like a for loop specifically for arrays. Let's take a look:

```javascript
const nameList = ["George", "Sue", "Tim", "Lin"]

document.getElementById("root").innerHTML = nameList.map(e => `<p>${e}</p>`).join('')
```

Using the above we are able to achieve the same goal but in two lines rather than six. **Map** is a specific method on arrays in JavaScript and it will iterate through the array applying the function inside the parenthesis to each element of the array.

In the above example it is going through the `nameList` array and changing each element into a `<p>` tag. We then use `join` which is another array method and we join all items of the array into one string.

The `nameList` array will then essential look like this:

```javascript
const nameList = ["George", "Sue", "Tim", "Lin"] //before

const nameList = "<p>George</p><p>Sue</p><p>Tim</p><p>Lin</p>" //after
```

### Filter

The `.filter()` method works largely the same way and the difference being that it only targets specific items.

```javascript
const nameList = ["George", "Sue", "Tim", "Lin"]

console.log(nameList.filter(e => e.includes("i")))
```

In this example `filter` also goes through each item of the array but it is looking for elements that include the letter `i`. When it finds those elements `filter` creates a new array and puts those elements in the new array.

