# GitHub

### **What, Why, and When**

GitHub is an online space to work collaboratively on projects and keep your code safe.

Most software requires teams of developers to work simultaneously in a safe way. GitHub is a tool that allows us to do that. We will cover only a few features of version control software today, but it is a powerful tool on which all developers rely heavily.

Virtually every software company stores its code GitHub or a similar service. 

Think about Google Drive: what is it?

It's a space to back up pictures and documents and share them with others.

When we work on projects as developers we need a similar service that backs up our work and allows us to share it and collaborate with others on it. The most popular tool for this is GitHub.

{% hint style="info" %}
 An explanation of why version control software like GitHub is important can be found in this [Medium article](https://medium.com/@lanceharvieruntime/version-control-why-do-we-need-it-1681f4888cec).
{% endhint %}

### Creating a Repository

* Head over to [https://github.com/ ](https://github.com/)and register for an account.
* Create a new repository using either of these buttons:

![](../../../.gitbook/assets/image%20%2838%29.png)

![](../../../.gitbook/assets/image%20%2864%29.png)

* Give the repository a name and make sure to initialize with a README

![](../../../.gitbook/assets/image%20%283%29.png)

* Click on clone or download and copy the link

![](../../../.gitbook/assets/image%20%2878%29.png)

* In terminal, or GitBash,`cd` into the directory where you want your repo to live
* Clone the repo using `git clone <repo link>`

![](../../../.gitbook/assets/image%20%2822%29.png)

![](../../../.gitbook/assets/image%20%2831%29.png)

Now that you have cloned the repo onto your machine you should see the new folder graphically. 

### Pushing to a Repository

Once your repo is cloned onto your machine `cd` into the repo and from there you can start adding new files and folders.

Once you have new files added we will need to push them to our GitHub repo in order to really harness the power of version control. Follow these steps:

* Stage the changes using `git add -A` **or** `git add .` 
  * Both of these commands adds **all** of the files to the commit
  * You can also add specific files but generally you want to add all.
* Commit the changes using `git commit -m "some message"`
  * It's good practice to make all of your commit messages lower case and a descriptive verb
  * Ex: `git commit -m "adds button functionality"` or `"fixes error messaging"`
* Push the changes using `git push origin master`

![](../../../.gitbook/assets/image%20%2855%29.png)

![](../../../.gitbook/assets/github-cheat-sheet.png)

