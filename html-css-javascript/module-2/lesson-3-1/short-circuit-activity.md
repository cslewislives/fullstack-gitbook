# Short Circuit - Activity



![Short Circuit](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution.

{% tabs %}
{% tab title="Instructions" %}
**Instructions:**

* Prompt the user for a username and store the response in a variable.
* Prompt the user for a password and store this data.
* If the `username` equals "admin" and the `password` equals "1234", then alert "Welcome to the admin page".
* If the `username` equals "average joe" and the `password` equals "jsRocks", then alert "Welcome to the user landing page".
* Otherwise alert "Invalid username and password, refresh the page to try again"

**Hint:**

You'll need to use the logical operators to make more sophisticated expressions in our if statements.
{% endtab %}

{% tab title="Solution" %}
```markup
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Mastering Conditionals</title>
</head>

<body>
  <script>
    const user = prompt('What\'s your username?');
    const password = prompt('What\'s your password?');
    
    if (user === 'admin' && password === '1234') {
      alert('Welcome to the admin page');
    } else if (user === 'average joe' && password === 'js rocks') {
      alert('Welcome to the user landing page');
    } else {
      alert('Invalid username and password. Refresh the page to retry');
    }
  </script>
</body>

</html>
```
{% endtab %}
{% endtabs %}



