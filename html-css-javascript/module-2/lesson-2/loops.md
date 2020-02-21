# Loops

Loops are a great way to keep you from having to write repetitive code because loops handle the repetition. Basically, loops offer a quick and easy way to do something repeatedly. 

We'll look at two different loops, or iterators, called `for` loops and `while` loops.

### While Loops

Take a look at the following `while` loop: 

```javascript
let counter = 0;

while (counter < 5){
  console.log(counter);  
  counter++;
}
```

* First, we set a variable, `counter`, equal to `0`. 
* Next, using the keyword, `while`, we pass in `counter` and give it a condition. 
  * In this case, we are saying that **while** `counter` is less than `5`, run this block of code. 
* Within this block of code, we start with our `console.log()` which only serves to print out `counter` so we can see the incrementation as it happens.
* Next we increment `counter` by 1 every time the block of code runs. 
  * `counter++` is shorthand for `counter = counter + 1`. 
  * This will be our control for how many times the block of code runs because when this counter eventually hits 5, it will stop running. 

### For Loops

Take a look at the following `for` loop:

```javascript
for (let i = 0; i < 5; i++){
  console.log(i);
}
```

* `let i = 0;` is our initial expression. 
  * We create a variable called `i` and store the number `0`. 
* The second expression is our condition. 
  * While `i` is less than `5`, we'll loop through our block of code. 
* Finally, we have `i++`which is simply our increment expression. 
* Within our block of code, we have our `console.log(i);` 
  * That will continuously run while our condition is true.

### Parallels

For Loops and While loops are fairly similar, with a for loop being shorter and easier to write and we are less likely to forget to add the incrementer. We tend to favor for loops.

The difference is that:

For loops are often used when the number of iterations is numerable \(When the number of iterations might be known or set\).

```javascript
for( int i = 0; i > 10; i++)
{
    //Some code here
}
```

Whereas while loops are often used when the number of iterations are indefinite.

```javascript
while(!done) //while something is NOT done run the following code
{
    //Some code goes here
}
```

