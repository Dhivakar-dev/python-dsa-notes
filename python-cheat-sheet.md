# Python Cheat Sheet with Explanations

## 1. Basics

### Hello World
```python
print("Hello, World!")  # Prints text to the console
```

### Comments
```python
# This is a single-line comment

"""
This is a
multi-line comment
"""
```

### Variables and Data Types
```python
x = 10           # Integer
y = 3.14         # Float
name = "Alice"   # String
is_valid = True  # Boolean
```

### Multiple Assignment
```python
a, b, c = 1, 2, 3
```

### Type Conversion
```python
int("7")          # Converts string to integer
str(100)          # Converts integer to string
float("5.5")      # Converts string to float
```

## 2. Data Structures

### Lists
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")     # Add to end
fruits.remove("banana")     # Remove value
print(fruits[0])            # Indexing
print(fruits[-1])           # Last item
fruits[1:3]                 # Slicing
```

### Tuples (immutable lists)
```python
coords = (1, 2)
```

### Dictionaries
```python
person = {"name": "Bob", "age": 25}
person["age"] = 26
print(person.get("name"))
for key, value in person.items():
    print(key, value)
```

### Sets
```python
colors = {"red", "green", "blue"}
colors.add("yellow")
colors.remove("red")
```

## 3. Operators

### Arithmetic
```python
x + y    # Addition
x - y    # Subtraction
x * y    # Multiplication
x / y    # Division
x // y   # Floor Division
x % y    # Modulus
x ** y   # Exponentiation
```

### Comparison
```python
x == y   # Equal to
x != y   # Not equal to
x > y    # Greater than
x < y    # Less than
x >= y   # Greater or equal
x <= y   # Less or equal
```

### Logical
```python
and, or, not
```

### Membership
```python
"a" in "cat"          # True
3 not in [1, 2, 3]    # False
```

## 4. Control Flow

### If-Else
```python
if x > 10:
    print("x is large")
elif x == 10:
    print("x is ten")
else:
    print("x is small")
```

### Loops

#### For Loop
```python
for i in range(5):          # 0 to 4
    print(i)

for item in ["a", "b", "c"]:
    print(item)
```

#### While Loop
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

#### Break & Continue
```python
for i in range(10):
    if i == 5:
        break     # Exits loop
    if i % 2 == 0:
        continue  # Skips even numbers
    print(i)
```

## 5. Functions

### Defining Functions
```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
```

### Return Statement
```python
def add(a, b):
    return a + b
```

### Default Arguments
```python
def power(x, y=2):
    return x ** y
```

### Lambda Functions
```python
square = lambda x: x*x
print(square(5))
```

## 6. Classes & Objects

```python
class Dog:
    def __init__(self, name):
        self.name = name
    
    def bark(self):
        print(f"{self.name} says woof!")

my_dog = Dog("Rex")
my_dog.bark()
```

## 7. Exception Handling

```python
try:
    val = int(input("Enter a number: "))
except ValueError:
    print("Not a number!")
else:
    print("You entered:", val)
finally:
    print("Done!")
```

## 8. Modules & Packages

### Importing
```python
import math
from math import sqrt
import my_module as mm
```

### Installing Packages
```bash
pip install requests
```

## 9. Working with Files

```python
# Write to file
with open("file.txt", "w") as f:
    f.write("Hello!")

# Read from file
with open("file.txt", "r") as f:
    content = f.read()
```

## 10. Useful Built-in Functions

```python
len([1, 2, 3])             # Length
sum([1, 2, 3])             # Sum
max([1, 2, 3])             # Maximum
min([1, 2, 3])             # Minimum
sorted([3, 1, 2])          # Sorts list
list(range(5))             # [0, 1, 2, 3, 4]
enumerate(['a','b','c'])   # Returns index & value
zip([1,2], ['a','b'])      # Pairs items
```

## 11. List Comprehensions

```python
squares = [x*x for x in range(10)]
evens = [x for x in range(10) if x%2 == 0]
```

## 12. Useful Standard Libraries

- **os**: Interact with operating system
    ```python
    import os
    os.getcwd()      # Current directory
    os.listdir()     # List files
    ```
- **sys**: System-specific parameters and functions
    ```python
    import sys
    sys.argv
    ```
- **datetime**: Date and time utilities
    ```python
    from datetime import datetime
    now = datetime.now()
    ```
- **random**: Random number generation
    ```python
    import random
    random.randint(1, 10)
    random.choice([1,2,3])
    ```

## 13. Advanced: Decorators

```python
def my_decorator(func):
    def wrapper():
        print("Before")
        func()
        print("After")
    return wrapper

@my_decorator
def say_hi():
    print("Hi!")

say_hi()
```

## 14. Advanced: Generators

```python
def count_up_to(n):
    num = 1
    while num <= n:
        yield num
        num += 1

for i in count_up_to(5):
    print(i)
```

---

**Python is simple, intuitive, and powerful. Use this cheat sheet for quick reference and to improve your coding efficiency!**
