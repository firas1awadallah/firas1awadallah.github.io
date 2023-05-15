# Scopes and Namespace
## Scopes:
In programming, the scope of a name defines the area of a program in which you can unambiguously access that name, such as variables, functions, objects, and so on.
* Global scope: The names that you define in this scope are available to all your code.
* Local scope: The names that you define in this scope are only available or visible to the code within the scope.
Names and Scopes in Python

## Namespace
In Python, the concept of scope is closely related to the concept of the namespace. As you’ve learned so far, a Python scope determines where in your program a name is visible. Python scopes are implemented as dictionaries that map names to objects. 

* Local (or function) scope is the code block or body of any Python function or lambda expression. This Python scope contains the names that you define inside the function. These names will only be visible from the code of the function. 

* Enclosing (or nonlocal) scope is a special scope that only exists for nested functions. If the local scope is an inner or nested function, then the enclosing scope is the scope of the outer or enclosing function. 

* Global (or module) scope is the top-most scope in a Python program, script, or module. This Python scope contains all of the names that you define at the top level of a program or a module. 

* Built-in scope is a special Python scope that’s created or loaded whenever you run a script or open an interactive session. This scope contains names such as keywords, functions, exceptions, and other attributes that are built into Python. 

### Modules:
* The Local Scope
The local scope or function scope is a Python scope created at function calls. Every time you call a function, you’re also creating a new local scope.
* The Global Scope
From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called __main__ to hold the main program’s execution. 

* Inside func(), you can freely access or reference the value of var. This has no effect on your global name var, but it shows you that var can be freely accessed from within func(). 

* Inside inner_func(): This is the local scope, but number doesn’t exist there.
* Inside outer_func(): This is the enclosing scope, but number isn’t defined there either.

* builtins: The Built-In Scope
The built-in scope is a special Python scope that’s implemented as a standard library module named builtins in Python 3.

### There are many built-in functions that are closely related to the concept of Python scope and namespaces. 

* globals()
In Python, globals() is a built-in function that returns a reference to the current global scope or namespace dictionary. This dictionary always stores the names of the current module. This means that if you call globals() in a given module, then you’ll get a dictionary containing all the names that you’ve defined in that module, right before the call to globals(). 
* locals()
Another function related to Python scope and namespaces is locals(). This function updates and returns a dictionary that holds a copy of the current state of the local Python scope or namespace. When you call locals() in a function block, you get all the names assigned in the local or function scope up to the point where you call locals(). 
* vars()
vars() is a Python built-in function that returns the .__dict__ attribute of a module, class, instance, or any other object which has a dictionary attribute. Remember that .__dict__ is a special dictionary that Python uses to implement namespaces.
* dir()
You can use dir() without arguments to get the list of names in the current Python scope. If you call dir() with an argument, then the 
function attempts to return a list of valid attributes for that object

## Reading Questions
1. Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.

* Local Scope: Variables defined within a function have a local scope. They are accessible only within the function where they are defined. Local variables have a limited lifespan and are created when the function is called and destroyed when the function completes execution. 
* Global Scope: Variables defined outside any function or code block have a global scope. They are accessible throughout the entire program, including inside functions. Global variables have a longer lifespan and exist as long as the program is running.

2. How do the global and nonlocal keywords work in Python, and in what situations might you use them?
In Python, the global and nonlocal keywords are used to access variables in enclosing scopes. Here's how they work:

* Global Keyword: The global keyword is used to indicate that a variable within a function should be treated as a global variable, even if it has the same name as a local variable or if it is defined outside the function.
* Nonlocal Keyword: The nonlocal keyword is used to indicate that a variable within a nested function should be treated as a nonlocal variable, rather than a local or global variable. It allows you to access and modify variables from the nearest enclosing scope, which is not the global scope.

3. In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.

* Big O notation provides a standardized way to analyze and compare algorithms, enabling us to reason about their efficiency, predict their performance, and make informed decisions when designing and optimizing software systems. 

4. Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.

* you can use the randint() function to generate a random integer between two specified values(1,6), representing the possible outcomes of a dice roll.

* To calculate the probability of rolling a specific number, such as the probability of rolling a 6, over a large number of trials, The probability is then estimated by dividing the number of successful outcomes by the total number of trials.

## Things I want to know more about
1. Scopes
2. Namespace
3. Modules
