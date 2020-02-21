# Objects II

An object's properties can be any type of value we can store in a regular variable. This includes numbers, strings, booleans, even other objects!

Object properties can also contain functions. We refer to functions that exist on an object as **methods**.

Check out the following code: 

```javascript
// In addition to static properties, an object can also contain functions we refer to as methods
const carObject = {
  make: 'Jeep',
  model: 'Wrangler',
  mileage: 110000,
  hasFuel: true,
  drive: function(miles) {
    // Inside of an object's method, "this" literally means "this object"
    if (this.hasFuel === true) {
      this.mileage += miles;
      this.hasFuel = false;
      console.log(`${this.make} ${this.model} has driven ${miles} miles! Total mileage is now ${this.mileage}!`);
    } else {
      console.log(`${this.make} ${this.model} has no fuel! Fill up the tank before driving!`);
    }
  },
  fillUpTank: function() {
    this.hasFuel = true;
    console.log(`Filling up on gas... ${this.make} ${this.model} now has a full tank!`);
  }
};
carObject.drive(500);
carObject.drive(500);
carObject.fillUpTank();
```

You may have noticed that a few of the properties on this object are methods. The syntax for accessing an object's methods are the same as accessing any other property. `<object-name>.<object-property>`.

Inside of an object's method, we'll often want to refer to other properties on the object. For example, according to our code, whenever the car's `drive` method is called, the car's `mileage` and `hasFuel` properties should update.

When we call the the `drive` method \(`carObject.drive()`\), `this` refers to the `carObject` object. So `this.mileage`is like writing `carObject.mileage`. It may not be immediately apparent why we would write it this way, but it will become apparent as you learn more about JavaScript.

