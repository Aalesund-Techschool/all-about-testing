# Exercise 4 - Test Driven Development (TDD)

In this exercise we'll learn how to apply the TDD methodology when we're writing code.  

## What is TDD

Test Driven Development is a way of writing code where we will **always** (a-l-w-a-y-s) write tests for our code
**before** we write the implementation code.

But wait! This means our code won't even compile, silly! Why yes. Yes it does.

So how does this makes sense?

## :book: How to do TDD

> :exclamation: This section contains a walkthrough of how to approach TDD. You should just read along, making sure you understand the workflow. You don't have to implement the calculator example yourself, the screenshots below are just for demonstration.

When following TDD, we always code in a certain pattern nicknamed "red-green-refactor".

![tdd](http://www.agilenutshell.com/assets/test-driven-development/tdd-circle-of-life.png)

### Red

First, we create a test.

![tdd1](../images/tdd1.PNG)

Then, we start implementing the test based on how we plan the implementation to work.

![tdd1](../images/tdd2.PNG)

Why not leverage the power of IntelliJ to help us out creating things as we go? Use `ALT+ENTER` or click the light-bulb.

![tdd1](../images/tdd3.png)

Ensure it selects the correct package

![tdd1](../images/tdd4.png)

Voila! The `Calculator.java` class and file has been created.

Let's continue in ``CalculatorTest.java``

I know I want an ``add`` function that takes two arguments and returns a value so I just start writing it so.

Again, there is no implementation, but I use ``ALT+ENTER`` to make IntelliJ create what I need.

![tdd1](../images/tdd5.png)

I now have an ``Calculator`` class that looks like this without having to write anything myself.

![tdd1](../images/tdd6.PNG)

Back in ``CalculatorTest`` I add the last line, then assert for the result.

![tdd1](../images/tdd7.PNG)

I can finally run the test (``CTRL+SHIFT+F10`` when the cursor is on the test, or the icon in the gutter).

As expected, it fails because there is no actual implementation yet.

![tdd1](../images/tdd8.PNG)

### Green

Now that we have a failing test, we can continue on to the next step - making it pass.

The only question you need to answer at this point: _what is the smallest amount of code I need to implement to make
this specific test pass?_

In the case of making the ``add()`` function work, it's quite simple

![tdd1](../images/tdd9.PNG)

Run the test again, and it goes green!

![tdd1](../images/tdd10.PNG)

### Refactor

Now that we have finished our test, we can refactor our code if necessary. Refactoring code just means to change
it's implementation details without changing it's behaviour. So we can change it, but our test should from now on always pass.

For the simple example we're using in these examples there's not much refactoring to do.

### Repeat

Now that ``add()`` is implemented, we can add more features to our calculator in the same way:
Write the test, implement the feature, make the test pass, refactor.

## Tasks

Exercise 4 contains a skeleton for a simple ``MonthParser`` class. It has one function: `parseMonth(int numberOfMonth)`
which given a number, returns a ``Month`` instance containing the month's name ("January", "February", etc) and the number of days
it contains.

_Please read all the text below before starting_.

:pencil2: Open exercise4 pom.xml file as a project in IntelliJ (same procedure as exercise 1).  
:pencil2: Using TDD **only**, implement the ``parseMonth`` method for at least 6 out of the 12 months. You can find a list of days in each month [here](http://www.howmanydaysin.com/).  
:pencil2: You should go through the red-green-refactor cycle (at least) _6 times_ in this exercise, one for each month.  
:poop: Copy & pasting code, or implementing more than one month at a time is strictly forbidden.  
:exclamation: There should be at least _one test per month_.  
:exclamation: There should be tests making sure we cannot enter invalid numbers (only 1 through 12 allowed, no negative numbers).  
:exclamation: The point of this exercise is not to come up with the most clever date time/month parsing algorithm ever created. Simply assert that you expect the month `1` to return a month named `January` with `31` days, then implement the least amount of code to make that happen and repeat for the next month.

### [Go to Bonus exercise 1 :arrow_right:](../exercise-5/README.md)
