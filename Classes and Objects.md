# Classes and Objects
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. 
Classes are essentially a template to create your objects.

## very basic class would look something like this:
class MyClass:
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")
### Accessing Object Variables
myobjectx = MyClass()

myobjectx.variable

## Recursive Functions in Python
 A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

### Maintaining State
When dealing with recursive functions, keep in mind that each recursive call has its own execution context, so to maintain state during recursion you have to either:

Thread the state through each recursive call so that the current state is part of the current call’s execution context

## fixtures 


Fixtures define the steps and data that constitute the arrange phase of a test . In pytest, they are functions you define that serve this purpose. They can also be used to define a test’s act phase; this is a powerful technique for designing more complex tests.

The services, state, or other operating environments set up by fixtures are accessed by test functions through arguments. For each fixture used by a test function there is typically a parameter (named after the fixture) in the test function’s definition.

## Reading Questions 
* What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?
 classes and objects are fundamental concepts in object-oriented programming, and they are used to create and manage instances of a class. Classes define the characteristics and behavior of objects, while objects have their own set of values for the variables defined in the class and can call the methods defined in the class.
 
 ## Things I want to know more about
 1. Classes 
 2. Objects
