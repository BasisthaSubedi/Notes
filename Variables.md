# Variables in Python

In Python, variables are used to store data values. A variable is essentially a container for a value, and the value can be of any data type, such as a number, string, or even more complex data types like lists and dictionaries. Variables make it easier to manipulate and work with data in a program.

### 1. **Declaring Variables**

To declare a variable in Python, you simply need to assign a value to a variable name using the `=` operator. Unlike some other programming languages, Python does not require you to declare the type of the variable explicitly. Python automatically infers the data type based on the value assigned.

### Example:
```python
x = 5
name = "Alice"
is_active = True
```
In this example:
- `x` is assigned an integer value (`5`).
- `name` is assigned a string value (`"Alice"`).
- `is_active` is assigned a boolean value (`True`).

### 2. **Variable Naming Rules**

When naming variables, there are a few important rules to follow:
- A variable name must start with a letter (a-z, A-Z) or an underscore (`_`).
- The rest of the name can contain letters, numbers (0-9), or underscores.
- Variable names are case-sensitive, meaning `age` and `Age` would be considered two different variables.
- Reserved words or keywords (like `if`, `for`, `while`, etc.) cannot be used as variable names.

### 3. **Assigning Values to Variables**

You can reassign a new value to a variable at any time during the program. Python allows dynamic typing, meaning that the data type of a variable can change throughout the program.

### Example:
```python
x = 10        # x is an integer
x = "Hello"   # Now x is a string
```

### 4. **Multiple Variable Assignment**

Python allows you to assign values to multiple variables in one line, separated by commas.

### Example:
```python
a, b, c = 5, "Bob", 3.14
```
Here, `a` is assigned the value `5`, `b` gets `"Bob"`, and `c` is assigned `3.14`.

### 5. **Variable Types**

Variables can store different types of data, such as:
- `int` for integers (e.g., `10`)
- `float` for floating-point numbers (e.g., `3.14`)
- `str` for strings (e.g., `"Hello"`)
- `bool` for boolean values (`True` or `False`)

You can check the type of a variable using the `type()` function.

### Example:
```python
x = 5
print(type(x))  # Output: <class 'int'>
```