# Conditional Warmup - Activity

![Conditional Warmup](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions**

We're building an application to allow a student to track their classes each semester. Students need to be able to update their list of classes in case they change one midway through the semester.

Using the given `classList` array:

1. Prompt the user for the name of a class they would like to update.
2. Prompt the user for a new class name.
3. Replace the old class name with the new one.

```markup
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Conditionals Activity</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
    
    <script>
        const classList = ['Math', 'Science', 'English', 'Music', 'Intro to Programming', 'Basketweaving'];
        
        // Remember to open up chrome dev tools to see your class list!
        console.log(classList);

        // Add your code below. Don't forget to console log classList again to see if the changes have taken place!

    </script>
</body>
</html>
```

**Challenge:**

Do the above without writing a for loop.
{% endtab %}

{% tab title="Solution" %}
```markup
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Conditionals Activity</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
    
    <script>
        const classList = ['Math', 'Science', 'English', 'Music', 'Intro to Programming', 'Basketweaving'];
        
        // Remember to open up chrome dev tools to see your class list!
        console.log(classList);

        const replaceClass = prompt('Please select which class you would like to replace (case sensitive!):'); 
        const newClass = prompt('Please enter the name of a new class:');
        
        for ( let i = 0; i < classList.length; i++ ) {
            if (classList[i] === replaceClass) {
                classList[i] = newClass;
            }
        }

        // Challenge
        if (classList.includes(replaceClass)) {
            const newIndex = classList.indexOf(replaceClass);
            classList[newIndex] = newClass;
        }

        console.log(`This is your new class list: ${classList}`);
    </script>
</body>
</html>
```
{% endtab %}
{% endtabs %}

 

