# Loops II - Activity

![Loops](../../../.gitbook/assets/image%20%2837%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions**

Create a flowchart to represent the following program, then code it out.

1. Using a loop, prompt the user to enter five names.
2. Push each name to a `nameList` array.
3. Using another loop, render/alert the five student names.

**Challenge:**

Don't forget to flowchart FIRST!

1. Prompt the user for a number of students in the class.
2. Prompt the user to input that many names.
3. Render all of the names.

**Ultra Challenge:**

Working off of the bonus, print only the people whose names include the letter `a`.
{% endtab %}

{% tab title="Solution" %}
```javascript
const nameList = [];

for (let i = 0; i < 5; i++){
  const name = prompt('Enter a name');
  nameList.push(name);
}

for (let i = 0; i < nameList.length; i++){
  const name = nameList[i];
  alert(name);
}

// Challenge

const challengeList = [];
const challengeQuestion = parseInt(prompt('How many people are in the class?'));

for (let i = 0; i < challengeQuestion; i++) {
    const newName = prompt(`Enter person number ${i+1}'s name:`);
    challengeList.push(newName);
}

for (let i = 0; i < challengeList.length; i++) {
    console.log(challengeList[i]);
}

// ULTRA CHALLENGE

for (let i = 0; i < challengeList.length; i++) {
    if (challengeList[i].includes('a')) {
        console.log(challengeList[i]);
    }
}
```
{% endtab %}
{% endtabs %}



