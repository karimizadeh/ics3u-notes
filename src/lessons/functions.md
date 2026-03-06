# Functions

Functions provide a way to compartmentalize your code into smaller tasks that can be called from multiple places in your program.
Function definitions create code blocks, so all indented lines below the function definition line are part of that function.
The first un-indented line is outside the function and will not be executed when the function is called.
A function only runs when it is called.
Functions should be re-usable code, written once and called as many times as needed.
You can pass data into functions, which are called parameters.
A function can also return data as a result.
Once a function finishes running, execution returns back to where the function was called.

## Creating A Function

In Python, functions are defined using the `def` keyword.

```python
def my_function(): # defining the function
    print("Hello from inside my_function()")

print("hello I'm outside my_function()") # first un-indented line

my_function() # calling the function
```

## Nested Functions

There should be no nested function definitions within a function.
All function definitions should be stand-alone.
However, you can call other already-defined functions within other function definitions.

```python
def function_one():
    print("no")

    def function_two():
        print("absolutely not")
```

The above will work, but it is bad practice.
Marks will be taken off if this is in any of your submissions.

```python
def function_one():
    print("yes")

def function_two():
    function_one()
    print("absolutely yes")
```

## Function Arguments/Parameters

The terms parameter and argument can be used to define the same thing: information that is passed into a function.
Parameters are the variables listed inside the parentheses in a function definition.
An argument is the value that is passed to a function when called.
Information can be passed into functions as arguments.
Arguments are specified after the function name, inside the parentheses.
You can add as many parameters as you want, just separate them with a comma.

```python
def my_function(name): # the variable inside is a parameter
    print("Hi " + name)

my_function("Marie") # the strings inside function calls are arguments
my_function("Xavier")
my_function("Adam")
```

Parameters are local only to that function, meaning it only exists inside the function.
It is recommended to name your parameters something different from a variable outside the function.
If you have a variable named `x` outside the function and another variable named `x` inside the function, any changes made to `x` inside the function won't affect the outer `x` variable.
This is called local scope.
Local scope means that the scope of the variables existance and influence stays inside the function and does not extend further.
Variables created and modified inside a function literally cease to exist the moment the function stops running.
Variables defined outside the function are unaffected by the going-ons inside the function.

## Number of Arguments

A function must be called with the correct number of arguments.
If your function expects 2 arguments, you have to call the function with 2 arguments, not more, and not less.
If you try to call the function with more or less arguments you will get an error.

## Keyword Arguments

You can send arguments with the `key = value syntax`
Ordering does not matter in this case.

```python
def my_function(child3, child2, child1):
    print("the youngest child is " + child3)

my_function(child1 = "Nikhil", child2 = "Rand", child3 = "Maya")
```

## Default Parameter Value

Parameters can be given default values.
If we call a function without an argument for a parameter, it will use the default value if one is provided instead of creating an error.

```python
def my_function(country = "Canada"):
    print("I am from" + country)

my_function("Sweden")
my_function("Brazil")
my_function("USA")
my_function() # will print off using the default value since one was not provided
```

## Return Values

Functions can return values using the `return` keyword.
The returned value can be used outside the function, and is placed right where the function was called.
The `return` keyword will stop the function's execution, so be careful where it is used.

```python
def my_function(x):
    return 5 * x

print(my_function(3)) # will print 15 since my_function returns the multiplication operation's result
print(my_function(7))
print(my_function(10))
```

## Recursion - Advanced

Recusion is a common mathematical and programming concept.
It means that a function calls itself.
This has the benefit of allowing you to loop through results over and over to reach a final result.
Developers should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates or uses too much memory/power.

```python
def tri_recursion(k):
    if k > 0:
        result = k + tri_recursion(k - 1)
        print(result)
    else:
        result = 0
    return result

tri_recursion(6)
```
