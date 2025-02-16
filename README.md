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

# Booleans

These are used in if else statements mostly.

# Some Values are False

In fact, there are not many values that evaluate to `False`, except empty values, such as `()`, `[]`, `{}`, `""`, the number `0`, and the value `None`. And of course the value `False` evaluates to `False`. one more that is if you have an object that is made from a class with a `__len__` function that returns `0` or `False`

# Operators

I think this is the easiest topic.

Python divides the operators in the following groups:

- Arithmetic operators
- Assignment operators
- Comparison operators
- Logical operators
- Identity operators
- Membership operators
- Bitwise operators

# Python Arithmetic Operators

Arithmetic operators are used with numeric values to perform common mathematical operations:

| Operator | Name | Example |
| --- | --- | --- |
| + | Addition | x + y |
| - | Subtraction | x - y |
| * | Multiplication | x * y |
| / | Division | x / y |
| % | Modulus | x % y |
| ** | Exponentiation | x ** y |
| // | Floor division | x // y |

# Python Assignment Operators

Assignment operators are used to assign values to variables:

| Operator | Example | Same As |
| --- | --- | --- |
| = | x = 5 | x = 5 |
| += | x += 3 | x = x + 3 |
| -= | x -= 3 | x = x - 3 |
| *= | x *= 3 | x = x * 3 |
| /= | x /= 3 | x = x / 3 |
| %= | x %= 3 | x = x % 3 |
| //= | x //= 3 | x = x // 3 |
| **= | x **= 3 | x = x ** 3 |
| &= | x &= 3 | x = x & 3 |
| |= | x |= 3 | x = x | 3 |
| ^= | x ^= 3 | x = x ^ 3 |
| >>= | x >>= 3 | x = x >> 3 |
| <<= | x <<= 3 | x = x << 3 |
| := | print(x := 3) | x = 3print(x) |

# Python Comparison Operators

Comparison operators are used to compare two values:

| Operator | Name | Example |
| --- | --- | --- |
| == | Equal | x == y |
| != | Not equal | x != y |
| > | Greater than | x > y |
| < | Less than | x < y |
| >= | Greater than or equal to | x >= y |
| <= | Less than or equal to | x <= y |

# Python Logical Operators

Logical operators are used to combine conditional statements:

| Operator | Description | Example |
| --- | --- | --- |
| and | Returns True if both statements are true | x < 5 and  x < 10 |
| or | Returns True if one of the statements is true | x < 5 or x < 4 |
| not | Reverse the result, returns False if the result is true | not(x<5 and x<10) |

# Python Identity Operators

Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:

| Operator | Description | Example |
| --- | --- | --- |
| is | Returns True if both variables are the same object | x is y |
| is not | Returns True if both variables are not the same object | x is not y |

# Python Membership Operators

Membership operators are used to test if a sequence is presented in an object:

| Operator | Description | Example |
| --- | --- | --- |
| in | Returns True if a sequence with the specified value is present in the object | x in y |
| not in | Returns True if a sequence with the specified value is not present in the object | x not in y |

# Python Bitwise Operators

Bitwise operators are used to compare (binary) numbers:

| Operator | Name | Description | Example |
| --- | --- | --- | --- |
| & | AND | Sets each bit to 1 if both bits are 1 | x & y |
| | | OR | Sets each bit to 1 if one of two bits is 1 | x | y |
| ^ | XOR | Sets each bit to 1 if only one of two bits is 1 | x ^ y |
| ~ | NOT | Inverts all the bits | ~x |
| << | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off | x << 2 |
| >> | Signed right shift | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off |  |

Opearot precedence

| Operator | Description | Try it |
| --- | --- | --- |
| `()` | Parentheses | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_parentheses) |
| `**` | Exponentiation | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_exponent) |
| `+x`  `-x`  `~x` | Unary plus, unary minus, and bitwise NOT | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_bitwise_not) |
| `*`  `/`  `//`  `%` | Multiplication, division, floor division, and modulus | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_multiplication) |
| `+`  `-` | Addition and subtraction | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_subtraction) |
| `<<`  `>>` | Bitwise left and right shifts | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_shift) |
| `&` | Bitwise AND | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_bitwise_and) |
| `^` | Bitwise XOR | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_bitwise_xor) |
| `|` | Bitwise OR | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_bitwise_or) |
| `==`  `!=`  `>`  `>=`  `<`  `<=`  `is`  `is not`  `in`  `not in` | Comparisons, identity, and membership operators | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_like) |
| `not` | Logical NOT | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_not) |
| `and` | AND | [Try it »](https://www.w3schools.com/python/trypython.asp?filename=demo_precedence_and) |
| `or` | OR |  |

Mostly Asked in interview


