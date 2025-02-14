## What is Python?

Python is a **popular programming language** created by **Guido van Rossum** and released in **1991**.

## Why Python?

1. Works on different platforms (Windows, Mac, Linux, etc.).
2. Simple and easy-to-read syntax.
3. Executes code **line by line** (interpreted language).

## Syntax

Python uses **indentation** instead of braces `{}`. Indentation matters a lot in Python!

---

## 🔗 Practice Links

- [**Quiz**](https://pynative.com/basic-python-quiz-for-beginners/)
- [**Questions**](https://technovlogs.com/30-python-programming-questions-on-operators-and-expressions/)
- [**W3Resource**](https://www.w3resource.com/python-exercises/)

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

- Convert one data type to another using functions like `str()`, `int()`, `float()`, etc.

```python
x = 6
print(str(x))  # '6' (string)

```

### Get Variable Type

```python
y = 10.5
print(type(y))  # <class 'float'>

```

### Variable Naming Rules

✅ Must **start** with a letter or an underscore `_`

✅ Can contain **letters, numbers, and underscores** (`A-z, 0-9, _`)

❌ Cannot **start** with a number

❌ Case-sensitive (`myVar`, `Myvar`, `MYVAR` are different)

### Assign Multiple Values

```python
x, y, z = 1, 2, 3

```

Useful in many programs!

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

There is also a **`range`** class:

```python
type(range(5))  # Output: <class 'range'>

```

---

## Understanding `id()` in Python

Python **optimizes memory** by assigning the same ID to variables with the same immutable values.

Example:

```python
a = 10
b = 10
print(id(a))  # Same ID
print(id(b))  # Same ID

c = 20
d = 20
e = 20
print(id(c))  # Same ID for all three
print(id(d))
print(id(e))

```

Since `a` and `b` have the **same value**, they share the **same memory location**. Comparing them (`a == b`) will return `True`.

---

### 📌 Numbers

1. **int**: A normal number.
2. **float**: A number with decimals.
3. **complex**: A number with alphabets.

➡️ Generate a random number using the **random** module.

---

### 📌 Strings

1. Strings can be made using **single (' ')**, **double (" ")**, or **triple quotes (""" """)** for multiline.
2. Strings are **arrays** in Python.

---

### 📌 Slicing

1. **Start & end value** → `string[0:1]`
2. **Start, end & step** → `string[1:12:2]`
3. **Negative indexing** → Rarely used, but good to know!

---

### 📌 Concatenation

```python
python
CopyEdit
a = "Hello"
b = "World"
c = a + b
print(c)  # HelloWorld

```

---

### 📌 String Formatting

✅ **f-strings** (modern & preferred)

```python
python
CopyEdit
a = "hello"
print(f"{a}")  # hello

```

---

### 📌 Escape Characters

| Escape | Meaning |
| --- | --- |
| `\'` | Single Quote |
| `\\` | Backslash |
| `\n` | New Line |
| `\r` | Carriage Return |
| `\t` | Tab |
| `\b` | Backspace |
| `\f` | Form Feed |
| `\ooo` | Octal Value |
| `\xhh` | Hex Value |

### 📌 String Methods

💡 Learn more: [W3Schools - String Methods](https://www.w3schools.com/python/python_strings_methods.asp) 🚀

