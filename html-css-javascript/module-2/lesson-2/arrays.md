# Arrays

### What, Why, and When

An **array**, denoted by brackets `[]`, is an indexed collection of data elements preferably of the same type and stored in a single variable. 

Anytime you have multiple elements you want to store, like a series of stock symbols you are watching, you can store them in an array. 

Additionally, there are some cool methods you can use specifically on arrays. So instead of creating a new variable for each stock symbol, you could simply hold all values in an array.

Let's say you needed to store the address of every Starbucks in California for use later with a geocoder. You would simply add to an array called `starbucksAddressList` and add the addresses in there.

### Creating an Array

For the following examples let's use a tool like [jsbin.com](www.jsbin.com) to see them in action. You could also use the DevTools console or your editor.

Let's talk about how to first create an empty array. Note the use of brackets to denote that we are storing an array inside of a variable.

```javascript
const randomList = [];
```

Within the newly created `randomList`, we can add a few elements.

```javascript
const randomList = ['George', 12, false];
```

An array _can_ hold elements of any type, you are free to mix-and-match any data type just as long as each element inside of the array is comma separated.

**However,** while the above is possible, you should almost never do it. Arrays should generally hold elements all of one type. JavaScript doesn't enforce this rule, but it's a best practice. Therefore, we should create the following:

```javascript
const nameList = ['George', 'Lisa', 'Glenna'];
```

### Array Method

Arrays have methods that you can use on them. One such method is the `push` method. Using the `push`method, you are able to add items to the _end_ of the array.

```javascript
nameList.push('Timothy');

console.log(nameList);
```

After running the above code, you should see the updated `nameList`. 

{% hint style="info" %}
`console.log` is a built-in JavaScript method that we can use to print out things in the console.
{% endhint %}

### Accessing an Element

How do we refer to an item in the array?

You are able to refer to an element within an array by using **bracket notation**.

```javascript
nameList[0];
```

The above code will evaluate to the first element in the array. **Remember** that 0 is the index of the first element and that indexing always starts from 0. So if you had an array with 3 items, you would start counting from 0 and eventually get to 2.

```javascript
const nameList = ['George', 'Lisa', 'Glenna'];

nameList[0]; //Evaluates to "George" or the first element in the array.
nameList[1]; //Evaluates to "Lisa" or the second element in the array.
nameList[2]; //Evaluates to "Glenna" or the third element in the array.
```

Using code how would we find the **length** of an array?

```javascript
nameList.length;
```

