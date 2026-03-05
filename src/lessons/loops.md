# Loops

Decision-making is a big part of writing all kinds of programs.
But, sometimes you need to count or perform a task over and over.
For those situations, we use a loop, which enables you to repeat a line of code, or several lines of code, as many times as you like.
In Python, there are two primitive loop commands: `while` loops and `for` loops.

## While Loops

While loops will execute a block of code as long as its condition is `True`.
It will first evaluate its condition, and if it returns `True`, the while loop will then execute its code block.
Once the code block is done, the `while` loop will then re-evaluate the condition again, and if it is `True`, it will repeat the code block again.
This will go on indefinitely until the condition evaluates to `False`.

### Example

```python
i = 1

while i < 6: # if True
    print(i) # will print out current value of i
    i += 1 # increments i by 1

print("The while loop is done")
```

If you don't increment `i`, the loop will continue forever.
`while` loop conditions require the relevant variables to be ready before the loop.
In this example, we need to define `i` prior to the loop.
In `while` loops, you need to make sure that the condition that makes the loop stop happens eventually.
Otherwise, the loop will keep running indefinitely.

## The `break` Statement

The `break` keyword allows you to stop a loop before the condition proves `False`.
When you use `break` in a while loop, you force execution to continue with the first line of code under and outside the loop.
This "breaks" the loop, but continues executing the rest of the program after the loop.
With the `break` statement, we can stop the loop even if the `while` condition is `True`

### Example

```python
i = 1

while i < 6: # if true
    if i == 3:
        break #when i is equal to 3, it will exit the loop
    print(i) # will print out current value of i
    i += 1 # increments i by 1

print("The while loop is done")
```

# The `continue` Statement

The `continue` keyword stops the current loop iteration and continue with the next.
`continue` can be used similarly to a `break` statement, except instead of breaking out of the entire loop, it will break out of the current code block.

### Example

The `continue` condition in this example causes the loop to continue indefinitely.
The program will not tell you this, but if it runs, it will print 1, 2, and then repeatedly print "3" over and over.

```python
i = 1

while i < 6: # if true
    if i == 3:
        continue # when i is equal to 3, it will stop and continue with the next
    print(i) # will print out current value of i
    i += 1 # increments i by 1
print("The while loop is done")
```

## The `else` Statement

The `else` statement declares a code block which will run when the loop condition is no longer `True`.
The `else` code block in a loop will not run if the loop is exited with a `break` statement.

### Example

```python
i = 1

while i < 6: # if true
    print(i) # will print out current value of i
    if i == 3:
        continue #when i is equal to 3, it will stop and continue with the next iteration
    i += 1 # increments i by 1
else:
    print("i is no longer less than 6")

print("The while loop is done")
```

## For Loops

`for` loops are used for iterating over a sequence (think of a list, tuple, dictionary, set, or a string - most of which we haven't learned yet).
With the `for` loop, we can execute a set of statements once for each item in a list, tuple, set.
`for` loops can also run for a fixed number of loops, as defined by a `range`.

### Example 1

```python
for x in range(7):
    print(x)

print("All done")
```

`range(x)` will create a sequence from 0 up to but not including `x`.
The above example will print 0-6, for example.

### Example 2

```python
for x in range(1, 10):
    print(x)
print("All done")
```

With two parameters, `range(x, y)` will create a sequence from `x` up to but not including `y`.
The above example will print 1-9, for example.

### Example 3 - Looping Through a String

```python
for x in "banana":
    print(x)
print("Done")

# The string doesn't have to be a literal string. It can be the name of any variable that contains a string
fruit = "banana"
for x in fruit:
    print(x)
print("Done")
```

A string is just a collection of letters, so looping over a string will operate on individual letters.

## `break`, `continue`, and `else`

The `break`, `continue`, and `else` keywords can all be used the same way in a `for` loop as they are used in a `while` loop.

### Examples

```python
for x in range(1, 100):
    if x == 42:
        print("is the meaning of life")
        break
    print(x)
print("The for loop is done")
```

```python
for x in range(1, 100):
    if x == 42:
        print("is the meaning of life")
        continue
    print(x)
print("The for loop is done")
```

```python
for x in range(6):
    print(x)
else:
    print("finally finished")
print("The for loop is done")
```

## Nested Loops

A nested loop is a loop inside another loop.
The entire inner loop will be executed one time for each iteration of the outer loop.
This can be done with any combination of differing or matching loop types, such as
`while` loops in a `while` loop, `while` loops in a `for` loop, `for` loops in a `while` loop, and `for` loops in a `for` loop

### Example

```python
for outer in range(20):
    for inner in range(1, 5):
        print(outer, inner)
    print("the inner loop is done")
print("The outer loop is done")
```

The inner loop iterates 4 times, and the outer loop iterates 20 times, resulting in 80 overall iterations in the inner loop.
