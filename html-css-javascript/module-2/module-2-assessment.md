# Module 2 Assessment

### Before You Begin

1. Create a new folder in your **prework repo** called `Module-2_Assessment`
2. Inside your `Module-2_Assessment` folder, create an `index.html`.
3. While still in that folder, create a directory called `assets`.
4. `cd` your way into the `assets` folder, then make three additional folders: `javascript`, `css` and `images`.
   * In the `javascript` folder, make a file called `game.js`. Use the `src` attribute of the `script` tag to link to this file, rather than embedding the code directly in your HTML document.
   * In the `css` folder, make a file called `style.css`.
   * Also in the `css` folder, make a file called `reset.css`. Paste into it the code from the Meyerweb reset stylesheet. If you opt to use Bootstrap instead of writing your own CSS, skip this step, and simply include a link to Bootstrap via CDN.
   * In the `images` folder, save whatever images you plan on using. 

```text
├── assets
|  ├── css
|  |  └── style.css
|  ├── images
|  └── javascript
|     └── game.js
└── index.html
```

Push the above changes to GitHub.

### Word Guess Game

1. [Watch the demo](https://youtu.be/W-IJcC4tYFI).
2. Choose a theme for your game! In the demo, we picked an 80s theme: 80s questions, 80s sound and an 80s aesthetic. You can choose any subject for your theme, though, so be creative!
3. Use key events to listen for the letters that your players will type.
4. Display the following on the page:
   1. Press any key to get started!
   2. Wins: \(\# of times user guessed the word correctly\).
      * If the word is `madonna`, display it like this when the game starts: `_ _ _ _ _ _ _`.
      * As the user guesses the correct letters, reveal them: `m a d o _ _ a`.
   3. Number of Guesses Remaining: \(\# of guesses remaining for the user\).
   4. Letters Already Guessed: \(Letters the user has guessed, displayed like `L Z Y H`\).
5. After the user wins/loses the game should automatically choose another word and make the user play it.

### **Word Guess Game Bonuses**

1. Play a sound or song when the user guesses their word correctly, like in our demo.
2. Write some stylish CSS rules to make a design that fits your game's theme.
3. **HARD MODE:** 
   1. Organize your game code as an object, except for the key events to get the letter guessed. This will be a challenge if you haven't coded with JavaScript before, but we encourage anyone already familiar with the language to try this out.
   2. Save your whole game and its properties in an object.
   3. Save any of your game's functions as methods, and call them underneath your object declaration using event listeners.
   4. Don't forget to place your global variables and functions above your object.
      * Remember: global variables, then objects, then calls.

### **A Few Tips**

1. **IMPORTANT:** Code your game one piece at a time! Code all of your apps one piece at a time. _Always code one piece at a time!_
2. Flowchart/pseudocode your program and break the app down into tiny, manageable fragments. This will make the coding process much less frustrating and a veritable Mach number faster. Otherwise, you'll be chipping away at a giant chunk of abstraction for way too many hours.
   * The ability to solve a large problem by treating it as a set of smaller ones is the hallmark of a strong programmer. Best start adapting this into your development routine now, to better prepare for your more complex future projects.
   * Remember:
     1. Split the whole program into many distinct, pseudocoded problems.
     2. Focus on one of the smaller problems and solve it.
     3. Only when you solve one problem should you then move onto your next problem.
3. When you encounter bugs \(and we all do\), `console.log` will become your best friend. Regularly check your console to make sure your app is spitting out the right values.
   * As a more advanced—but more powerful—alternative, feel free to experiment with the [Chrome DevTools Debugger](https://developers.google.com/web/tools/chrome-devtools/).
4. Try your best to deliver a 'working/playable game' by the end of the deadline.
5. Substance over style! Submitting a working game matters more that making a broken app that at least looks pretty. We're focusing on game mechanics, not just on the look and feel of your app.
6. That said, coding a functional app that also looks pretty would be impressive.
7. Always commit your work and back it up with GitHub pushes. You don't want to lose hours of your work because you didn't push it to GitHub every half hour or so.
   * **Commit often**.
8. Turn in anything you have! Even if you don't finish, we still want to see what you were able to accomplish in the time we gave you.

### Minimum Requirements

Attempt to complete the assessment as described in instructions. If unable to complete certain portions, please pseudocode these portions to describe what remains to be completed. Adding a README.md as is required as well and more information can be found below.

### Create a README.md

Add a `README.md` to your repository describing the project. Here are some resources for creating your `README.md`. Here are some resources to help you along the way:

* [About READMEs](https://help.github.com/articles/about-readmes/)
* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

**Good Luck!**

