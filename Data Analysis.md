# Data Analysis

## Reading Questions

1. What are the key features and benefits of Jupyter Lab, and how does it differ from Jupyter Notebook?
* JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. 

* You can arrange multiple documents and activities side by side in the work area using tabs and splitters. Documents and activities integrate with each other, enabling new workflows for interactive computing, 

* Code Consoles provide transient scratchpads for running code interactively, with full support for rich output. A code console can be linked to a notebook kernel as a computation log from the notebook, 

* Notebook cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.

* To navigate the user interface, JupyterLab offers customizable keyboard shortcuts and the ability to use key maps from vim, emacs, and Sublime Text in the text editor.

* JupyterLab extensions can customize or enhance any part of JupyterLab, including new themes, file editors, and custom components.
2. What are the main functionalities provided by the NumPy library, and how can it be useful in Python programming, particularly for scientific computing and data manipulation tasks?
* NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. 

* Lists Of Lists for CSV Data
Before using NumPy, we'll first try to work with the data using Python and the csv package. We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.

Import the csv library.
1. Open the winequality-red.csv file.
2. With the file open, create a new csv.reader object.
3. Pass in the keyword argument delimiter=";" 
4. Call the list type to get all the rows from the file.
5. Assign the result 

* Extract the last element from each row after the header row.
1. Convert each extracted element to a float.
2. Assign all the extracted elements to the list qualities.
3. Divide the sum of all the elements in qualities by the total number of elements in qualities to the get the mean.
## Numpy 2-Dimensional Arrays
With NumPy, we work with multidimensional arrays., but for now, we'll focus on 2-dimensional arrays. A 2-dimensional array is also known as a matrix, and is something you should be familiar with.  A matrix has rows and columns. By specifying a row number and a column number, we're able to extract an element from a matrix.

## Creating A NumPy Array
We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we'll leave off the header row, which contains strings. One of the limitations of NumPy is that all the elements in an array have to be of the same type, so if we include the header row, all the elements in the array will be read in as strings.

1. Import the numpy package.
2. Pass the list of lists wines into the array function, which converts it 3. into a NumPy array.
4. Exclude the header row with list slicing.
5. Specify the keyword argument dtype to make sure each element is converted to a float. 


* We can check the number of rows and columns in our data using the shape property of NumPy arrays:
Alternative NumPy Array Creation Methods
There are a variety of methods that you can use to create NumPy arrays. To start with, you can create an array where every element is zero. 


* Using NumPy To Read In Files
It's possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function. 
1. Use the genfromtxt function to read in the winequality-red.csv file.
2. Specify the keyword argument delimiter=";" so that the fields are parsed properly.
3. Specify the keyword argument skip_header=1 so that the header row is skipped.

3. Explain the basic structure and properties of NumPy arrays, and provide examples of how to create, manipulate, and perform operations on them.
NumPy is a powerful library in Python for numerical computations, particularly for working with arrays. NumPy arrays are multi-dimensional, homogeneous data structures that allow efficient storage and manipulation of large amounts of numerical data.

1. Importing NumPy:
2. Creating NumPy arrays:
3. Array attributes:
4. Array indexing and slicing:
5. Array operations:
6. 
## Indexing NumPy Arrays
We now know how to create arrays, but unless we can retrieve results from them, there isn't a lot we can do with NumPy. We can use array indexing to select individual elements, groups of elements, or entire rows and columns. One important thing to keep in mind is that just like Python lists, NumPy is zero-indexed, meaning that the index of the first row is 0, and the index of the first column is 0. If we want to work with the fourth row, we'd use index 3, if we want to work with the second row, we'd use index 1, and so on.

* 1-Dimensional NumPy Arrays
So far, we've worked with 2-dimensional arrays, such as wines. However, NumPy is a package for working with multidimensional arrays. One of the most common types of multidimensional arrays is the 1-dimensional array, or vector. As you may have noticed above, when we sliced wines, we retrieved a 1-dimensional array. A 1-dimensional array only needs a single index to retrieve an element. Each row and column in a 2-dimensional array is a 1-dimensional array. Just like a list of lists is analogous to a 2-dimensional array, a single list is analogous to a 1-dimensional array. If we slice wines and only retrieve the third row, we get a 1-dimensional array:

* N-Dimensional NumPy Arrays
This doesn't happen extremely often, but there are cases when you'll want to deal with arrays that have greater than 3 dimensions. One way to think of this is as a list of lists of lists. Let's say we want to store the monthly earnings of a store, but we want to be able to quickly lookup the results for a quarter, and for a year. 


* NumPy Data Types
NumPy has several different data types, which mostly map to Python data types, like float, and str. You can find a full listing of NumPy data types here, but here are a few important ones:

1. float -- numeric floating point data.
2. int -- integer data.
3. string -- character data.
4. object -- Python objects.
Data types additionally end with a suffix that indicates how many bits of memory they take up. So int32 is a 32 bit integer data type, and float64 is a 64 bit float data type.

* Converting Data Types
You can use the numpy.ndarray.astype method to convert an array to a different type. The method will actually copy the array, and return a new array with the specified data type. For instance, we can convert wines to the int data type:


1. NumPy Array Operations
NumPy makes it simple to perform mathematical operations on arrays. This is one of the primary advantages of NumPy, and makes it quite easy to do computations.

2. Single Array Math
If you do any of the basic mathematical operations (/, *, -, +, ^) with an array and a value, it will apply the operation to each of the elements in the array.



3. Multiple Array Math
It's also possible to do mathematical operations between arrays. This will apply the operation to pairs of elements. For example, if we add the quality column to itself, here's what we get:

## Broadcasting
Unless the arrays that you're operating on are the exact same size, it's not possible to do elementwise operations. In cases like this, NumPy performs broadcasting to try to match up elements. Essentially, broadcasting involves a few steps:

1. The last dimension of each array is compared.
2. If the dimension lengths are equal, or one of the dimensions is of length 1, then we keep going.
3. If the dimension lengths aren't equal, and none of the dimensions have length 1, then there's an error.
4. Continue checking dimensions until the shortest array is out of dimensions.

NumPy Array Methods
In addition to the common mathematical operations, NumPy also has several methods that you can use for more complex calculations on arrays. An example of this is the numpy.ndarray.sum method. This finds the sum of all the elements in an array by default:


* There are several other methods that behave like the sum method, including:

1. numpy.ndarray.mean — finds the mean of an array.
2. numpy.ndarray.std — finds the standard deviation of an array.
3. numpy.ndarray.min — finds the minimum value in an array.
4. numpy.ndarray.max — finds the maximum value in an array.
You can find a full list of array methods here.

## NumPy Array Comparisons
NumPy makes it possible to test to see if rows match certain values using mathematical comparison operations like <, >, >=, <=, and ==. 

## Things I want to know more about
* more than about Data Analysis
