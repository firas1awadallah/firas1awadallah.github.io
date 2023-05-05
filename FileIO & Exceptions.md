# File & Exceptions

## File?
a file is a contiguous set of bytes used to store data. This data is organized in a specific format and can be anything as simple as a text file or as complicated as a program executable. In the end, these byte files are then translated into binary 1 and 0 for easier processing by the computer.


Files on most modern file systems are composed of three main parts:
*Header: metadata about the contents of the file (file name, size, type, and so on)
*Data: contents of the file as written by the creator or editor
*End of file (EOF): special character that indicates the end of the file

### File Paths
The file path is a string that represents the location of a file. It’s broken up into three major parts:
1. Folder Path: the file folder location on the file system where subsequent folders are separated by  backslash \ (Windows)
2. File Name: the actual name of the file
3. Extension: the end of the file path pre-pended with a period (.) used to indicate the file type

### Opening and Closing a File in Python
When you want to work with a file, the first thing to do is to open it. This is done by invoking the open() built-in function. open() has a single required argument that is the path to the file. open() has a single return, the file object:

* reader. open()
After you open a file, the next thing to learn is how to close it.
* reader.close()

### Reading and Writing Opened Files
Once you’ve opened up a file, you’ll want to read or write to the file. First off, let’s cover reading a file. There are multiple methods that can be called on a file object to help you out:
* reader.read()
. As with reading files, file objects have multiple methods that are useful for writing to a file:
* write() and .writelines()

## Exceptions
A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception. 
Exceptions versus Syntax Errors
Syntax errors occur when the parser detects an incorrect statement. 
SyntaxError: invalid syntax


### The AssertionError Exception
Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We assert that a certain condition is met. If this condition turns out to be True, then that is excellent! The program can continue. If the condition turns out to be False, you can have the program throw an AssertionError exception.


Summing Up:
1. raise allows you to throw an exception at any time.
2. assert enables you to verify if a certain condition is met and throw an exception if it isn’t.
3. In the try clause, all statements are executed until an exception is encountered.
4. except is used to catch and handle the exception(s) that are encountered in the try clause.
5. else lets you code sections that should run only when no exceptions are encountered in the try clause.
6. finally enables you to execute sections of code that should always run, with or without any previously encountered exceptions.

## Reading Questions Answer 

1. What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?

In Python, the with statement is used when working with files to ensure that a file is closed properly after it has been used. The primary purpose of using the with statement when opening a file is to manage resources like file descriptors in a way that's cleaner, safer, and more readable than traditional methods of opening and closing files.


2. Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method.


The read() method reads the entire contents of the file into a single string, while the readline() method reads a single line of the file at a time. The read() method returns the entire contents of the file as a string, while the readline() method returns a single line of the file as a string.

*  use the read() method:

with open('example.txt', 'r') as f:
    content = f.read()
In this example, the entire contents of the file example.txt are read into the content variable as a string.

Here's an example of how to use the readline() method:

with open('example.txt', 'r') as f:
    line = f.readline()
    while line:
        print(line)
        line = f.readline()


3. Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.

In Python, exception handling is a way of dealing with errors or exceptional situations that may occur during the execution of a program. The try, except, and finally blocks are used to handle exceptions in Python, with the try block enclosing the code that may raise an exception, the except block handling the exception, and the finally block executing code that should be run regardless of whether an exception was raised or not.
* use try, except, and finally :

try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("This will always execute")
The output of this code will be:
Cannot divide by zero

## Things I want to know more about
Files and exceptions and how exceptions are used to handle errors and unexpected situations that may arise during the execution of a program.
