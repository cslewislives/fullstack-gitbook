---
description: Adding Interactivity
---

# Forms - Event Listeners

Forms are interactive components of web applications. They utilize various components like the following to get user input:

* Buttons
* Text input fields
* Check boxes

How do you send an email, post on Facebook, or add a task to an online to do list? A form. 

## Event Listeners

In order for our forms to perform actions when we want them to, we will need to add **event listeners**. 

Event listeners wait for an event to occur and respond with an action.

There are many different events that you could use but some common examples are:

* a button click
* hovering over a certain area
* focusing on an input area

{% hint style="info" %}
Check out the complete [list of event listeners here!](http://developer.mozilla.org/en-US/docs/web/Events)
{% endhint %}

### Mouse Click

Let's take a look at the code we would use to add an event listener to a mouse click

```javascript
document.addEventListener('click',function(e){
    const first = "dog"
    const second = "cat"
    document.getElementById("root").innerHTML = `
        <ol>
            <li>${first}</li>
            <li>${cat}</li>
        </ol>` 
})
```

**Notice** that at line one we are using the `document.addEventListener` method to create our event listener. The specific event we are listening for is `"click"`, a.k.a. mouse click, then we are creating a `function` that will run when the click happens.

The function contents should look familiar, therefore, what do you suppose happens when you mouse click on that page?

#### Specific Element

Now what if you want to confine the event to a specific area on your page, such as a button click?

We can do this using the below code:

```javascript
document.getElementById("root").innerHTML = `<button id="btn">click</button>`
    
document.addEventListener("click",function(e){ 
    if(e.target && e.target.id == "btn"){ 
        const first = "dog"
        const second = "cat"
        document.getElementById("root").innerHTML = `
            <ol>
                <li>${first}</li>
                <li>${cat}</li>
            </ol>`
    }
})
```

Looking at the first line of the above code, we have created a button with and id of `btn`. This button will appear as soon as we load the page.

We then created an event listener on a mouse click and inside our function we used built in JavaScript event properties to look for a specific target. 

```javascript
if(e.target && e.target.id == "btn")
```

This block of code is what confines our event listener to the button. It will not fire unless there is a valid target for the event **as well as** a target with the id of `btn`. Only then will it trigger the rest of the code.

{% hint style="info" %}
The `e` that we use inside our function and as our function parameter is the **event** itself. We could call that parameter whatever we want, we use `e` to simplify but also to remind us what we are referencing.
{% endhint %}

