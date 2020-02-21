# Objects II - Activity

![Objects](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

Add code for makeSound, sleep, and feed methods on the dog object.

1. Open the following in your code editor.
2. When makeSound is called, the object's sound property should be logged to the console using the this keyword.
3. When sleep is called, the object's isSleepy property should be set to false, and its isHungry property should be set to true. Use the this keyword to access both properties. Add a console log statement to explain to the user what's happening.
4. When feed is called, the object's isHungry property should be set to false, and its isSleepy property should be set to true. Use the this keyword to access both properties. Add a console log statement to explain to the user what's happening.
5. At each step remember to test your code in the console!

```javascript
const dog = {
  isSleepy: false,
  isHungry: true,
  sound: "Woof!",
  name: "Spot"
};
dog.makeSound();
dog.feed();
dog.sleep();

// Add code to implement the following methods:
// 1. dog.makeSound() should print the sound property to the console

// 2. dog.sleep() should set isSleepy to false
// And isHungry to true
// Throw in a console log to let the user know the dog is took a nap and is now hungry

// 3. dog.feed() should set isHungry to false
// And isSleepy to true
// Throw in a console log to let the user know the dog just ate and is now sleepy
```
{% endtab %}

{% tab title="Solution" %}
```javascript
const dog = {
  isSleepy: false,
  isHungry: true,
  sound: 'Woof!',
  name: 'Spot',
  makeSound: function() {
    console.log(this.sound);
  },
  sleep: function() {
    console.log(`${this.name} is going to sleep...`);
    this.isSleepy = false;
    this.isHungry = true;
    console.log(`${this.name} woke up hungry!`);
  },
  feed: function() { 
    console.log(`Feeding ${this.name}...`);
    this.isHungry = false;
    this.isSleepy = true;
    console.log(`${this.name} is sleepy!`);
  }
};
dog.makeSound();
dog.feed();
dog.sleep();
```
{% endtab %}
{% endtabs %}

 

