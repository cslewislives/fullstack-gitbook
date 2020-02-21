# Components - Activity

![Components](../.gitbook/assets/image%20%2879%29.png)

As always attempt the activity yourself before checking out the solution.

Head to [this JSBin link](https://jsbin.com/quhadom/1/edit?html,js,output) and follow the instructions below, remember to incorporate everything you've learned up till this point:

{% tabs %}
{% tab title="Instructions" %}
1. Using bootstrap, create a Person component and use it to render 4 people you know.
{% endtab %}

{% tab title="JS Solution" %}
As with all code there are many ways to achieve the same result. If your code works and performs as instructed, great job! Here is an example of one way you could achieve the desired result:

```javascript
class PersonComponent {

  constructor (name) {
    this.name = name;
    this.template = `
    <div class="card">
      <div class="card-body">
        ${this.name}
      </div>
    </div>
    `
  }
}

class PersonListComponent {
  template = `
    <div>
      ${new PersonComponent("Harry").template}
      ${new PersonComponent("Ron").template}
      ${new PersonComponent("Hermione").template}
    </div>
  `
}
 
document.getElementById('root').innerHTML = `${new PersonListComponent().template}`;
```
{% endtab %}
{% endtabs %}

 

