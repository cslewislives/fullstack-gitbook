# Forms - Activity

![Forms](../.gitbook/assets/image%20%2892%29.png)

As always attempt the activity yourself before checking out the solution.

Head to [this JSBin link](https://jsbin.com/lotazuq/edit?html,js,output) and follow the instructions below, remember to incorporate everything you've learned up till this point: 

{% tabs %}
{% tab title="Instructions" %}
1. Dynamically add both a username and password to the page and a “login” button.
2. When the login button is clicked, if the username is admin and the password has more than 8 characters, display “Welcome” on the page.
3. Otherwise display “Invalid Credentials”
{% endtab %}

{% tab title="JS Solution" %}
As with all code there are many ways to achieve the same result. If your code works and performs as instructed, great job! Here is an example of one way you could achieve the desired result:

```javascript
document.getElementById("root").innerHTML = `
    <input id="username" />
    <input id="password" type="password" />
    <button id="login">login</button>
    <p id="res"></p>
`
document.addEventListener("click",function(e){ 
    if(e.target && e.target.id== "login"){ 
       console.log(document.getElementById("username").value)
       if(document.getElementById("username").value == "admin" && document.getElementById("password").value.length >= 8) {
           document.getElementById("res").innerText = "Welcome";
        } else {
            document.getElementById("res").innerText = "Invalid Credentials";
        }
    } 
});
```
{% endtab %}
{% endtabs %}



