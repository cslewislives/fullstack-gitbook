# Arrays - Activity

![Arrays](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
**Instructions**

1. Create an empty student array.
2. Prompt the user to input five separate names.
3. Push each name onto the array.
4. Alert the second name in the array.

**Challenge:**

Don't forget to flowchart FIRST!

Adding onto the code above:

1. Prompt the user for an index.
2. Alert the student name at the index provided.

**Ultra Challenge:**

Don't forget to flowchart FIRST!

Google to find a way to implement the following:

1. Create an array with five students.
2. Take in a student name as input from the user.
3. Alert `true` if that student is in the array.
4. Alert `false` if that student is not in the array.
{% endtab %}

{% tab title="Solution" %}
We will capture the 5 user inputs into 5 different variables.

```javascript
const name1 = prompt('enter a student name');
const name2 = prompt('enter a student name');
const name3 = prompt('enter a student name');
const name4 = prompt('enter a student name');
const name5 = prompt('enter a student name');
```

Next, we initialize an empty array for use later as well as use the `.push()` method to add our user input variables into that array.

```javascript
const studentList = [];

studentList.push(name1);
studentList.push(name2);
studentList.push(name3);
studentList.push(name4);
studentList.push(name5);
```

Finally, we'll store the second element in the array into a new variable and alert that variable to the user. When referring to elements in an array, we use indices and that indices start at `0`. Therefore, the second element in the array is at the `1` index.

```javascript
const student = studentList[1];

alert(student);
```

The full solution should look like this:

```markup
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Arrays, Prompts, and Alerts</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
    <script>
        const name1 = prompt('enter a student name');
        const name2 = prompt('enter a student name');
        const name3 = prompt('enter a student name');
        const name4 = prompt('enter a student name');
        const name5 = prompt('enter a student name');
        
        const studentList = [];
        
        studentList.push(name1);
        studentList.push(name2);
        studentList.push(name3);
        studentList.push(name4);
        studentList.push(name5);
        
        const student = studentList[1];
        
        alert(student);

            // Challenge -- Uncomment this section to showcase the Challenge!

        // const newIndex = prompt("Please enter an index #:");
        // alert(nameList[newIndex]);

            // Ultra Challenge -- Uncomment this section to showcase the Challenge!

        // const challengeArray = ["George", "CJ", "Timothy", "Lisa", "Daniel"];
        // const challengeName = prompt("Please enter a name to check:");
        // alert(challengeArray.includes(challengeName));

    </script>
</body>
</html>
```
{% endtab %}
{% endtabs %}

