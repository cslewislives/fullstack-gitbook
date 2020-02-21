# Prompt/Alert - Activity

![Prompt/Alert](../../../.gitbook/assets/image%20%284%29.png)

Make sure you attempt the activity on your own before checking out the solution. 

{% tabs %}
{% tab title="Instructions" %}
**Instructions**

In this activity we will collect some information from the user using prompt and confirm dialogues, and alert the information back at the user.

Update the `script` tag in the following code using `prompt` to collect the following information from the user:

1. Their name
2. Their email address
3. A password \(should be fake\)

Store each value inside of a variable. Once each value has been collected, use an `alert` dialog to display all of the information back to the user.

```markup
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
	<script>
    const greeting = prompt('enter your name');
    alert('Hello ' + greeting);
	</script>
</body>
</html>
```

**Challenge**

Use the [confirm dialog](https://www.tutorialspoint.com/javascript/javascript_dialog_boxes.htm) to ask the user if they would like their login credentials to be remembered and `alert` the response back to the user.
{% endtab %}

{% tab title="Solution" %}
```markup
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>Prompt & Alert</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>
<body>
    
    <script>
        const userName = prompt('What is your name?');
        const userEmail = prompt('What is your email?');
        const userPass = prompt('Enter a password.');

        // CHALLENGE
        const userConfirm = confirm('Would you like your login credentials to be remembered?');

        alert(`Username: ${userName}`);
        alert(`Email: ${userEmail}`);
        alert(`Password: ${userPass}`);

        // CHALLENGE
        alert(`Remember Login Credentials? ${userConfirm}`);

    </script>
</body>
</html>
```
{% endtab %}
{% endtabs %}

