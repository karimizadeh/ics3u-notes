# Input

The input function is a way for users to interact with a program at runtime.
A string can be placed inside the parentheses which will be printed before the program takes input.
You should store the input in a variable so you can refer back to it later as needed.
The response from the user is returned as a string.
If the user enters a number, it'll still be a string, as proven when you use type().
If you want to do arithmetic with an input from the user, you must cast it into a number (typically int).

### Example 1

```python
price = input("What is the price? ")
print(price)
```

### Example 2

```python
x = input("Enter a number ")
y = int(input("Enter another number "))
print(x)
print(y)
```

### Type

```python
print(type(x)) # string
print(type(y)) # int
```

[Practice #1](https://codecheck.it/files/21090422277xnacr7mu90si43xnsgp5nf1j)

## Floor Division (Integer division)

The floor division operator was briefly mentioned last lesson, but it is most useful for returning the answer of a division operation while ignoring the remainder.

```python
result = int(x) // y # have to cast x to int because input() returns a str
print(type(result)) # int
print(x, "divided by", y, "gives us", result)
```

## Modulo

Also mentioned last lesson, this operator is essentially the inverse of the floor division operator. It returns only the remainder of a division operator, ignoring the quotient.

```python
result1 = int(x) % y
print(x, "divide by", y, "gives us", result, "with a remainder of", result1)
```

## Math Functions

| Function | Description |
|-|-|
| `max(x, y, z, ...)` | Returns the largest provided numeric argument |
| `min(x, y, z, ...)` | Returns the smallest provided numeric argument |
| `round(x, y)` | Returns the number x rounded to y number of decimal places |

[Practice #2](https://codecheck.it/files/2109070120daokxx12s4ke4dr6gcbqjzjwm)

## Additional Math Functions

In addition to the built-in functions above, there are other functions we can use when we import them from the math module.
To use those additional math functions in our program, add the following line to the TOP of your program: `import math`.
| Function | Description |
|-|-|
| `math.ceil(x)` | Rounds x up to the nearest integer |
| `math.ceil(x)` | Rounds x down to the nearest integer |
| `math.pow(x, y)` | Raises x to the power of y. This is the same as the `**` operator |
| `math.pi` | Returns the mathematical constant pi (3.14159265...) |

## Formatting Numbers

You can format numbers within a string using Format strings or f-strings.
To create an f-string, all you need to do is place a lowercase f or uppercase F right before a string.

### Example

```python
username = "Marie"
print(f"Hello {username}")
```

The f before the first quotation mark tells python that what follows is a format string.
Inside the quotation marks, the text, called the literal, is displayed literally (exactly as typed in the f-string).
Anything in curly braces is an expression in the f-string, a placeholder or template for what will appear when the code executes.
Inside the curly braces, you can have any python expression (a formula to perform some calculation, a variable name, or a combination of the two).

### Example

```python
unit_price = 49.99
quantity = 30
print(f"Subtotal: ${quantity * unit_price}") # Subtotal: 1499.7
```

Numbers can be further formatted in f-strings.
If we want to show the price to two decimal places and a comma in thousands places we can modify the above to the following:

```python
unit_price = 49.99
quantity = 30
print(f"Subtotal: ${quantity * unit_price:,.2f}") # Subtotal: 1,499.70
```

The beginning of the formatting for the expression begins with the colon right up against the end of the expression within the curly brace.
To show a comma in the thousands place, we put a comma right after the colon.
To get the price to show two decimal places, we add `.2f`.
`.2f` means "two decimal places, fixed" never any more or less than two decimal places.

### Formatting percentages

Decimals can be formatted as percentages.

```python
sales_tax_rate = 0.065
print(f"Sales Tax Rate: {sales_tax_rate:.2%}") # Sales Tax Rate: 6.50%
```

The `%` after the colon formats the decimal number as a percentage, and the `.2` locks the percentage to 2 decimals.

## Escape Characters

An escape character is a character in a sring with a backslash before it.
Certain escape characters have special meanings, but many just tell python the character is a literal and to treat it as pure text.

Commonly used escape characters include:
| Escape character | Usage |
|-|-|
| `\n` | Represents a newline |
| `\t` | Represents a tab |
| `\'` | A literal '. Allows printing apostrophes and single quotes in strings created with single quotes |
| `\"` | A literal ". Allows printing double quotes in strings created with double quotes |
| `\\` | A literal \\. Allows printing backslashes in strings instead of escaping whatever comes next |

### Example

```python
print("Ms.\nMarie says \"You will get 90\\100\"\tI'm hoping that she\'s right!")

'''
Ms.
Marie says "You will get 90\100"	I'm hoping that she's right!
'''
```

[Practice #3](https://codecheck.it/files/21090421552ya8ho37hoozhz8mrgewpkkt5)

[Practice #4](https://codecheck.it/files/21082917309kepalrlooxz5vnpqispzwh0g)

[Practice #5](https://codecheck.it/files/2109042157798sqfwcuqeq9r8dpu74lodh2)

## Multiline format strings

If you want to have multiline output in a single print statement, you can add line breaks to your format string in two ways:

1. Use `\n`: you can use a single-line format string with `\n` any place you want a line break within the literal part of the string.
1. Use triple quotation marks (single or double). Direct newlines within the triple quotes will create newlines in the string.

### Examples

```python
output = "hello \\n my name is Marie"
print(output)
```

```python
output = f"hello\\n my name is Marie"
print(output)
```

```python
output = """
hello
my
name
is
Marie"""
print(output)
```

```python
output = f"""
hello
my
name
is
Marie"""
print(output)
```

## Formatting width and alignment

You can control the width of printed strings and the alignment of the content within that width.
To do this, we put a colon in our f-string with < (for left aligned), ^ (for centered), or > (for right aligned).
Following the arrows, we can add a number that will indicate how many characters wide we want the content to be aligned.

### Example

```python
unit_price = 49.99
quantity = 32
sales_tax_rate = 0.065
subtotal = quantity * unit_price
sales_tax = sales_tax_rate * subtotal
total = subtotal + sales_tax
output = f"""
Sales Tax Rate: {sales_tax_rate:,.2%}
Subtotal: ${subtotal:>9,.2f}
Sales Tax: ${sales_tax:>9,.2f}
Total: ${total:>9,.2f}
"""

print(output)
```

The above will output

```

Sales Tax Rate: 6.50%
Subtotal: $ 1,599.68
Sales Tax: $   103.98
Total: $ 1,703.66

```
