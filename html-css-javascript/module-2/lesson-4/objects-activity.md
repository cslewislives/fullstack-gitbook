# Objects - Activity

![Objects](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

In this activity , you'll use objects to make an interactive phone book:

1. In the code provided, add more contacts to the `contacts` object.
2. `console.log` one person's phone number.
3. Next add a `prompt` that prompts the user for a name and store the response in a variable called `prop`
4. Use an `alert` to display the phone number associated with the name the user entered.

**Hint:** You may need to use bracket notation for this exercise.

```javascript
const contacts = {
    dan: "555-330-2289",
    dante: "555-660-2295"
  }
```

**Challenge:**

For each person in the `contacts` object, create a new object that will hold their phone number, address, and state of residency. Then `console.log` one person's address.
{% endtab %}

{% tab title="Solution" %}
```javascript
const contacts = {
    dan: '555-330-2289',
    dante: '555-660-2295',
    jenny: '555-867-5309',
    keisha: '660-228-4765',
    jacob: '992-443-0087',
    don: '667-333-4427'
    };

    console.log(contacts.jacob);

    const prop = prompt(`Whose number do you need?`);

    alert(contacts[prop]);

// Challenge
// const contacts = {
//     dan: {
//         number: '555-330-2289',
//         address: '123 Pelegrino St.',
//         state: 'CA'
//     },
//     george: {
//         number: '555-123-3321',
//         address: '550 Cappuccino Ave.',
//         state: 'GA'
//     }
// };

// console.log(contacts.george.address);
```
{% endtab %}
{% endtabs %}

 

