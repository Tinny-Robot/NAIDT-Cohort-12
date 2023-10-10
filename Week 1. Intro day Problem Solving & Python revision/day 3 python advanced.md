# Introduction
Advance Python Techniques

# Error Handling in Python 

Welcome to  Error Handling in Python!

Error handling is essential for gracefully handling unexpected situations during program execution.
## Introduction to Errors and Exceptions

Syntax errors vs. exceptions: Syntax errors occur when the code violates the rules of the programming language, while exceptions are raised during the program's execution.
Common types of exceptions in Python: Examples include **TypeError**, **ValueError**, **FileNotFoundError**, etc.\


## 3: Try-Except Block


Syntax and structure of the try-except block: The try block contains the code that might raise an exception, and the except block specifies how to handle the exception.

Handling specific exceptions: Multiple except blocks can be used to handle different exceptions separately.

Multiple except blocks and their order of execution: The first matching except block is executed, so the order of except blocks is crucial.

Handling multiple exceptions with a single except block: Multiple exceptions can be specified within a single except block.

Using the else clause with try-except: The else clause is executed when no exceptions occur in the try block.
### Code Example:

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
```
## 4: Handling Exceptions and Obtaining Information

Accessing the exception message: The exception message can be obtained using the str function or directly accessing the args attribute of the exception object.

Using the traceback module for detailed error information: The traceback module provides functions to access and print detailed error information.

Raising exceptions explicitly with the raise statement: Custom exceptions can be raised using the raise statement.

Creating custom exception classes: Custom exception classes can be defined by inheriting from the built-in Exception class.

### Code Example:

```python

try:
    raise ValueError("This is a custom exception.")
except ValueError as e:
    print("Exception message:", str(e))
```

## 5: Handling Exceptions in Real-World Scenarios

File handling and exception handling: Exception handling is crucial when working with files to handle potential errors like file not found or permission issues.

Exception handling in database operations: Error handling is essential when performing database operations to handle connection errors or query failures.

Exception handling with network requests: Exception handling is important for handling network-related errors like connection timeouts or HTTP errors.

Best practices for error handling in production code: Suggestions for handling exceptions effectively, such as logging errors and providing meaningful error messages.

### Code Example:

```python

try:
    file = open("example.txt", "r")
    # Perform file operations
    file.close()
except FileNotFoundError:
    print("Error: File not found.")
except PermissionError:
    print("Error: Permission denied.")
```


## 6: Exception Handling Techniques and Patterns


Using the finally block for cleanup actions: The finally block is executed regardless of whether an exception occurs, allowing for cleanup tasks.

Context managers and the "with" statement: Context managers simplify resource management and automatically handle clean-up actions.

Suppressing exceptions with the "pass" statement: The pass statement allows the handling of exceptions without performing any actions.

Logging and error reporting strategies: Proper logging and error reporting help in diagnosing and fixing issues in production code.

### Code Example:

```python

try:
    file = open("example.txt", "r")
    # Perform file operations
finally:
    file.close()
```
## 7: Exception Propagation and Debugging



Understanding exception propagation across function calls: Exceptions can be propagated up the call stack until they are handled or reach the top-level of the program.

Using debugger tools for error diagnosis: Debugging tools like breakpoints and stepping through code aid in identifying the cause of exceptions.

Debugging techniques for handling complex exceptions: Strategies for debugging complex issues that involve multiple exceptions or intricate error flows.

### Code Example:

```python
def divide(a, b):
    return a / b

def perform_calculation():
    try:
        result = divide(10, 0)
    except Exception as e:
        print("An error occurred:", str(e))

perform_calculation()

```
Final Example
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print("Result:", result)
except ValueError:
    print("Invalid input. Please enter a valid number.")
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
except Exception as e:
    print("An error occurred:", str(e))
else:
    print("No exceptions occurred.")
finally:
    print("This code will always execute, regardless of exceptions.")
```

 - - -
 - - -
 - - -
 - - -



# File Handling in Python 

Welcome to the 1-hour class on File Handling in Python!

File handling is essential for reading from and writing to files in a program.

## 2: Opening and Closing Files


Opening files with the open() function: The open() function is used to open files in different modes (e.g., read, write, append).

File modes: Examples include **'r'** for reading, **'w'** for writing, and **'a'** for appending.

Closing files with the **close()** method: It's important to close files after using them to free up system resources.

### Code Example:

```python

file = open("example.txt", "r")
# Perform file operations
file.close()
```

## 3: Reading from Files


Reading file content using **read()** and **readlines()**: The **read()** method reads the entire file content, while **readlines()** returns a list of lines.

Iterating over file lines: By iterating over the file object, we can process each line individually.
Using the with statement for automatic file closing: The with statement ensures proper file closing and exception handling.

### Code Example:

```python

with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
## 4: Writing to Files


Writing to files using **write()** and **writelines()**: The **write()** method is used to write a string to a file, while **writelines()** writes a list of strings.

Overwriting vs. appending: Opening a file in write mode (**'w'**) overwrites the existing content, while appending (**'a'**) adds new content at the end.

Using the with statement for automatic file closing: The with statement ensures proper file closing and exception handling.
### Code Example:

```python

with open("example.txt", "w") as file:
    file.write("Hello, World!")
```

## 5: File Pointer and Seeking


Understanding the file pointer: The file pointer indicates the current position within the file.

Moving the file pointer with **seek()**: The **seek()** method allows us to move the file pointer to a specific position.
Reading and writing at a specific file position: By moving the file pointer, we can read or write at a desired location within the file.
Code Example:

```python

with open("example.txt", "r") as file:
    file.seek(5)  # Move the file pointer to position 5
    content = file.read()
    print(content)
```
## 6: Error Handling in File Operations



Handling file-related exceptions: Exceptions like FileNotFoundError or PermissionError may occur during file handling.

Using try-except blocks for error handling: Wrap file operations in a try-except block to handle potential exceptions gracefully.

Providing meaningful error messages: Displaying informative error messages helps with troubleshooting and debugging.

Code Example:

```python
try:
    file = open("example.txt", "r")
    # Perform file operations
except FileNotFoundError:
    print("Error: File not found.")
except PermissionError:
    print("Error: Permission denied.")
finally:
    file.close()
```

## 7: File Handling Best Practices



- Properly closing files: Always close files after using them to avoid resource leaks.

- Using context managers: The with statement is recommended for file handling, as it automatically handles file closing.

- Error handling and exception management: Handle file-related exceptions and provide appropriate error messages.

- Proper file permissions and access controls: Ensure the program has the necessary permissions to read from and write to files.

## 8: Conclusion

File handling is a fundamental aspect of Python programming, allowing us to read from and write to files effectively.

Practice working with files, experiment with different modes, and explore advanced file handling techniques to enhance your skills.

Remember, file handling is an essential skill for building applications that interact with external data. Mastering this skill will make you a more versatile and capable Python programmer. Good luck!