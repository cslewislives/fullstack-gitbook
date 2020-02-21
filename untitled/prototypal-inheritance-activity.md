# Prototypal Inheritance - Activity

![Prototypal Inheritance](../.gitbook/assets/image%20%28102%29.png)

Make sure you attempt the following activity before checking out the solution code 

{% tabs %}
{% tab title="Instructions" %}
Using either [JSFiddle.net](www.jsfiddle.net) or [JSBin.com](www.JSBin.com) complete the following:

Think of an object that could be created from a class that extends another class.

Write the code to create those classes and instantiate an object from them. A good tip to keep in mind as you are working on this activity is how objects can be related to each other and in what ways certain objects are different.

**Hint:** Think about vehicles! Within the category of vehicles, you might have cars, trains, and airplanes. Within cars, you can make coupes, sedans, or SUVs. Within sedans, you could have a Ford Taurus, Honda Accord, or a Toyota Camry.
{% endtab %}

{% tab title="Possible Solution" %}
```javascript
// General Vehicle class
class Vehicle {
    constructor (speed, acceleration) {
      this.speed = speed;
      this.acceleration = acceleration;
    }
  }
  
  // Car class, which extends Vehicle class to add wheel count and color, as well as honk method
  class Car extends Vehicle {
    constructor(speed, acceleration, color) {
      super(speed, acceleration);
      this.color = color;
      this.numWheels = 4;
    }
  
    honk () {
      console.log('BEEP BEEP');
    }
  }
  
  // Coupe class which extends Car and has 2 doors
  class Coupe extends Car {
    constructor(speed, acceleration, color) {
      super(speed, acceleration, color);
      this.numDoors = 2;
    }
  }
  
  // Sedan class which extends car and has 4 doors
  class Sedan extends Car {
    constructor(speed, acceleration, color) {
      super(speed, acceleration, color);
      this.numDoors = 4;
    }
  }
  
  // Airplace class which extends Vehicle, and has a maxAltitude as well flying attribute and method
  class Airplane extends Vehicle {
    constructor(speed, acceleration, maxAltitude) {
      super(speed, acceleration);
      this.maxAltitude = maxAltitude;
      this.flying = false;
    }
  
    takeOff () {
      this.flying = true;
    }
  }
  
  
  const camry = new Sedan(120, 10, 'blue');
  camry.honk();
  console.log(camry);
  
  const boeing = new Airplane(850, 125, 60000);
  boeing.takeOff();
  console.log(boeing);
```
{% endtab %}
{% endtabs %}

