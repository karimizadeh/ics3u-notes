# Python Collections

Sometimes in code you work with one item at a time, such as a person's name or a unit price.
Other times, you work with larger sets of data, such as a list of people's names or a list of products and their prices.
These sets of data are often referred to as lists or arrays in most programming languages.

## Python Collection Types

There are four collection data types in Python:

- List - is a collection which is ordered and changeable. Allows duplicate entries
- Tuple - is a collection which is ordered and UNchangeable. Allows duplicate entries
- Set - is a collection which is unordered and not indexable. No duplicate entries
- Dictionary - is a collection which is unordered and changeable. No duplicate entries

## Lists

The simplest data collection is a list.
A list is any list of data items separated by commas inside square brackets.
You can assign a name to the list like you would a variable.
In a Python List, we can use it to store multiple values, and access them sequentially, by their position (index)

A list is defined by putting comma-separated list of values inside square brackets (`[]`).

### Example

```python
my_list = [] #an empty list.
animals = ['cat', 'dog', 'fish', 'bird'] #a list of strings
numbers = [1, 7, 64, 873] # a list of numbers
```

### Accessing a list

To refer to an element in the list, we will use the list identifier followed by the index inside square brackets.
Indices are integers which start from zero.

### Example

```python
print(animals[0]) # cat
print(numbers[1]) # 7

# We can also count from the end using negative numbers
print(animals[-1]) # will give us the last element, which is bird
print(numbers[-2]) # will give us the second-last element, which is 64
```

Lists are mutable, meaning we can modify elements, add elements, or remove elements from them.
A list will change in size dynamically when we add or remove elements - we don't have to manage this.

### Example

```python
# assign a new value to an existing element
animals[3] = "hamster"

# add a new element to the end of the list
animals.append("Squirrel")

# remove an element by its index
del animals[2]
```

## Tuples (Pronounced "two-pull")

Tuples are similar to lists in many ways, but they are immutable (not changeable).
A tuple is defined by putting a comma-separated list of values inside ROUND brackets (`()`).
Tuples are good for when we want to create a sequence of values that we don't want to modify.

```python
weekdays = ('Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday')
```

## Sets

A set is a collection of unique elements.
If we add multiple copies of the same element to a set, the duplicates will be eliminated, and we will be left with one of each element.
Sets are used as a means to organize data.
The difference between a set and a list is that the items in a set have no specific order.
To create a set, we put comma-separated list of values inside curly brackets (`{}`).

```python
animals = {'cat', 'dog', 'goldfish', 'bird', 'cat'}
print(animals) # should only print cat once because it is a set and the duplicate(s) got eliminated
```

Unlike lists and tuples, sets are not ordered.
When we print a set, the order of the elements will be random.
Items within a set dont get an index number to identify their position and you can't change an item already in the set or the order.
Methods available on lists such as `.sort()` or `.reverse()` don't work.
If we want to process the contents of a set in a particular order, you will have to convert it to a list or tuple first, then sort it.

## Dictionary

Dictionaries are similar to lists except each item is not identified by its position (index) but by a key.
We can use a dictionary to store key-value pairs.
Think of a dictionary being similar to a table, where the first column is the unique key and the second column is the value for that key.

To create a dictionary, we put a comma-separated list of key-value pairs between curly brackets (`{}`), just like a set.
But, we use a colon to separate each key from its value.
We access values in the dictionary in the same way as a list or tuple, but instead of using indices we use the keys instead.
Dictionaries are stored in a variable name that should represent the data being stored.

```python
marbles = { "red": 34, "green": 30, "brown": 31, "yellow": 29 }

student = { "name": "Rand", "age": 15 }
```

Keys of a dictionary don't have to be a string - they can be any immutable type, including numbers and tuples.
The only requirement is that it is unique to each item in the dictionary.
Keys are UNIQUE - if we repeat a key, it will overwrite the old value with the new value.
When we store a value in a dictionary, the key doesn't have to exist - it will be created automatically.

Similar to sets, dictionaries are not ordered - if we print a dictionary, the order will be random.
We can check if a value is in the dictionary using the `in` keyword in conjunction with the `values()` method.

```python
print("Rand" in student.values())
```

## Python Lists Vs Arrays in other languages

Many other languages don't have a built-in type that behaves like a Python list, as those who use those languages use arrays instead.
Arrays are simpler, more low-level data structures that don't have all the functionality of a list.

Major differences are:

- An array has a fixed size. If you need to add or remove elements, you need to make a new array
- Typically, arrays can only contain one data type. If you create an array of numbers, you cannot add strings to it
- In languages which have primitive types, arrays are not objects and won't have any methods

Arrays are less easy to use in many ways but they have advantages.
Because they are so simple and there are so many restrictions on what you can do, the computer can handle them very efficiently.

## Additional List Examples

You can do a lot with lists in Python, so here's a non-exhaustive list of things you can do with them, along with examples:

### Finding the Length of a List

```python
# Use the len() method
fruits = ["apple", "banana", "cherry"]
print(len(fruits))
```

### Slicing

You can "slice" a list so that it returns a subset of its values as another list as opposed to just a single values.
This is done when you specify a range of indexes using slicing syntax when.
The syntax is as follows:

`[start:end]`, where:
start is the index of the first element in your slice
end is the index after the index of the last element in your slice

Omitting either variable will default to the first/last element in the list.
Negative numbers may also be used, behaving exactly like they would during regular indexing.

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
print(fruits[2:5]) # The search will start (and include) at index 2 and end at index 5 (not included)

# If we were to leave out the start value, the range will start at the first item
print(fruits[:5])

# If we were to leave out the end value, the range will go on to the end of the list
print(fruits[2:])

# Can also specify negative indexes if you want to search from the end of the list
print(fruits[-4:-1])
```

### Modifying a Range of Item Values

To change the value of items within a specific range, define a list with the new values.
You can then modify the range of values like you would with just a single index using slicing notation.

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
fruits[1:3] = ["pear", "strawberry"]
print(fruits)
```

If you try to insert more items than you replace, the new items will be inserted where you specified and the remaining items will move accordingly.

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
print(len(fruits))
fruits[1:2] = ["pear", "strawberry"]
print(len(fruits))
print(fruits) # ["apple", "pear", "strawberry", "cherry", ...]
```

### Inserting Items

To insert a new list item, without replacing any of the existing values, we can use the `insert()` method.

```python
fruits = ["banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
fruits.insert(3, "apple")
print(fruits) # [..., "orange", "apple", "mango", ...]
```

### Extending/Combining Lists

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
more_fruits = ["pears", "strawberry", "kiwi", "peach"]
fruits.extend(more_fruits)
print(fruits)
```

The `extend()` method can add any iterable object (lists, tuples, dictionaries, etc.) together.

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
more_fruits = ("pears", "strawberry", "kiwi", "peach")
print(type(fruits), type(more_fruits)) # <class 'list'> <class 'tuple'>

fruits.extend(more_fruits)
print(type(fruits))
print(fruits)
```

### Removing Items

As mentioned before, the `del` keyword can delete specific items in lists.
However, the `del` keyword can also delete entire lists.

```python
del fruits
print(fruits) # would give an error since it is no longer defined.
```

The `remove()` method can be used to remove the specified item if you know what it is.

```python
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
fruits.remove("cherry")
print(fruits) # "cherry" is no longer present in the list
```

The `pop()` method can be used to remove the an item at the specified index.

```python
#If no index is given, the pop() method will remove the last item
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
fruits.pop(2)
print(fruits)
fruits.pop()
print(fruits)
```

### Joining Two Lists

There are a few ways to join/concatenate two or more lists in Python.
The addition operator (`+`) is one such way

```python
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]
list3 = list1 + list2
print(list3)
```

Another way to join two lists is by appending all the items from list2 into list1, one by one.

```python
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]
print(list1)
for x in list2:
list1.append(x)

print(list1)
```

Or you ca the `extend()` method, whose purpose is to specifically add elements from one list to another list.

```python
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]
print(list1)
list1.extend(list2)
print(list1)
```

## Using Python Collections with Loops

```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
    print(x)
```

```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
    for y in fruits:
        print(x, y)
```

```python
# Check if an item exists
# To determine if a specified item is present in a list we use the in keyword
fruits = ["apple", "banana", "cherry", "orange", "mango", "pineapple", "watermelon"]
if "apple" in fruits:
    print("Yes, apple is in the fruits list")

for i in fruits:
    print(i)
```
