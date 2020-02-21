---
description: A Scalable Front-End Architecture
---

# Components

We've learned how to dynamically render data from the server to the page on a small scale but real applications are doing this on a much larger scale.

Think about Facebook and you're on your feed: 

* New posts are being rendered. 
* New comments are coming in on each post. 
* The like count is rising and falling. 
* Ads are changing every couple of minutes. 
* Your notification count rises. 
* A new message comes from a friend and the chat widget opens.

That's a lot of dynamic data! How would you plan to build that out?

### Component-based Architecture

Component-based architecture is a common way to break building data heavy web apps down into manageable pieces of code.

**Components** are small elements which can be used together to create large applications. Think of them like building blocks.

React, Angular, and Vue all employ this pattern. These are all popular frameworks that make CBA easier but you can also achieve this using vanilla JavaScript

#### JavaScript Components

Using the same HTML file we have been using to dynamically render elements we can then write the following JS code:

```javascript
class MovieComponent {
	template = `<p> Sample Movie </p>`
}

document.getElementById("root").innerHTML = new MovieComponent().template
```

Pretty straight-forward. Can you see how this can be compounded to make things easier?

Let's take a look at it in action:

```javascript
class MovieComponent {
    template = `<p> Sample Movie </p>`
}
    
class MovieListComponent {
template = `
	<div>
		${new MovieComponent().template}
		${new MovieComponent().template}
		${new MovieComponent().template}
	</div>`
}

document.getElementById("root").innerHTML = `${new MovieListComponent().template}`
```

By creating our smaller components we are able to combine them together in a way that allows us to only write one line of code to render all three movies.

But how do we render them dynamically? By using a constructor!

```javascript
class MovieComponent {
    constructor (title){
        this.title = title
        this.template = `<p> ${title} </p>`
    }
}
    
class MovieListComponent {
    template = `
        <div>
            ${new MovieComponent("Jurassic Park").template}
            ${new MovieComponent("Toy Story").template}
            ${new MovieComponent("Dumbo").template}
        </div>`
}

document.getElementById("root").innerHTML = `${new MovieListComponent().template}`
```

#### Bootstrap

Can you also add Bootstrap to your components? You bet!

```javascript
class MovieComponent {
    constructor (title){
        this.title = title
        this.template = `
            <div class="card">
                <div class="card-body">
                    ${this.title}
                </div>
            </div>
        `
    }
}

document.getElementById("root").innerHTML = `${new MovieComponent("Curious George").template}`
```

