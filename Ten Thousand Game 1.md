## Random Module in Python
The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.
The Random module functions namely randint() , random() , choice() , randrange()  and shuffle() 

## Risk Analysis
risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test
* Why use Risk Analysis?
In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks.
* Following points can be taken care of:

1. Conduct Risk Assessment review meeting

2. Use maximum resources to work on high-risk areas

3. Create a Risk Assessment database for future use

4. Identify and notice the risk magnitude indicators: high, medium, low.

* How to perform Risk Analysis?
There are three steps:

1. Searching the risk

2. Analyzing the impact of each individual risk

3. Measures for the risk identified

## Test Coverage
Test coverage is a useful tool for finding untested parts of a codebase.
and it helps you find which bits of your code aren't being tested

## Dependency Injection
dependency injection is a technique whereby one object (or static method) supplies the dependencies of another object. A dependency is an object that can be used
* There are basically three types of dependency injection:
1. constructor injection: the dependencies are provided through a class constructor.
2. setter injection: the client exposes a setter method that the injector uses to inject the dependency.
3. interface injection: the dependency provides an injector method that will inject the dependency into any client passed to it. Clients must implement an interface that exposes a setter method that accepts the dependency.
* Benefits of using DI
1. Helps in Unit testing.
2. Boiler plate code is reduced, as initializing of dependencies is done by the injector component.
3. Extending the application becomes easier.
4. Helps to enable loose coupling, which is important in application programming.
* Disadvantages of DI
1. It’s a bit complex to learn, and if overused can lead to management issues and other problems.
2. Many compile time errors are pushed to run-time.
3. Dependency injection frameworks are implemented with reflection or dynamic programming. This can hinder use of IDE automation, such as “find references”, “show call hierarchy” and safe refactoring.

## Reading Questions
1. How can the random module be utilized in Python to generate random numbers or make selections from a list, and what are some common functions available within the module?
* Generating random numbers:
random():
randint(a, b):
uniform(a, b):
* Making random selections:
choice(seq): 
shuffle(lst): 
getstate(): 

2. In the context of software development, what is risk analysis, and what are the key steps involved in conducting a risk analysis for a software project?
 risk analysis is the process of identifying, assessing, and prioritizing potential risks that may affect the success of a software project.
By effectively identifying and managing risks, software development teams can minimize potential disruptions and increase the chances of project success.
3. What is test coverage and why is it an important (or potentially misleading) metric in software testing?
test coverage is a metric used in software testing to measure the extent to which the source code of a program is exercised by the test suite. It indicates the percentage of code lines, branches, statements, or conditions that have been executed during testing. Test coverage helps assess the effectiveness and completeness of the testing effort, providing insights into the areas of the code that have been tested and those that have not.
4. What is Big O notation, and how is it used to describe the performance of an algorithm? Give an example of an everyday task (not software related) that demonstrates O(n) time complexity.
Big O notation is a mathematical notation used to describe the performance or time complexity of an algorithm. It provides a standardized way to express how the runtime of an algorithm grows in relation to the size of its input.
* O(1): Constant time complexity. The algorithm takes a constant amount of time regardless of the input size.
* O(n): Linear time complexity. The algorithm's runtime grows linearly in proportion to the input size.
* O(n^2): Quadratic time complexity. The algorithm's runtime grows quadratically as the square of the input size.
## Things I want to know more about
* Risk Analysis
