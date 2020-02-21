---
description: Understanding real world models in order to turn them into code.
---

# Abstraction

As we think about the world around us, what kind of **tools** help us to accomplish everyday tasks like getting directions to a new restaurant or saving an email attachment to our computer? What about more complex tasks like building a garden-shed or putting together some flat-pack furniture?

If you answered Google Maps, files and folders on our computer desktop, construction blue prints or Ikea's famous step-by-step directions, you are on the correct path. 

What do all of these seemingly dis-separate things all have in common? They are **models**, or abstractions, of the things that will help us accomplish our goal. 

Google Maps is a model of the actual streets that we need to traverse in order to get to dinner; the Finder window on my Mac is a model of my computer's internal file structure; the construction plans and Ikea directions contain the exact information we need to assemble our structure while eliminating the extraneous details.

> Models and metaphors are important to programming languages as well. Java is an **object oriented** language that models everything as...you guessed it...**objects**. We'll see how that helps us model and solve problems with Java."

### Abstraction Defined

Abstraction is the representation of essential features without including the background details or explanations. In software development, abstraction is used to reduce complexity and allow efficient design and implementation of complex software systems by allowing developers to include only the relevant features of a problem.

#### Real World Examples of Abstraction

* The desktop metaphor in Windows, Mac, and Linux - images of files and folders are a simplified representation of the Unix file structure that exists on our computers. Using Terminal/Gitbash is a window into that structure. 
* Password 'vaults' such as LastPass.
* Email - The very efficient user-interface masks the complexity of the process. 

### Abstraction in Computer Languages

All programming languages use abstraction in some way.

One approach is to start with the format of the solution and then map the problem into that format. 

Low level languages do this – they closely mimic how a computer works and it is up to the programmer to map the problem space into something close to how a computer works \(which may or may not be convenient\).

* Assembly language  - Assembly's world view is almost the same as the computer. It is very logical. The language mirrors how the computer actually works very closely. The language does not abstract the computer away for the developer. The developer is required to map the problem almost directly to how a computer works.

Some languages model everything as lists or mathematical functions.

* Functional language - Functional languages model everything as mathematical functions. Again, the developer is require to map their problem into the language worldview.
* Lisp - Lisp represents almost everything as a list. Developers must map their problems into the Lisp worldview

Object-oriented languages model everything as objects, which is convenient since almost everything in the real world is an object.

* Object-oriented languages model everything around data, rather than logic or functions. An object can be defined as a data field that has unique attributes and behaviors. 
* Java, JavaScript, Python and C++ are a few examples of object-oriented programming languages. 

In the next section, we will examine the characteristics of an object-oriented programming language more closely. 

