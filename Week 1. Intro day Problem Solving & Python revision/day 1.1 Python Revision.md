# Python Revision Class - 1 Hour

## Introduction to Python

Python is a high-level, interpreted programming language known for its simplicity and readability. It's widely used in various domains, such as web development, data analysis, artificial intelligence, and more. Let's start with some basics.

## Variables and Data Types

In Python, we use variables to store values. They don't require explicit declaration and their data type is dynamically inferred. Python supports various data types like integers, floats, strings, booleans, and more. Let's see some examples:

**Code Example 1**:
```python
age = 25
name = "John Doe"
is_new = True
```

## Operators 
 Operators are a fundamental part of Python, and they allow you to perform various operations on data. Here are some of the most commonly used operators in Python:

1. **Arithmetic Operators**:
   - Addition: `+`
   - Subtraction: `-`
   - Multiplication: `*`
   - Division: `/`
   - Modulus (remainder): `%`
   - Exponentiation: `**`
   - Floor Division (rounded down division): `//`

   Example:
   ```python
   a = 10
   b = 3
   sum_result = a + b
   division_result = a / b
   ```

2. **Comparison Operators**:
   - Is Equal to: `==`
   - Not equal to: `!=`
   - Greater than: `>`
   - Less than: `<`
   - Greater than or equal to: `>=`
   - Less than or equal to: `<=`

   Example:
   ```python
   x = 5
   y = 8
   is_equal = x == y
   ```

3. **Logical Operators**:
   - Logical AND: `and`
   - Logical OR: `or`
   - Logical NOT: `not`

   Example:
   ```python
   is_true = True
   is_false = False
   result = is_true and is_false
   ```

4. **Assignment Operators**:
   - Assignment: `=`
   - Addition Assignment: `+=`
   - Subtraction Assignment: `-=`
   - Multiplication Assignment: `*=`
   - Division Assignment: `/=`

   Example:
   ```python
   x = 10
   x += 5  # Equivalent to x = x + 5
   ```

5. **Bitwise Operators** (for working with binary data):
   - Bitwise AND: `&`
   - Bitwise OR: `|`
   - Bitwise XOR: `^`
   - Bitwise NOT: `~`
   - Left Shift: `<<`
   - Right Shift: `>>`

   Example:
   ```python
   a = 5  # Binary: 0101
   b = 3  # Binary: 0011
   result = a & b  # Bitwise AND: 0001 (Decimal: 1)
   ```

You can use these operators in your Python code to perform various operations and calculations.


## Control Flow Statements
Control flow statements allow us to control the flow of execution in our programs. We have conditional statements like if-else and loops like for and while. Let's look at an example:

**Code Example 2**:

```python
num = 10
if num > 0:
    print("Positive number")
elif num == 0:
    print("Zero")
else:
    print("Negative number")

```
## Loop

Loops in Python are control structures that allow you to execute a block of code repeatedly. Python provides two main types of loops: `for` loops and `while` loops.

### `for` Loops:
- `for` loops are used for iterating over a sequence (such as a list, tuple, string, or range) or other iterable objects.
- They execute a set of statements for each item in the sequence.
- You can use the `for` loop along with the `range()` function to loop a specific number of times.

Example:
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### `while` Loops:
- `while` loops repeatedly execute a block of code as long as a given condition is `True`.
- They are suitable when you want to loop until a specific condition is met.

Example:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

Loops are powerful tools in Python for automating repetitive tasks, processing data, and iterating through collections. They allow you to efficiently perform actions like data manipulation, calculations, and more. Remember to use appropriate looping constructs based on the problem you are solving to make your code more efficient and readable.

## Functions
Functions in Python help us divide our code into reusable blocks. They improve code organization and reusability. Let's see how to define and call a function:

**Code Example 3**:

```python
def greet(name):
    print("Hello, " + name + "!")

greet("Alice")
```

## Lists and Dictionaries
Lists and dictionaries are two fundamental data structures in Python. Lists are ordered collections of elements, while dictionaries are key-value pairs. Let's see some examples:

**Code Example 4**:

```python
fruits = ["apple", "banana", "orange"]
person = {"name": "John", "age": 30, "city": "New York"}
```

## File Handling
Python provides convenient ways to read from and write to files. Let's see an example of reading and writing data to a file:

**Code Example 5**:
```python
# Reading from a file
file = open("data.txt", "r")
content = file.read()
print(content)
file.close()

# Writing to a file
file = open("output.txt", "w")
file.write("Hello, World!")
file.close()

```

## Error Handling
Errors are common in programming, but Python provides robust error handling mechanisms using try-except blocks. Let's see an example:

**Code Example 6**:

```python
try:
    num = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero")
```

## Modules and Packages
Python offers a vast ecosystem of modules and packages that extend its capabilities. We can import and use them in our programs. Let's see an example of using the math module: