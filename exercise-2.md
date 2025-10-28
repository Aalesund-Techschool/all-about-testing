# Exercise 2 - Exceptions, failures and errors

This exercise will cover how to test code that throws exceptions, and explore what the difference between failures and
errors are in tests.

## You will learn how to:

1. Check for exceptions in a test
2. Understand the difference between failures and errors

# 2.1. Checking for exceptions

Sometimes an exception is the correct result of a test. For example, if we have some code validating if a given input is
a valid phone number, in most cases the code would be set up to throw an exception if the input is not a valid phone
number.

JUnit provides some syntax to check for exceptions in a test:

```Java

@Test
void test() {
    assertThrows(Exception.class, () -> ...)
}
```

:pencil2: Take a look at the `SmoothieBar` class. The `blend` method will throw a `IllegalStateException` if the stock
of ingredients required for the smoothie to be blended is to low.  
:pencil2: Create a test that tests this logic (hint: It has something to do with restocking ingredients).  
:pencil2: Run the test, see that test fails with the `IllegalStateException` as cause.  
:pencil2: Use `expected` syntax above to make green again.  
:pencil2: What other behaviors causes `blend` to throw exception(s)? Write test(s) confirming the behavior.

### [Go to exercise 3 :arrow_right:](exercise-3.md)
