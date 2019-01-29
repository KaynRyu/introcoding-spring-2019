---
layout: default
title: Hello world
parent: Getting started
nav_order: 7
---

# Getting started

Here are some of the most basic Python commands so that you can create your very first notebook.

**Few comments about Jupyter notebooks**
- Code lives in cells, which help organizing your code. The main advantage of cells is that you can run (i.e. execute code) cells individually to ensure that the code is working properly before you move forward.
- To run code in a cell press: ctrl + enter key. The result will appear right below the code.
- To run code in a cell and move onto the next cell when done press: ctrl + shift + enter keys


```python
# The most iconic line of code when learning how to program
print("Hello World")
```

    Hello World



```python
# Comments are represented by the pound symbol "#". 
# So these few lines are comments and will be ignored by the Python interpreter.
# Comments are useful to document your code
```


```python
print("This sentence will print") # This one will not
```

    This sentence will print



```python
# Print multiple items: strings and numbers
print("I have", 78, "boxes to move")
print("Remainder is ", 10 % 3) # % is the modulus operator
```

    I have 78 boxes to move
    Remainder is  1



```python
# Define variables using equality
a = 134
print(a)

# Define multiple variables at once
mu, sigma = 0, 0.2

# See variable output
mu
```

    134





    0




```python
# variables can be accessed from a different cell (variables are not actually attach to any cell)
# As long as variables are in memory you can call and use them
print(a)
```

    134



```python
# Re-define a variable
a = 2
print(a)

# Now a changed its value
```

    2



```python
# Student question: Can we define 1 = a? or 1 = "a"
1 = "a"

# The answer is no. Variable names must start with a letter or an underscore
```


      File "<ipython-input-12-e25cb9124501>", line 2
        1 = "a"
               ^
    SyntaxError: can't assign to literal




```python
# Python as a calculator
cars = 50
sits_per_car = 4
carpool_capacity = cars * sits_per_car
passengers = 185
sits_available = carpool_capacity - passengers

# Multiple ways of printing the output
print("There are", cars, "cars and remain only", sits_available , "sits available.")
print("There are " + str(cars) + " cars and remain only " + str(sits_available) + " sits available.")

# Previous line requires manual insertion of spaces

print("There are %f cars and remain only %f sits available." % (cars, sits_available))
print("There are %d cars and remain only %d sits available." % (cars, sits_available))

# Modern and perhaps better option. Previous choices may be deprecated in future Python versions
print("There are {} cars and remain only {} sits available.".format(cars, sits_available))

# %f and %d are defined within the string
# Note that the percent symbol could be used to calcualte remainder, but also to indicate variables
```

    There are 50 cars and remain only 15 sits available.
    There are 50 cars and remain only 15 sits available.
    There are 50.000000 cars and remain only 15.000000 sits available.
    There are 50 cars and remain only 15 sits available.
    There are 50 cars and remain only 15 sits available.



```python
# Body height conversion
height_inches = 72 # inches
height_cm = height_inches * 2.54
print("My height is",height_cm,"cm")
print("My height is",round(height_cm,1),"cm")
```

    My height is 182.88 cm
    My height is 182.9 cm



```python
# Student question: Why do we need to separate inputs by commas?
# Answer: It allows you to detach strings from variables and allows you to pass variables
# already defined in memory.
```


```python
# Data types
print(type("hello world"))
print(type(4.0))
print(type(4))
```


```python
# The last part of this notebook consists of simple arithmetic operations
# In python we can store information in the form of variables.
# We use variables so that we can use useful information in later steps. For instance:

print(3 + 4)
print(3 - 4)
print(3 * 4)
print(3 / 4)
print(3**4)
print(10 % 4)

# This case is trivial and we could have easily wrote c = 1 + 3, but often times we deal with
# multiple values (arrays) or extensive datasets, in which case we use variables.
```

    7
    -1
    12
    0.75
    81
    2



```python
# PROBLEM

# Given two positive integers a and b
# Return the integer corresponding to the square of the hypotenuse of the right triangle 
# whose legs have lengths a and b.

# For instance, if a=3 and b=5, the result should be 34

# Hint: define a and b as two separate variables. A function would be better.
```


```python
# Solution

a = 3
b = 5
result = a**2 + b**2
print(result)
```
