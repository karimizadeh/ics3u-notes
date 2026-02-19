# Python Data Types

In python, there are three main categories of data types we will work with. Thos are numbers, text (strings), and booleans.
Numbers are amounts and strings consists of letters and words.
The main difference is that computers can do arithmetic with numbers but not with letters or words.

Text type: str (string)
Numeric types: int (integer), float (think of float as a decimal)
Boolean type: bool (true or false)

## Examples

```python
a = 1
b = "hi"
c = 4.4
d = True

# To check what type a variable is, we use type()
print(type(x))
```

### Practice

Print the type and output of variables, a, b, c, and d.

## Python Text (Strings)

Strings are sort of the opposite of numbers.
Numbers represent quantities.
Strings are for almost everything else, such as names, addresses, and all other kinds of text or information.
It is called a string as it is a string of characters (letters, spaces, punctuations).
To a computer, if a piece of information is not something on which it can do arithmetic, it's just a string of characters.
Strings MUST be enclosed in quotation marks (single-quotes or double-quotes).
You cannot interchange quotations marks. Must be one or the other. If you start a string with a single quote, you must end with a single quote.
Numbers inside a string aren't the same as the number data type and you cannot perform arithmetic with them.

```python
# x and y are completely different
x = 4 != y = "4"
```

### Example

```python
# In Python, you can assign a different DataType to a variable by changing the value assigned to it.
var = 5

# Earlier, var was an integer with a value of 5. Now it is a string.
var = "Hi, my name is 'Marie'."
```

## Python Numbers

Numbers in python either start with a number digit (0-9), a dot (which represents a decimal point), or a hypen (-) used as a negative sign for negative numbers.
A number can contain only one decimal point, CANNOT contain letters, spaces, $ (currency signs), or anything that isn't part of a regular number.
In the computer world, the data type considered numbers are numbers you can add, subtract, multiple, and divide.
Python also differentiates between whole numbers (integers) and numbers that contain a decimal point (floats).

Integers are a whole number, positive or negative.
Any valid number that doesn't contain a decimal point are considered integers.
Any valid number that does contain a decimal point is considered a float.

## Boolean Values

This data type isn't exactly a number or a string.
It can be one of two values: True or False.
Booleans are not strings as you don't need quotations, and they aren't treated the same as numbers either.
In python, you often need to know if an expression is True or False.
You can evaluate any expression in Python, and get one of two answers: True or False.

```python
print(10 > 9) # True

# When you compare two values, the expression is evaluated and Python returns the boolean answers
print(10 == 9) # False
print(10 < 9) # False
```

## Casting Data Types in Python

Some values may be valid as multiple different data types.
There are scenarios where you may need to convert a variable from one type into another without changing its value.
Casting allows this, as long as the value being casted can be represented properly in the target data type.

When casting a float into an int, the value will not be rounded and the decimal portion will be discarded.

```python
j = 1 # original datatype is an integer
k = 2.8 # original datatype is a float

w = float(j) # casted value is now: 1.0
q = int(k) # casted value is now: 2
l = str(k) # casted value is now: '2.8'

print(w, q, l)
print(type(w)) # float
print(type(q)) # int
print(type(l)) # str
```

## Python Operators

Above, we worked with and converted between different data types in python.
We can also use computers to 'operate' on that information.
In order to do any necessary math, comparisons, or search, you need to operate on that information.

### Assignment Operator

`=` assigns values to variables.

```python
t = 8
```

### Arithmetic Operators

These operators perform mathematical operations on numbers.

| Operator | Name | Description | Example |
-|-|-|-
| + | Addition | Add two numbers together | `x + y` |
| - | Subtraction | Subtract one number from another | `x - y` |
| * | Multiplication | Multiply two numbers together | `x * y` |
| / | Division | Divide one number by another | `x / y` |
| % | Modulus | Divide on number by another and return the remainder | `x % y` |
| \*\* | Exponentiation | Raise a number to the power of another | `x ** y` |
| // | Floor Division | Divide a number by another number, but the result is rounded down to the nearest integer | `x // y` |

```python
print(1 + 3) # 4
print(2 * 3) # 6
print(6 / 2) # 3
```

### Comparison Operators

These operators compare values.

| Operator | Name | Description | Example |
-|-|-|-
| == | Equivalence | Checks if two values are equal | `x == y` |
| != | Not Equivalent | Checks if two values are not equal | `x != y` |
| > | Greater Than | Checks if the first value is larger than the second | `x > y` |
| < | Less Than | Checks if the first value is less than the second | `x < y` |
| >= | Greater Than or Equal To | The equivalence and greater than operators combined | `x >= y` |
| \<= | Less Than or Equal To | The equivalence and less than operators combined | `x <= y` |

```python
print(10 != 8) # True
print(12 >= 3) # True
print(5 < 5) # False
```

### Practice

[Practice #1](https://codecheck.it/files/21082917309kepalrlooxz5vnpqispzwh0g)

[Practice #2](https://codecheck.it/files/210829181323aexx8netd7fcfia4pm8aq3k)

## Errors

### Syntax Errors/Compile-time Errors

As mentioned last lesson, syntax is very important in programming languages.
In statically typed or compiled languages such as C and Java, your code cannot be run before being compiled.
Attempting to compile your code with a mistake in the syntax will result in a compile-time error, preventing your code from being run.
In python and other dynamically typed languages, the code is run line by line by an interpreter.
When it encounters something unexpected or out of place from python syntax rules, the program will crash and return an error.

```python
areaOfRectangle = 15 x 17
print("area is", areaOfRectangle)
```

When run, the above will result in the following output:

```
  File "main.py", line 1
    areaOfRectangle = 15 x 17
                         ^
SyntaxError: invalid syntax
```

Python will provide information about an error when they occur, such as what line the error occurred on,
what character(s) caused the error (the `^` underneath a word or symbol will indicate this), and the error type.
In this case, a SyntaxError occurred on line 1 because of the character "x".
"x" is not the multiplication operator in python, so this is a clear syntax error as "x" has no meaning in this context and is not expected by python.

### Logic Error/Run-time Error

Another problem that may occur in programs is a logic error/bug, sometimes called a runtime error.
While certain logic errors may cause a program to crash, they often just result in unexpected outputs.
As the name implies, logic bugs are caused when the logic of the program does not produce the expected outcome,
as opposed to a syntax error which is caused by the program being unable to properly run the code.

```python
areaOfRectangle = 15 / 17
print("area is", areaOfRectangle)
```

When run, the above will result in the following output:

```
area is 0.8823529411764706
```

While the program successfully ran, the output was not the area of a rectangle with the dimensions 15 and 17.
This is not a bug in the syntax as the program runs perfectly fine, but an error in the logic of the program.
The area of a rectangle is calculated by multiplying its two dimensions together, but the program divides them instead, resulting in the unexpected output.
