# Functions in Python - Part 1

Functions are one of the core building blocks in Python programming. A function is a reusable block of code designed to perform a specific task. By defining a function, you can execute the same piece of code multiple times, which promotes code reusability and improves code readability.

## 1. Defining Functions

To define a function in Python, we use the `def` keyword, followed by the function name, and a pair of parentheses. Any input to the function (parameters) goes inside the parentheses. The function definition ends with a colon, and the code inside the function is indented.

### Syntax:
```python
def function_name(parameters):
    # Code block
    return value  # Optional return
```

### Example:
```python
def greet(name):
    print(f"Hello, {name}!")
```

Here, the function `greet` takes one parameter `name` and prints a greeting message. You can call this function by passing a string value as an argument:

```python
greet("Alice")  # Output: Hello, Alice!
```

## 2. Parameters and Arguments

Functions can accept inputs known as parameters. When calling a function, you provide values known as arguments. Parameters are placeholders in the function definition, while arguments are the actual values passed to the function.

### Example with Parameters:
```python
def add(a, b):
    return a + b
```

In this example, `a` and `b` are parameters. When calling the function:

```python
result = add(3, 5)  # Arguments: 3 and 5
print(result)        # Output: 8
```

You can pass multiple arguments or just one, depending on the function's definition.

## 3. Default Parameters

You can define default values for parameters. If no argument is provided for that parameter, the default value is used.

### Example:
```python
def greet(name="Guest"):
    print(f"Hello, {name}!")
```

Here, if no argument is passed, the function will use "Guest" as the default name:

```python
greet()       # Output: Hello, Guest!
greet("John") # Output: Hello, John!
```

### 4. Return Statement

The `return` statement is used to send back a result from a function. If no `return` statement is provided, the function returns `None` by default.

### Example:
```python
def multiply(x, y):
    return x * y
```

Calling the function:

```python
result = multiply(4, 5)
print(result)  # Output: 20
```

The `return` statement allows you to send back any kind of data, including numbers, strings, lists, or even another function.

