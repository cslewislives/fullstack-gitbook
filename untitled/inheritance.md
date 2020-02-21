# Inheritance

JavaScript lacks abstract classes and interfaces, but it does have a mechanism for inheritance called **Prototypal Inheritance**. 

Although internally JavaScript inheritance differs from Java inheritance a bit, on the surface the two are very similar. 

{% tabs %}
{% tab title="Java" %}
```java
class Person extends Animal{
	private String name;
	private int age; 

	public Person(String name, int age){
	  this.name = name;
	  this.age = age;
	}

	public void greet(String hi){
	  System.out.println(hi + this.name);
	}
}
```
{% endtab %}

{% tab title="JavaScript" %}
```javascript
//This is syntax is new to JavaScript as of ES6
class Person extends Animal{
	
	constructor (name, age){
		this.name = name
		this.age = age
	}
	
	greet(hi){
	  console.log(hi + this.name)
	}
}
```
{% endtab %}
{% endtabs %}

This concept can get really tricky so we won't go to far here, but be aware that this concept exists. Feel free to do your own research on this.

{% hint style="info" %}
 Note we must use **`super()`** which calls the constructor of the parent class.
{% endhint %}

### Inheritance Code Walkthrough

Walkthrough the code below and see if you can figure out which property belongs to which object.

```javascript
class Animal {
  constructor (numOfFeet, sound, color){
    this.numOfFeet = numOfFeet;
    this.sound = sound;
    this.color = color;
  }
  
  makeNoise(){
    console.log(this.sound);
  }
  
}
  
class Dog extends Animal{
  constructor (color, name){
    super(4, 'woof', color);
    this.name = name;
  }
  
  sayName (){
    console.log(this.name);
  }
}
  
const rover = new Dog('black', 'Rover McSweeten III');
  
rover.rollOver = function (){
  console.log('rolling over');
}
```

