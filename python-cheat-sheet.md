# Python Cheat Sheet

## Basics

```python
# Print Statement
print("Hello, World!")

# Variables
x = 5
name = "Alice"

# Data Types
int_var = 10
float_var = 10.5
str_var = "Hello"
bool_var = True
list_var = [1, 2, 3]
tuple_var = (1, 2, 3)
dict_var = {"a": 1, "b": 2}
set_var = {1, 2, 3}
NoneType = None

# Type Checking
type(x)  # <class 'int'>
isinstance(x, int)  # True

# Comments
# Single line
""" Multi-line
comment """

# Input
user_input = input("Enter something: ")

# Casting
int("5")    # 5
str(5)      # "5"
float("5.2")# 5.2
```

## Operators

```python
# Arithmetic: +, -, *, /, //, %, **
# Comparison: ==, !=, <, >, <=, >=
# Logical: and, or, not
# Assignment: =, +=, -=, *=, /=, //=, %=, **=
# Membership: in, not in
# Identity: is, is not
```

## String Operations

```python
s = "hello"
s.upper()           # 'HELLO'
s.lower()           # 'hello'
s.title()           # 'Hello'
s.strip()           # Remove surrounding whitespace
s.replace("l", "z") # 'hezzo'
s.split(",")        # Split into list
".join(['a','b']) # 'a,b'
len(s)              # 5
s[0]                # 'h'
s[-1]               # 'o'
s[1:4]              # 'ell'
```

## Lists

```python
lst = [1, 2, 3]
lst.append(4)
lst.insert(1, 10)
lst.remove(3)
lst.pop()           # Removes last
lst[0] = 100
lst2 = lst + [5, 6]
lst.sort()
lst.reverse()
lst.index(10)
lst.count(1)
lst.clear()
lst.copy()
```

## Tuples

```python
tup = (1, 2, 3)
tup[0]          # 1
tup.count(2)    # 1
tup.index(3)    # 2
```

## Dictionaries

```python
d = {"a": 1, "b": 2}
d['a']             # 1
d.get('c', 0)      # 0
d['c'] = 3
d.keys()
d.values()
d.items()
d.pop('a')
d.update({"d": 4})
d.clear()
```

## Sets

```python
s = {1, 2, 3}
s.add(4)
s.remove(2)
s.discard(5)    # No error if not present
s.union({5, 6})
s.intersection({2, 3, 4})
s.difference({1})
s.clear()
```

## Control Flow

```python
# If-elif-else
if x > 5:
    print("Big")
elif x == 5:
    print("Equal")
else:
    print("Small")

# For loop
for i in range(5):
    print(i)

for item in lst:
    print(item)

# While loop
i = 0
while i < 5:
    print(i)
    i += 1

# Break, Continue, Pass
for i in range(5):
    if i == 3:
        break
    if i == 2:
        continue
    pass
```

## Functions

```python
def greet(name):
    return f"Hello, {name}"

def add(a, b=5):
    return a + b

def multi_return():
    return 1, 2, 3

def variable_args(*args, **kwargs):
    print(args, kwargs)

# Lambda
add = lambda x, y: x + y
```

## Classes & Objects

```python
class Person:
    def __init__(self, name):
        self.name = name

    def hello(self):
        print(f"Hello, {self.name}")

p = Person("Alice")
p.hello()
```

## Exceptions

```python
try:
    x = 1 / 0
except ZeroDivisionError as e:
    print("Error:", e)
finally:
    print("Done")
```

## Useful Built-in Functions

```python
abs(-5)           # 5
round(5.678, 2)   # 5.68
min([1, 2, 3])    # 1
max([1, 2, 3])    # 3
sum([1, 2, 3])    # 6
sorted([3, 1, 2]) # [1, 2, 3]
enumerate(['a','b']) # [(0, 'a'), (1, 'b')]
zip([1,2],[3,4])  # [(1,3), (2,4)]
map(str, [1,2,3]) # ['1','2','3']
filter(lambda x:x>1, [1,2,3]) # [2,3]
list(map(int, ['1','2']))
```

## File I/O

```python
with open("file.txt", "r") as f:
    content = f.read()

with open("file.txt", "w") as f:
    f.write("Hello!")

with open("file.txt", "a") as f:
    f.write("Append this line")
```

## Modules & Imports

```python
import math
import sys
from math import sqrt
import random as rnd

# List installed modules
help("modules")
```

## Common Standard Libraries

```python
import os         # OS functions
import sys        # System-specific parameters
import datetime   # Dates and times
import time       # Time-related functions
import collections# Specialized container datatypes
import json       # JSON encoding/decoding
import re         # Regular expressions
import itertools  # Advanced iteration functions
```

## List Comprehensions

```python
squares = [x**2 for x in range(10)]
evens = [x for x in range(10) if x % 2 == 0]
pairs = [(x, y) for x in range(3) for y in range(3)]
```

## Useful Tips

- Indentation is crucial (use 4 spaces)
- Use `pip install package` for external packages
- Use `help(obj)` or `dir(obj)` for introspection
- Use `__name__ == "__main__"` to make code runnable as script

## Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
deactivate
```

## Decorators

```python
def decorator(func):
    def wrapper(*args, **kwargs):
        print("Before")
        result = func(*args, **kwargs)
        print("After")
        return result
    return wrapper

@decorator
def say_hello():
    print("Hello")
```

## Generators

```python
def count_up_to(n):
    i = 1
    while i <= n:
        yield i
        i += 1

for num in count_up_to(5):
    print(num)
```

## Useful One-liners

```python
[x for x in range(100) if x%2 == 0]           # Even numbers
{v:k for k,v in d.items()}                    # Swap dict keys/values
''.join(reversed('hello'))                    # Reverse string
sum(map(int, input().split()))                # Sum from input
```

## Type Hints

```python
def greet(name: str) -> str:
    return "Hello " + name
```

---

**References:**
- [Python Docs](https://docs.python.org/3/)
- [Real Python](https://realpython.com/)