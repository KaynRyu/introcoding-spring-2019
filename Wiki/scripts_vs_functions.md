# Scripts vs Functions

Scripts and function might look similar, but they are conceptually different. A script is a set of instructions in the form of code that may accomplish one specific task or multiple tasks. A script is usually a collection of functions. A function is a well-polished piece of code that we intend to re-use. A function does something specific and constitutes the processing machinery of functional languages. In languages such as Matlab, Python, R, and Julia the output of one function often becomes the input of another function, each function constituting a step of the ladder, where the ladder represents the problem to be solved.

Functions many times emerge as a portion of a  scripts.

## Script

```python
    # Circle area and circumference from user-specified diameter
    # Script that calculates the area and circumference of a circle with a specified diameter D.

    D = 5                       # Diameter of the circle in centimeters
    r = D/2;                    # Calculate radius 
    area = pi * r^2;            # Calculate area of circle
    circumference = pi * D;     # Calculate perimeter of the circle
```

## Function

```python
    def circlefn (D):
        #CIRCLE Area and circumference of a circle given diameter D.

        r = D/2;                  # Calculate radius
        area = pi - r^2;          # Calculate area of the circle
        circumference = pi * D;   # Calculate perimeter of the circle

        return circumference
```

More resources:

+ <https://www.mathworks.com/help/matlab/matlab_prog/scripts-and-functions.html>