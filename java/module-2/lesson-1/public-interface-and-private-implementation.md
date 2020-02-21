---
description: Separating "what" a class can do from "how" it does it.
---

# Public Interface and Private Implementation

Every class should have a well defined way to interact with the world. Generically, we call this the class's **public interface**. 

The implementation of the class \(the **how**\) should be hidden from the outside world . We call this the class's **private implementation**. 

"Public interface vs. private implementation" allows us to separate the "what" from the "how".

* The  clients of an object should only be concerned with **what it can do**, not how it does it.
* This allows the person implementing the class to reserve the right to change the implementation at their discretion

Some illustrations of public interface v. private implementation are:

* **An ATM machine**
  * The public **what**: The slot where the card is inserted; the key pad were we type the PIN or dollar amount; the touch display screen. 
  * The private **how**: The program that takes our information and processes the transaction.
    * What language is the code written in?
    * How exactly is our account balance being calculated?
    * How is our balance being stored on the bank's system?
* **Amazon.com** 
  * The public **what**: The entire Amazon order interface. 
  * The private **how**: After we press enter, our order is fulfilled and shipped to us, perhaps same day. 
    * Who fulfills our order?
    * Where is it shipped from?
    * Do we know if it even comes from Amazon? Should we care?
* **A drive-thru pharmacy**
  * The public **what**: The drive-up window and the person with whom we interact. 
  * The private **how**:
    * Who dispenses our medicine?
    * How many pharmacists are there working at the store?
    * What does the store even look like? From the window, we might not even be able to tell. 

In the next section, you will be asked to think of your own real-world example of a public interface/private implementation scenario. 

