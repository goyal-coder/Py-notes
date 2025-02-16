## Python Full Course Notes

### Introduction to Python
- Python is an interpreted, high-level, and general-purpose programming language.
- Created by Guido van Rossum in 1991.
- Python follows a simple and readable syntax similar to English.

### Variables and Data Types
- Variables store values and do not require explicit declaration.
- Common data types:
  - `int` (integer)
  - `float` (decimal numbers)
  - `str` (string)
  - `bool` (boolean - True/False)
  - `list` (ordered, mutable collection)
  - `tuple` (ordered, immutable collection)
  - `dict` (key-value pairs)
  - `set` (unordered collection of unique elements)

### Basic Input and Output
- `input()` is used to take user input.
- `print()` is used to display output.
- Type casting can be done using `int()`, `float()`, `str()`, etc.

### Operators
- Arithmetic operators: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- Comparison operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
- Logical operators: `and`, `or`, `not`
- Assignment operators: `=`, `+=`, `-=`, `*=`, `/=`, etc.

### Conditional Statements
- `if` statement executes code if a condition is true.
- `if-else` provides an alternative execution path.
- `if-elif-else` allows multiple conditions to be checked.

Example:
```python
num = int(input("Enter a number: "))
if num > 0:
    print("Positive")
elif num < 0:
    print("Negative")
else:
    print("Zero")
```

### Loops
- `for` loop is used for iterating over a sequence.
- `while` loop executes as long as a condition is true.
- Loop control statements:
  - `break` exits the loop.
  - `continue` skips the current iteration.
  - `pass` is a placeholder.

Example:
```python
for i in range(5):
    print(i)
```

### Functions
- Functions are defined using `def` keyword.
- Parameters allow passing data into functions.
- `return` statement returns a value.

Example:
```python
def add(a, b):
    return a + b
print(add(3, 4))
```

### Lists
- Lists store multiple items in a single variable.
- Lists are mutable (can be changed).
- Common methods: `append()`, `remove()`, `pop()`, `sort()`, `reverse()`.

Example:
```python
my_list = [1, 2, 3]
my_list.append(4)
print(my_list)
```

### Tuples
- Similar to lists but immutable.
- Defined using parentheses `()`.

Example:
```python
tuple1 = (1, 2, 3)
print(tuple1[0])
```

### Dictionaries
- Stores key-value pairs.
- Access elements using keys.

Example:
```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict["name"])
```

### Sets
- Unordered collection of unique items.

Example:
```python
my_set = {1, 2, 3, 3}
print(my_set)
```

### File Handling
- Opening a file: `open('filename', 'mode')`
- Modes: `r` (read), `w` (write), `a` (append), `r+` (read and write).

Example:
```python
with open("test.txt", "w") as f:
    f.write("Hello, world!")
```

### Exception Handling
- `try` and `except` blocks handle errors.

Example:
```python
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### Object-Oriented Programming (OOP)
- Classes and Objects.
- Inheritance, Polymorphism, Encapsulation, Abstraction.

Example:
```python
class Car:
    def __init__(self, brand):
        self.brand = brand
    def show(self):
        print("Car brand:", self.brand)

car1 = Car("Toyota")
car1.show()
```

### Additional Topics
- **Lambda Functions**: `lambda x, y: x + y`
- **Map, Filter, Reduce**: Used for functional programming.
- **Regular Expressions**: `re` module for pattern matching.
- **Multithreading**: `threading` module for parallel execution.
- **Database Connectivity**: `sqlite3` for database operations.
- **APIs and Web Scraping**: `requests`, `BeautifulSoup` for web data.

---
These notes cover essential Python topics with examples. More details can be added based on further learning! 🚀
