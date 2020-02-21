# Boolean Coercion - Activity

![Boolean Coercion](../../../.gitbook/assets/image%20%2837%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

Study the JavaScript code inside of the `script` tags.

```markup
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Boolean Coercion</title>
</head>

<body>

  <script>
    const age = prompt('How old are you?');

    // What would we put inside of the parentheses to check if the user supplied an age?
    if () {
      alert(`You are ${age}`);
    } else {
      alert('You did not input your age');
    }
    
  </script>
  
</body>

</html>
```

Without using the equality comparison operator \(`===`\) what could you write inside the parentheses for the `if`statement to check if the user has supplied a value to `age`?

**Hints:**

Run the code and when prompted for an age, press enter without inputting anything and try to log the type and value of age.

Utilize `console.log` to check possible solutions for truthy and falsy values.

Don't try to run the code without adding a condition to the `if` statement. You'll get a syntax error for not having a value inside the `if () {` parentheses.
{% endtab %}

{% tab title="Solution" %}
```markup
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Boolean Coercion</title>
</head>

<body>

  <script>
    const age = prompt('How old are you?');

    // Inside of the if statement, age is cast to a boolean
    if (age) {
      alert(`You are ${age}`);
    } else {
      alert('You did not input your age');
    }
    
  </script>

</body>

</html>
```
{% endtab %}
{% endtabs %}

