## Linear Regressions

### What Is Regression?
Regression searches for relationships among variables. For example, you can observe several employees of some company and try to understand how their salaries depend on their features, such as experience, education level, role, city of employment, and so on.


* The dependent features are called the dependent variables, outputs, or responses. The independent features are called the independent variables, inputs, regressors, or predictors.

* When Do You Need Regression?
Typically, you need regression to answer whether and how some phenomenon influences the other or how several variables are related. For example, you can use it to determine if and to what extent experience or gender impacts salaries.


Regression is used in many different fields, including economics, computer science, and the social sciences. Its importance rises every day with the availability of large amounts of data and increased awareness of the practical value of data.

* Linear Regression
Linear regression is probably one of the most important and widely used regression techniques. It’s among the simplest regression methods. One of its main advantages is the ease of interpreting results.

* Multiple Linear Regression
Multiple or multivariate linear regression is a case of linear regression with two or more independent variables.
If there are just two independent variables, then the estimated regression function is 𝑓(𝑥₁, 𝑥₂) = 𝑏₀ + 𝑏₁𝑥₁ + 𝑏₂𝑥₂. It represents a regression plane in a three-dimensional space. The goal of regression is to determine the values of the weights 𝑏₀, 𝑏₁, and 𝑏₂ such that this plane is as close as possible to the actual responses, while yielding the minimal SSR.

* Polynomial Regression
You can regard polynomial regression as a generalized case of linear regression. You assume the polynomial dependence between the output and inputs and, consequently, the polynomial estimated regression function.


### Underfitting and Overfitting

* Underfitting occurs when a model can’t accurately capture the dependencies among data, usually as a consequence of its own simplicity. It often yields a low 𝑅² with known data and bad generalization capabilities when applied with new data.

* Overfitting happens when a model learns both data dependencies and random fluctuations. In other words, a model learns the existing data too well. Complex models, which have many features or terms, are often prone to overfitting. When applied to known data, such models usually yield high 𝑅². However, they often don’t generalize well and have significantly lower 𝑅² when used with new data.

### Model linear regressions: 
* Linear regression can be thought of as finding the straight line that best fits a set of scattered data points: 
* Scikit-learn is a Python package that simplifies the implementation of a wide range of Machine Learning (ML) methods for predictive data analysis, including linear regression.
* Linear Regression Concepts
The following are some key concepts you will come across when you work with scikit-learn’s linear regression method:
1. Best Fit – the straight line in a plot that minimizes the deviation between related scattered data points.
2. Coefficient – also known as a parameter, is the factor a variable is multiplied by. In linear regression, a coefficient represents changes in a Response Variable (see below).
3. Coefficient of Determination – the correlation coefficient denoted as 𝑅². Used to describe the precision or degree of fit in a regression. 
4. Correlation – the relationship between two variables in terms of quantifiable strength and degree, often referred to as the ‘degree of correlation’.  Values range between -1.0 and 1.0. 
5. Dependent Feature – a variable denoted as y in the slope equation y=ax+b. Also known as an Output, or a Response. 
6. Estimated Regression Line – the straight line that best fits a set of scattered data points.
7. Independent Feature – a variable denoted as x in the slope equation y=ax+b. Also known as an Input, or a predictor. 
8. Intercept – the location where the Slope intercepts the Y-axis denoted b in the slope equation y=ax+b. 
9. Least Squares – a method of estimating a Best Fit to data, by minimizing the sum of the squares of the differences between observed and estimated values.
10. Mean – an average of a set of numbers, but in linear regression, Mean is modeled by a linear function.
11. Ordinary Least Squares Regression (OLS) – more commonly known as Linear Regression. 
12. Residual – vertical distance between a data point and the line of regression (see Residual in Figure 1 below).
13. Regression – estimate of predictive change in a variable in relation to changes in other variables (see Predicted Response in Figure 1 below).
14. Regression Model – the ideal formula for approximating a regression.
15. Response Variables – includes both the Predicted Response (the value predicted by the regression) and the Actual Response, which is the actual value of the data point (see Figure 1 below).
16. Slope – the steepness of a line of regression. Slope and Intercept can be used to define the linear relationship between two variables: y=ax+b.
17. Simple Linear Regression – a linear regression that has a single independent variable.

### Linear Regression Class Definition
* A scikit-learn linear regression script begins by importing the LinearRegression class:

from sklearn.linear_model import LinearRegression
sklearn.linear_model.LinearRegression()

* Although the class is not visible in the script, it contains default parameters that do the heavy lifting for simple least squares linear regression:

sklearn.linear_model.LinearRegression(fit_intercept=True, normalize=False, copy_X=True)

* Parameters: 

fit_interceptbool, default=True

* Calculate the intercept for the model. If set to False, no intercept will be used in the calculation.

normalizebool, default=False
Converts an input value to a boolean. 

copy_Xbool, default=True
Copies the X value. If True, X will be copied; else it may be overwritten.

* How to Create a Linear Regression Model
In this example, a linear regression model is created based on data in a numpy array. The coefficients are formulated and then printed in the console:

1. Import the packages and classes needed in this example:
import numpy as np
from sklearn.linear_model import LinearRegression

2. Create a numpy array of data:
x = np.array([6, 16, 26, 36, 46, 56]).reshape((-1, 1))
y = np.array([4, 23, 10, 12, 22, 35])

3. Create an instance of a linear regression model and fit it to the data with the fit() function:
model = LinearRegression().fit(x, y) 

4. The following section will get results by interpreting the created instance: 

5. Obtain the coefficient of determination by calling the model with the score() function, then print the coefficient:
r_sq = model.score(x, y)
print('coefficient of determination:', r_sq)

6. Print the Intercept:
print('intercept:', model.intercept_)

7. Print the Slope:
print('slope:', model.coef_) 

8. Predict a Response and print it:
y_pred = model.predict(x)
print('Predicted response:', y_pred, sep='\n')
Watch how to create a Linear Regression and then print the Coefficients

* How to Create a Linear Regression and Display it
In this example, random data is displayed in a plot. A linear regression model is then created against the data, and an estimated regression line is finally displayed.

1.  Import the packages and classes needed for this example:
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

2. Create random data with numpy, and plot it with matplotlib:
rnstate = np.random.RandomState(1)
x = 10 * rnstate.rand(50)
y = 2 * x - 5 + rnstate.randn(50)
plt.scatter(x, y);
plt.show()

3. Create a linear regression model based the positioning of the data and Intercept, and predict a Best Fit:
model = LinearRegression(fit_intercept=True)
model.fit(x[:, np.newaxis], y)
xfit = np.linspace(0, 10, 1000)
yfit = model.predict(xfit[:, np.newaxis])

4. Plot the estimated linear regression line with matplotlib:
plt.scatter(x, y)
plt.plot(xfit, yfit);
plt.show()

### Regression vs Classification 
The main difference between regression and classification is that the output variable in regression is continuous, while the output for classification is discrete. Regression predicts quantity; classification predicts labels. 

## Reading Questions
1. Can you explain the basic concept of linear regression and its purpose in the context of machine learning and data analysis?

Linear regression is a statistical modeling technique used to understand and analyze the relationship between a dependent variable and one or more independent variables. It assumes a linear relationship between the independent variables and the dependent variable, represented by a straight line in a scatter plot. The purpose of linear regression in the context of machine learning and data analysis is to predict or estimate the value of the dependent variable based on the values of the independent variables. It is commonly used for tasks such as prediction, forecasting, and understanding the impact of variables on an outcome.

2. Describe the process of implementing a linear regression model using Python’s Scikit Learn library, including the necessary steps and functions.

Implementing a linear regression model using Python's Scikit Learn library involves several steps:
Step 1: Import the necessary libraries:
Step 2: Prepare the data:Load or generate the dataset.
Step 3: Split the dataset into train and test sets:
Step 4: Create a linear regression model and fit it to the training data:
Step 5: Predict the target variable for the test data:
Step 6: Evaluate the model

3. What is the purpose of splitting the dataset into train and test sets, and how does this contribute to the evaluation of a machine learning model’s performance?

The purpose of splitting the dataset into train and test sets is to evaluate the performance and generalization ability of a machine learning model. By using separate datasets for training and testing, we can simulate the model's performance on unseen data. 

## Things I want to know more about
linear regression and Scikit Learn library
