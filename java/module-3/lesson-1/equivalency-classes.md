# Equivalency Classes

### Can't Test Every Input

Now we just discussed testing for multiple inputs however, when unit testing we can’t test **every** possible input. 

We need to group inputs together into **equivalency classes**. 

If our add method can add 1+2 and 100+15 and 43+72, it stands to reason that it can handle all positive integers with some upper bound based on memory limitations.

#### What equivalency classes might we have for an add method?

Some possible options include:

* Positive integers
* Negative integers
* One positive and one negative
* Zeros
* One zero along with a positive
* One zero along with a negative
* Two integers whose sum exceeds the maximum or minimum allowed integer

Can you think of any others?

