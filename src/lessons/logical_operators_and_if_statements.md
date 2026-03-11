# Decisions

## Statements

a statement is an instruction that the Python interpreter can execute.
We have seen assignment statements so far (`x = 4`).
Some other statements we'll see shortly are while statement, for statements, and if statements.
This lesson will be focusing on if-statements

## Expression

An expression is a combination of values, variables, operators, and calls to functions.
Expressions need to be evaluated.
If you were to print an expression, the Python interpreter will evaluate the expression and display the results.

### Evaluation of an Expression

The evaluation of an expression produces a value.
A value all by itself is a simple expression, and so is a variable.
Evaluating a variable gives the value that the variable refers to.

## Comparison Operators

As a refresher from lesson 2, here is a table of comparison operators:

| Operator | Name | Description | Example |
-|-|-|-
| == | Equivalence | Checks if two values are equal | `x == y` |
| != | Not Equivalent | Checks if two values are not equal | `x != y` |
| > | Greater Than | Checks if the first value is larger than the second | `x > y` |
| < | Less Than | Checks if the first value is less than the second | `x < y` |
| >= | Greater Than or Equal To | The equivalence and greater than operators combined | `x >= y` |
| \<= | Less Than or Equal To | The equivalence and less than operators combined | `x <= y` |

These operators will return True or False.
These conditions can be used in several ways, most commonly in if statements and loops.

## If-Statements

The word 'if' is used a lot in all computer programs to make decisions.
An if-statement is written by using the `if` keyword.
If statements create a block, and have the following structure:

```
if condition:
    do this

do this no matter what
```

To do more than one thing when a condition is true, you need to indent each line you want executed if the condition is true.
This is called a "code block."
Code that is not indented below the if will be executed regardless if the condition was True or False.
This is because it isn't dependent on the condition.
If the condition proves False, the instructions inside the code block is ignored.

[Practice #1](https://codecheck.it/files/2109241808b32uwhtkz8unaz1rvh0zh3fpj)

### Example

```python
a = 33
b = 200

# if keyword, followed by an expression to be evaluated
# If evaluated to True, it will run the code in the code block
if b > a:
    print("b is greater than a") # needs to be indented
    print("") # indentation represents a code block
    print("")

# as soon as there is no indentation, the previous code block ends
# any code afterwards isn't a part of the code block
print("")
```

## Else

Sometimes you want a chunk of code to execute if a condition proves True.
Otherwise (else), if it doesn't prove True, you want some other chunk of code to be executed.
The `else` keyword creates a block that catches anything that isn't caught by the preceding if condition.
Any lines of code indented under the `else` are executed only if the condition did not prove True.

### Example

```python
a = 200
b = 33

if b > a:
    print("b is greater than a")
else:
    print("a is greater than b")
```

### Flowchart Example

<p align="center">
    <img src="../assets/if_flowchart_template.png">
</p>

The `if FALSE statement` branch represents the `else` block.

<p align="center">
    <img src="../assets/if_flowchart_example.png">
</p>

The corresponding code would be:

```python
mark = 100

if mark >= 50:
    print("you passed!")
else:
    print("you failed!")
```

## Elif

The `elif` keyword is python's way of saying "if the previous conditions were not true, then try this condition."
When `if...else` is not enough, `elif` can be used, which stands for "else if."
An if statement can include any number of `elif` conditions and doesn't have to have an `else` at the end.

### Examples

```python
a = 33
b = 33

if b > a:
    print("b is greater than a")
elif a == b:
    print("a and b are equal")
```

```python
a = 200
b = 33
if b > a:
    print("b is greater than a")
elif a == b:
    print("a and b are equal")
else:
    print("a is greater than b")
```

### Flowchart Example

<p align="center">
    <img src="../assets/elif_flowchart_template.png">
</p>

Note the lack of an "if all else fails" branch.
This would be covered by an `else` block, but `else` blocks are optional.

<p align="center">
    <img src="../assets/elif_flowchart_example.png">
</p>

[Practice #2](https://codecheck.it/files/21092418121710zkw29od2pejbl3w06pmro)

[Practice #3](https://codecheck.it/files/210924182185pu4g59updjhrky0wtx6v096)

[Practice #4](https://codecheck.it/files/21092619572qtebcjn7k79iazrj51acpzs5)

## Python Logical Operators

Logical operators are used to combine conditional statements.

| Operator | Description | Example |
|-|-|-|
| `and` | return True only if both statements are True | `x < 5 and x < 10` |
| `or` | returns True if either statement is True | `x < 5 or x < 4` |
| `not` | reverse the result (True -> False, False -> True) | `not (x < 5 and x < 10)` |

Below is each operators' truth table. `a` and `b` represent expressions which evaluate to True or False

<p align="center">
 <img src="../assets/logical_operators_truth_table.png">
</p>

### Examples

```python
a = 200
b = 33
c = 500

if a > b and c > a:
    print("both conditions are true")
```

```python
a = 200
b = 33
c = 500

if a > b or c > a:
    print("at least one of the conditions are true")
```

```python
a = 200
b = 33
c = 500

if not(a > b and c > a) == False:
    print("both conditions are false")
elif not(a > b or c > a) == False:
    print("one of the conditions are false")
```

[Practice #5](https://codecheck.it/files/210924183094x8ir1etmeloo9ay6fpp3ua8)

[Practice #6](https://codecheck.it/files/2109241836a4cjz7pstsdpvcwfs9o9f5tt3)

## Nested Ifs

You can have if-statements inside if-statements and other code blocks.

### Example

```python
x = 41
if x > 10:
    print("Above 10")
    if x > 20:
        print("Above 20") # nested block, requires x > 10 and x > 20
    else:
        print("but not above 20")
else:
    print("not above 10")
```
