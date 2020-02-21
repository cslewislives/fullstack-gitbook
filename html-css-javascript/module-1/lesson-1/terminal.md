# Terminal

### **What, Why, and When**

The terminal/gitbash is a way to interact with your computer via text only.

Creating directories and files on your computer through the terminal is much more efficient than creating them through the graphical interface. The terminal will also be a vital tool when we start using version control software which we'll learn about shortly.

Developers use the terminal every day at work. It may feel clunky now, but with practice it will make you a much better developer.

After this section, you will be able to navigate your computer's folder structure and perform basic operations using only the terminal.

### Creating Files and Folders

Normally when creating a new folder most people will right click using the mouse then choose **New &gt; Folder**. Then they will create a new file in whatever software they are using, etc.

We can do these same steps all in one place using Terminal or GitBash for Windows

{% hint style="info" %}
To install GitBash head over to [https://git-scm.com/downloads](https://git-scm.com/downloads)
{% endhint %}

Go ahead and open terminal if you are on a Mac or GitBash if you are on a PC.

Terminal or GitBash should open to your home directory. This will be indicated by the `~` at the end of the line.

![](../../../.gitbook/assets/image%20%2812%29.png)

Navigate to your desktop by typing `cd Desktop` and hitting enter. 

![](../../../.gitbook/assets/cd-desktop.gif)

**Notice** that I didn't finish typing Desktop. I used **tab complete** to finish the name for me. `tab` only works when you have a _unique_ file or directory name that matches. Ex \(`cd pota` will work if you have a directory named `potato` and no other directories that start with `pota`\).

Next type `mkdir <directory name>` then `cd` into the directory and use `touch` to create an empty file. 

![](../../../.gitbook/assets/image%20%2817%29.png)

We can use the `ls` command to view the contents of the directory.

![](../../../.gitbook/assets/image%20%2829%29.png)

You can check graphically that the new directory exists on your desktop and has a file inside. 

![](../../../.gitbook/assets/image%20%2861%29.png)

This is simply two ways of accomplishing the same thing, but developer jobs require you to master the terminal way of doing it.

Don't worry about trying to remember all of the commands, there are great resources out there to help you remember.

![](../../../.gitbook/assets/command-cheat-sheet.png)

