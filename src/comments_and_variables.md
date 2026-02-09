# Introduction to Python

Python is an easy language to learn and use due to its simplified syntax and natural language flow.
It has all the capabilities for the type of software development thats driving the world these days, such as machine learning, robotics, AI, and data science.

## Code/Coding

The term "code" refers to anything written in a programming language to provide instruction to a computer.
The term "coding" is used to describe the act of writing code.
A code editor is an app that lets you type code, similarly like typing an essay on word.
Just like how there are many brands of toothpaste and other products, there are many brands of code editors.
There isn't a right or wrong or a best or worst one.
For our class, we will use [replit.com](https://replit.com), [codewith.mu](https://codewith.mu/), or VS Code to code in Python.
Replit will work in your browser, so chromebooks will be able to use it.
codewith.mu can be installed on school or personal computers.
VS Code is used in industry and can be installed on your personal device, but not the school computers.

Do NOT leave code on Replit.
It is public for everyone, so if someone finds your code and submits it as their own, it is considered plagiarism and everyone involved will receive a 0, and calls will be made to your parents.

## Our First Python Program

```python
print("Hello World")
```

[Practice #1](https://codecheck.it/files/21082917085wnxm0e98w9yknpp52yithung)

## Comments

A comment is text in the program that does nothing.
Comments are used as notes about what the code is doing or why something was done.
Professionals use comments to explain their code to team members.
They are useful as if you review your code at a later time, you can refer to your comments as a reminder on what the code is doing and why you did something the way you did.
Comments can be a new line or at the end of a line, and there is no limit to the amount of comments used or their length.

In Python, and most other languages, there are two types of comments: single-line and multi-line.
As their name implies, single-line comments only exist on one line, and multi-line comments may span multiple lines.
To create a single-line comment, you place a hashtag/number sign/pound symbol (`#`) before your comment.
For multi-line comments, you surround the comment with either triple double-quotes or single-quotes (`"""` or `'''`)

```python
# this is a single line comment

print("There is a comment at the end of this line!") # Hello there

'''
this is a multi-line comment

it can be used for easily putting lots of text, notes,
or documentation within your code
'''
```

Other languages often use `//` for single-line comments and `/* comment here */` for multi-line comments.

## Python Syntax

Many programming languages focus on things that the computer does and how it does them rather than on the way humans think and work.
This makes most languages hard to learn for most people.
The one feature that really makes python different from other languages is that it uses colons alongside indentations and whitespace (tabs and spaces) rather than parantheses and curly braces to indicate blocks of code.
Python also doesn't require semi-colons at the end of lines.
Because python doesn't use special characters to indicate the beginning or end of a code block, indentations are required and have a considerable effect on how the code runs.
As a result of using indentation to create code blocks, it is easier to read chunks of code and see whats going on.
Indentation refers to the spaces at the beginning of a code line.

### Why Syntax Matters

The definition of syntax is "the arrangement of words and phrases to create well-formed sentences in a language."
In programming languages, there are no sentences, but they do have words in the sense that you need space between each word (just as you do when typing regular text) and the order of those words is important.
The order of the words contribute to the meaning.
Proper syntax in programming languages is just as important as human languages.
When you make a mistake writing or speaking, others will typically notice.
However, computers speak in 1's and 0's so they cannot guess the actual meaning of your words.

### Example of Python Syntax

```python
if (...): # colon denoting a code block
    print("...") # inside the if-statement. This line only exists within this block
print("...") # no semi-colons at the end of lines
```

### Summary

- new line means the command is completed, no need for semi-colon
- Python relies on indentation and whitespace, there no need parantheses { }
- Python is more human readable than other languages

## Python Variables

Variables are a big part of all computer programming languages.
A variable is simply a placeholder for information.
This information may change at any time or stay the same.
A variable is represented by a variable name.
What you name your variable should briefly relate to the information it will hold.
Variables are created when you assign a value to it.
Python does not require any other keywords to define a variable.
Python variables dont need to be declare with a type, and variables can change types after they have been set.
This is called dynamic typing, and not all programming languages have it.
Many are statically typed, which means variables are created with a specific type and cannot have that type changed after initialization.

### Examples

```python
y # incorrect as y does not have a value. Python doesn't know it is a variable.

print(y)
```

```python
name = "Marie" # this variable is given a value with the syntax "variable_name = value"

print("Hello", name)
```

```python
x = 4 # variable x would be considered an integer (number) based on its value of 4

print(x)
```

In order to declare a variable in statically typed languages such as C, we do the following:

```c
// DataType VariableName = Value`

int x = 4;
```

In the previous Python example, x originally had an integer value of 4, now it is a string that holds a value of "Zayaan."

```python
x = "Zayaan"

print(x)
```

Python variables are case-sensitive.

```python
age = 10
Age = 11
print(age, Age)
```

These are two different variables; they are not the same.

## Python Variable Rules

- Variable name must start with a letter or an underscore character
- Variable names CANNOT start with a number
- Variable names can only be alpha-numeric characters and underscores ( A - z, 0 - 9, and _ )
- Variable names are case-sensitive

## Naming Style Conventions

There are many different conventions for the way you name variables and other things within programing languages, and they may differ between languages.

- camelCase: each word, except the first, starts with a capital letter. There are no separator characters between words.
- PascalCase: same as camel case, except the first word also starts with a capital letter.
- snake_case: each word is separated by an underscore character. The words may start with a capital letter, but if that is the case all words in the name should start with capital letters as well.

Snake case is the recommended one to use in Python.

[Practice #2](https://codecheck.it/files/2108291728eesbucomc3an96g3dcalgincj)
