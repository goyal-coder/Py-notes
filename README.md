```markdown
# Python Notes

## What is Python?

Python is a **popular programming language** created by **Guido van Rossum** and released in **1991**.

## Why Python?

1. Works on different platforms (Windows, Mac, Linux, etc.).
2. Simple and easy-to-read syntax.
3. Executes code **line by line** (interpreted language).

## Syntax

Python uses **indentation** instead of braces `{}`. Indentation matters a lot in Python!

## What is a Statement?

A **statement is an instruction that a Python interpreter can execute**. In simple words, anything written in Python is a statement.

---

## 🔗 Practice Links

- [**Quiz**](<https://pynative.com/basic-python-quiz-for-beginners/>)
- [**Questions**](<https://technovlogs.com/30-python-programming-questions-on-operators-and-expressions/>)
- [**W3Resource**](<https://www.w3resource.com/python-exercises/>)

---

## Comments in Python

### 1. Normal Comment

```python
# This is a comment

```

### 2. Multiline Comment

```python
"""
This is a multiline comment.
It spans multiple lines.
"""

```

### 3. Docstring

- **Written inside a function**, right after its declaration.
- **Not a comment** but a description of what the function does.
- **Can be printed** using `print(function_name.__doc__)`.

Example:

```python
def greet():
    """This function prints a greeting message."""
    print("Hello, world!")

```

---

## Variables in Python

- No need to **declare** a variable type like JavaScript.
- **Case-sensitive** (`age`, `Age`, and `AGE` are different variables).

### Typecasting

There are two types of casting.

1. implicit: done by python interpreter itself.
2. explicit: we externally add methods to do so.

Convert one data type to another using functions like `str()`, `int()`, `float()`, etc.

```python
x = 6
print(str(x))  # '6' (string)

```

### Get Variable Type

```python
y = 10.5
print(type(y))  # <class 'float'>

```

- we can actually convert a bool to int which will either return 0 or 1.
- float will return 1.0 and 0.0
- In complex we can turn using complex(). `complex(x, y)`: To convert the value `x` and `y` into a `complex` type. In this form, the real value is `x`, and the imaginary is `y`.
- In string i guess only empty string returns false.

---

### Variable Naming Rules

✅ Must **start** with a letter or an underscore `_`

✅ Can contain **letters, numbers, and underscores** (`A-z, 0-9, _`)

❌ Cannot **start** with a number

❌ Case-sensitive (`myVar`, `Myvar`, `MYVAR` are different)

### Assign Multiple Values

```python
x, y, z = 1, 2, 3

```

### Assign One Value to Multiple Variables

```python
x = y = z = 10

```

### Global Variables

- A variable declared **outside** a function is **global**.
- Use `global` keyword to modify it inside a function.

Example:

```python
x = "awesome"

def myfunc():
    global x
    x = "fantastic"

myfunc()
print("Python is " + x)  # Output: Python is fantastic

```

---

## Data Types in Python

| **Category** | **Data Types** |
| --- | --- |
| **Text Type** | `str` |
| **Numeric Types** | `int`, `float`, `complex` |
| **Sequence Types** | `list`, `tuple`, `range` |
| **Mapping Type** | `dict` |
| **Set Types** | `set`, `frozenset` |
| **Boolean Type** | `bool` |
| **Binary Types** | `bytes`, `bytearray`, `memoryview` |
| **None Type** | `NoneType` |

This table for easier reference.

| **Data type** | **Description** | **Example** |
| --- | --- | --- |
| `int` | To store integer values. | `n = 20` |
| `float` | To store decimal values | `n = 20.75` |
| `complex` | To store complex numbers (real and imaginary part) | `n = 10+20j` |
| str | To store textual/string data | `name = 'Jessa'` |
| bool | To store boolean values | `flag = True` |
| list | To store a sequence of mutable data | `l = [3, 'a', 2.5]` |
| tuple | To store sequence immutable data | `t =(2, 'b', 6.4)` |
| dict | To store key: value pair | `d = {1:'J', 2:'E'}` |
| set | To store unorder and unindexed values | `s = {1, 3, 5}` |
| frozenset | To store immutable version of the set | `f_set=frozenset({5,7})` |
| range | To generate a sequence of number | `numbers = range(10)` |
| bytes | To store bytes values | `b=bytes([5,10,15,11])` |
- bytes are immutable. we have to create a normal array and then assign a new variable saying new=bytes(old_arr). now we can’t make any change in new.
- Frozen set also works like bytes. but these are used on set.
- byte array also works like bytes but byteaaray are mutable
- memoryview is like i still don’t know.
- In range the steps can not be 0 or else it will raise error.
- we can’t use float as an argument in range parameters.
- For reversed there are few methods. one is: using (10,-1,-1) ,second is using reversed method.

The range can become a hot topic itself:

| **Operation** | **Description** |
| --- | --- |
| `range(stop)` | Generate a sequence of integers from zero to stop-1 |
| `range(start, stop)` | Generate a sequence of integers from start to stop-1 |
| `range(start, stop, step)` | Generate a sequence of integers starting from the start number, increments by step, and stops before a stop number. I.e., Each next number is generated by adding the step value to a preceding number. |
| `range(5, -1, -1)` | Reverse range |
| `reversed(range(5))` | Reverse range using a `reversed()` function |
| `range(-1, -11, -1)` | Negative range from -1 to -10 |
| `list(range(2, 10, 2))` | Convert range() to list |
| `range(start, stop+step, step)` | Generate an inclusive range |
| `range(0, 10)[5]` | Access fifth number of a `range()` directly |
| `range(10)[3:8]` | Slice a range to access numbers from index 3 to 8 |
| `range.start` | Get the start value of a `range()` |
| `range.stop` | Get the stop value of a `range()` |
| `range.step` | Get the step value of a `range()` |

---

# Imp about inputs

I have to learn these:

1. `sys` module
2. `getopt`m odule
3. `argsparse` module
4. `fire` module
5. `docotp` module

# Imp things about output

1. format string and if you think that you know f string very well then you are judging the book by it’s cover.

---

## Understanding `id()` in Python

Python **optimizes memory** by assigning the same ID to variables with the same immutable values.

Example:

```python
a = 10
b = 10
print(id(a))  # Same ID
print(id(b))  # Same IDname, age, marks = input("Enter your Name, Age, Percentage separated by space ").split()
print("\\n")
print("User Details: ", name, age, marks)

```

---

## Numbers in Python

1. **int**: A normal number.
2. **float**: A number with decimals.
3. **complex**: A number with imaginary parts.

➡️ Generate a random number using the **random** module.

---

## Strings in Python

1. Strings can be made using **single (' ')**, **double (" ")**, or **triple quotes (""" """)** for multiline.
2. Strings are **arrays** in Python.

### 📌 Slicing

1. **Start & end value** → `string[0:1]`
2. **Start, end & step** → `string[1:12:2]`
3. **Negative indexing** → Rarely used, but good to know!

### 📌 Concatenation

```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)  # Hello World

```

### 📌 String Formatting

✅ **f-strings** (modern & preferred)

```python
a = "hello"
print(f"{a}")  # hello

```

### 📌 Escape Characters

| Escape | Meaning |
| --- | --- |
| `\\\\'` | Single Quote |
| `\\\\\\\\` | Backslash |
| `\\\\n` | New Line |
| `\\\\t` | Tab |

### 📌 String Methods

💡 Learn more: [W3Schools - String Methods](https://www.w3schools.com/python/python_strings_methods.asp) 🚀

---

## Booleans in Python

Booleans are mostly used in `if-else` statements.

Some values evaluate to `False`: `()`, `[]`, `{}`, `""`, `0`, `None`, and objects with `__len__()` returning `0`.

---

## Python Operators

Python divides the operators into different groups:

- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

### Arithmetic Operators

| Operator | Name | Example |
| --- | --- | --- |
| `+` | Addition | x + y |
| `-` | Subtraction | x - y |
| `*` | Multiplication | x * y |
| `/` | Division | x / y |
| `%` | Modulus | x % y |
| `**` | Exponentiation | x ** y |
| `//` | Floor division | x // y |

### Comparison Operators

| Operator | Name | Example |
| --- | --- | --- |
| `==` | Equal | x == y |
| `!=` | Not equal | x != y |
| `>` | Greater than | x > y |
| `<` | Less than | x < y |
| `>=` | Greater than or equal to | x >= y |
| `<=` | Less than or equal to | x <= y |

### Assignment Operators

| Operator | Meaning | Example |
| --- | --- | --- |
| `=` | Assign | a = 5 |
| `+=` | Add and assign | a += 5 |
| `-=` | Subtract and assign | a -= 5 |
| `*=` | Multiply and assign | a *= 5 |
| `/=` | Divide and assign | a /= 5 |
| `%=` | Modulus and assign | a %= 5 |
| `**=` | Exponentiation and assign | a **= 5 |
| `//=` | Floor-divide and assign | a //= 5 |

### Logical Operators

| Operator | Description | Example |
| --- | --- | --- |
| `and` | Logical AND | a and b |
| `or` | Logical OR | a or b |
| `not` | Logical NOT | not a |

### Membership Operators

- `in`: Returns `True` if the object is present in the sequence.
- `not in`: Returns `True` if the object is not present in the sequence.

### Identity Operators

- `is`: Returns `True` if both variables point to the same object.
- `is not`: Returns `True` if both variables do not point to the same object.

### Bitwise Operators

1. `&` Bitwise AND
2. `|` Bitwise OR
3. `^` Bitwise XOR
4. `~` Bitwise NOT
5. `<<` Bitwise left shift
6. `>>` Bitwise right shift

---

## Lists

- Lists are ordered, changeable, and allow duplicate values.
- They can store multiple data types.
- For more list methods visit w3schools.

### Changing Item Value

```python
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)

```

### Looping

- Use `for` or `while` loops, but `for` is easier.

### List Comprehensions

- A shorter way to write loops.

```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x for x in fruits if "a" in x]
print(newlist)

```

### Sorting

- Use `sort()` to sort alphanumerically.

```python
fruits.sort()

```

- For descending order:

```python
fruits.sort(reverse=True)

```

### Copying a List

- Use `list2 = list1.copy()` instead of `list2 = list1`.

### Joining Two Lists

- Using `+` operator:

```python
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]
list3 = list1 + list2
print(list3)

```

- Using `extend()`:

```python
list1.extend(list2)
print(list1)

```

---

## Tuples

- Tuples are ordered, unchangeable, and allow duplicate values.

```python
thistuple = ("apple", "banana", "cherry")

```

- Tuple with one item:

```python
thistuple = ("apple",)  # Notice the comma
print(type(thistuple))

```

---

## Sets

- Sets are unordered, unchangeable (but can add/remove items), and unindexed.

```python
thisset = {"apple", "banana", "cherry"}

```

---

## Dictionaries

- Dictionaries store key-value pairs.
- They are ordered (from Python 3.7+), changeable, and do not allow duplicates.

---

# Flow control statements

The flow control statements are divided into **three categories**

1. Conditional statements: if else
2. Iterative statements: for ,while
3. Transfer statements: break, continue, pass

## If-Else Statements

- Indentation is very important.

```python
a = 10
b = 5
if a > b:
    print("a is greater")
elif a == b:
    print("a and b are equal")
else:
    print("b is greater")

```

### Short-hand If

```python
if a > b: print("a is greater than b")

```

### Pass Statement

```python
if a > b:
    pass

```

---

## While Loops

```python
i = 1
while i < 6:
    print(i)
    i += 1

```

### Continue Statement

```python
i = 0
while i < 6:
    i += 1
    if i == 3:
        continue
    print(i)

```

### Else with While

```python
i = 1
while i < 6:
    print(i)
    i += 1
else:
    print("Loop finished!")
    
    #mostly asked in interviews

```

---

## For Loops

```python
for x in range(6):
    print(x)

```

### Else in For Loop

```python
for x in range(6):
    print(x)
else:
    print("Finally finished!")

 #mostly asked in interviews
```

---

## 

# Functions

- block of code used to make some functions that can be used many times.

### Two types of functions

1. built-in: range is a built in function.
2. User-defined: we create a function.

### Imp concepts

1. Docstring
2. Calling function
3. Parameters
4. Return
5. Scope
6. nonlocal keyword: used for variable inside a function inside a function.

### Python function arguments

1. Positional arguments
2. keyword arguments
3. Default arguments
4. Variable-length arguments: *args and **kargs.

# Recursive function

function that calls itself again and again.

**The advantages of the recursive function are:**

1. By using recursive, we can reduce the length of the code.
2. The readability of code improves due to code reduction.
3. Useful for solving a complex problem

**The disadvantage of the recursive function:**

1. The recursive function takes more memory and time for execution.
2. Debugging is not easy for the recursive function.

## Lambda function/anonymous

**Syntax of `lambda` function:**

```python
lambda: argument_list:expression
```

**Example : Program for even number with a lambda function**

`l = [10, 5, 12, 78, 6, 1, 7, 9]
even_nos = list(filter(lambda x: x % 2 == 0, l))
print("Even numbers are: ", even_nos)`

# Modules

Modules are nothing but a file containing some kind of code which will make it easier to program something. we borrow the code basically.

**Types of modules:**

1. Build in modules: comes with default py installation.
2. User-defined: we install and then use these like pandas.

### Rename a module

`from <module_name> import <name> as <alternative_name>`

or we can say that

`from math import random as rand`

We can also import all by usign `from math import*`  which is not a good practice at all.

# OOPS

There are so many  things to learn in Oops. check [oops](https://pynative.com/python/object-oriented-programming/).

# Exception handling

1. Try-except-finally
2. Raise
3. Exception chaining
4. Build in exceptions
5. Custom exceptions
