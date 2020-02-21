# Lists and Loops

### What, Why, and When

Loops are a programming tool used to iterate through a list of data. In JavaScript, we call lists of data **arrays**.

Lists \(aka arrays\) are the data structure that developers deal with most frequently, so learning to master them is a vital part of being a successful developer. Loops are the tool we use _every single time_ we need to access every element in an array.

Imagine you are building an online phone book. You'll need to store all those names and phone numbers in an array. Want to look up a friend? You'll need to loop through the array checking each entry until you find your friend. Want to print the whole list? You'll need to loop through the array rendering each one individually.

### Flowcharting Lists

Booleans, Strings, and numbers are what we call primitive types.

JavaScript can also store more complex types. Arrays are what we call lists of things in JavaScript. `1,2,3,4,5`is a list of numbers so we would store that as an array. Perhaps we want to store a list of all the students in the class so we can take role. We can make an array of strings like `'Jan', 'Maryam', 'Tisha', 'Winson'`.

![Array](../../../.gitbook/assets/array.png)

The above image represents an array of strings.

**Remember** coding is about storing and manipulating data in an organized way. Every element in an array has an index. The first element has an index of _zero_; the second, an index of 1; And so on. 

![Index](../../../.gitbook/assets/index.png)

To manipulate data in an array, we must access an individual element first. For that we use _brackets_ with the index of the element inside.

Looking at the flowchart below what do you think the array will hold at the end?

![](../../../.gitbook/assets/arr-accessor.png)

The array will hold `'Jim', 'Maryam', 'Tisha', 'Winson'`. Jan was changed to Jim.

{% hint style="info" %}
**Remember** that the first element of an array has an index of _**zero;**_ the second, an index of 1; And so on.
{% endhint %}

### Flowcharting Loops

Loops are a way of performing a set of operations over and over again a set number of times. We could use a loop to display 'hey!' 14 times or to add 1 to a number 12 times in a row.

Though loops can do anything over and over, they are primarily used for iterating through arrays.

Any time we want to access every element in an array we need to use a loop. 

* How do we display _each_ individual element in an array? We use a loop. 
* How do we double _each_ element in an array of numbers? We use a loop. 
* How can we check _every_ element in an array of numbers to see if it's greater than 100? We use a loop. 
* If you are dealing with an array in any capacity, odds are you will use a loop at some point.

The following is how a loop is represented in a flowchart:

![Basic Loop](../../../.gitbook/assets/piggywoo.png)

What do you think the above program does? 

If you said that it displays 'piggywoo' 4 times you are correct!

In computing we always start from zero not one. The loop runs from zero to four inclusive of zero but exclusive of four. Meaning 0,1,2,3. 4 times, starting at 0.

Suppose we are tasked with printing each student in a list of students in our class. Let's build a flowchart to map out how we would build this program.

![Iterate](../../../.gitbook/assets/iterate.png)

We start with an array \(that's a list\) of 4 students. We then loop from zero to `studentList.length`. The length of the `studentList` is 4, so that's like saying loop from 0 to 4, just like our last example!

Inside the loop we are using the notation `studentList[i]`. The `i` is a variable that indicates that on each iteration of the loop we will access the next element in the array. So the first time through we will access the first element in the array, `'Jan'`, and then display it. The second time through, we will access the second element, `'Maryam'`, and then display it, and so on.

Take some time on this one. This section is about learning logic NOT syntax. There's a little syntax thrown in to ease the transition to actually coding, but try to focus on the logic for now.

