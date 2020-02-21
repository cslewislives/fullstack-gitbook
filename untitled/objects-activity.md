# Objects - Activity

![Objects](../.gitbook/assets/image%20%2892%29.png)

Make sure you attempt the following activity before checking out the solution code.

{% tabs %}
{% tab title="Instructions" %}
Using either [JSFiddle.net](www.jsfiddle.net) or [JSBin.com](www.JSBin.com) complete the following:

* In 2 ways, create the equivalent of a Java motorcycle class with the properties VIN, make, model, year, maxSpeed, currentSpeed.
* Include methods accelerate and brake which increment and decrement the currentSpeed by 5 with limits of 0 and maxSpeed.
{% endtab %}

{% tab title="Java Class" %}
```java
class Motorcycle {
	
	constructor (VIN, make, model, year, maxSpeed, currentSpeed){
		this.VIN = VIN;
		this.make = make;
        this.model = model;
        this.year = year;
        this.maxSpeed = maxSpeed;
        this.currentSpeed = currentSpeed;
	}
	
	accelerate(){
        this.currentSpeed = this.currentSpeed + 5;
	}

    brake() {
        this.currentSpeed = 0;
    }
}
```
{% endtab %}

{% tab title="JS Solution" %}
```javascript
function Motorcycle(VIN, make, model, year, maxSpeed, currentSpeed) {
    this.VIN = VIN;
    this.make = make;
    this.model = model;
    this.year = year;
    this.maxSpeed = maxSpeed;
    this.currentSpeed = currentSpeed;
    this.accelerate = function() {
        this.currentSpeed = this.currentSpeed + 5;
    };
    this.brake = function() {
        this.currentSpeed = 0;
    };
}
```
{% endtab %}
{% endtabs %}

