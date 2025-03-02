# Hello World in Python

Hello, World! in Python is the first Python program that we learn when we start learning any programming language. It’s a simple program that displays the message “Hello, World!” on the screen.

Here’s the “Hello World” program:

```python
print("Hello, World!")
```
# Python Comments

Comments in Python are the lines in the code that are ignored by the interpreter during the execution of the program.

## Importance of Comments:

- **Enhance Readability**: Comments help make the code more readable and understandable for others (or even for yourself when you come back to the code later).
  
- **Identify Functionality**: Comments can be used to explain what a certain section of the code is doing, making it easier to understand its purpose and logic.
  
- **Structure the Code-Base**: Comments can help organize the code, making it easier to navigate through large codebases by adding headings or explanations for different parts of the program.
  
- **Explain Tricky Scenarios**: Comments are useful for explaining unusual or complex sections of code, helping others (or yourself) avoid accidental removal or changes.
  
- **Prevent Code Execution**: Comments can be used to temporarily prevent executing specific parts of the code, useful when making changes or testing different sections without deleting the code.
  
## Example of Comments in Python:

```python
# This is a single-line comment

# The following function calculates the square of a number
def square(x):
    return x ** 2

# print(square(5))  # This line is commented out for testing purposes
```
# Explanation:

- In Python, single line comments starts with  hashtag symbol #.
Python ignores the string literals that are not assigned to a variable. So, we can use these string literals as Python Comments.

# Python Indentation

In Python, indentation is not just for readability; it is **required** to define the structure of the code. Unlike many other programming languages, Python uses indentation to indicate blocks of code rather than braces `{}`.

## Importance of Indentation:

- **Defines Code Blocks**: Indentation is used to define the body of loops, functions, classes, and conditionals. Without proper indentation, Python will throw an error because it won't know where a block starts or ends.

- **Enhances Readability**: Consistent indentation makes the code easier to read and understand. It visually separates different sections of the code, improving clarity.

- **Prevents Syntax Errors**: Improper indentation can lead to syntax errors or unexpected behavior in the code. It's essential to use consistent indentation to avoid such issues.

## Rules of Indentation in Python:

- **Consistent Spaces or Tabs**: Python requires that you use either spaces or tabs for indentation, but **you cannot mix both** in the same project. PEP 8 (Python’s style guide) recommends using **4 spaces** for each level of indentation.
  
- **Indentation in Loops and Conditionals**: Code inside loops or conditionals must be indented. Python uses indentation to determine which code belongs to which loop or condition.
  
- **No Indentation for Code Outside Blocks**: Code that is not part of any block, such as simple function definitions or statements, should not be indented.

## Example of Proper Indentation:

```python
# Example of using indentation in Python

def greet(name):
    # This is the body of the function, indented by 4 spaces
    print(f"Hello, {name}!")

if __name__ == "__main__":
    # This is the main block, indented under the if statement
    greet("Alice")
    greet("Bob")

    # Loop with indentation to define the body of the loop
    for i in range(3):
        print(i)  # This print statement is part of the for loop body
