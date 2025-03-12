# Functions in Python - Part 2

## 5. Variable Scope and Lifetime

Variables defined inside a function are local to that function. This means they exist only while the function is executing. These variables are not accessible outside the function, which helps in preventing accidental changes to them.

### Example:
```python
def example_function():
    x = 10  # Local variable
    print(x)

example_function()  # Output: 10
print(x)             # Error: NameError: name 'x' is not defined
```

On the other hand, variables defined outside any function are considered global. They can be accessed from within any function using the `global` keyword.

### Example with Global Variables:
```python
x = 5  # Global variable

def access_global():
    global x
    x = 10  # Modifies the global variable

access_global()
print(x)  # Output: 10
```

The `global` keyword allows the function to modify the global variable instead of creating a new local one.

## 6. Lambda Functions

Lambda functions are small anonymous functions defined using the `lambda` keyword. These functions are often used when you need a simple function for a short period.

### Syntax:
```python
lambda arguments: expression
```

### Example:
```python
add = lambda a, b: a + b
print(add(3, 4))  # Output: 7
```

Lambda functions are particularly useful when working with functions like `map()`, `filter()`, or `sorted()`, where a small, one-line function is required.

## 7. Functions as First-Class Objects

In Python, functions are first-class citizens, meaning they can be passed around as arguments, returned from other functions, or assigned to variables. This allows for powerful functional programming techniques.

### Example of Passing Functions as Arguments:
```python
def operate_on_two_numbers(func, a, b):
    return func(a, b)

result = operate_on_two_numbers(lambda x, y: x - y, 10, 3)
print(result)  # Output: 7
```

In this example, the lambda function `lambda x, y: x - y` is passed as an argument to `operate_on_two_numbers()`, allowing for dynamic behavior based on the passed function.

## 8. Nested Functions

A function can also be defined inside another function, which is called a nested function. These inner functions can access variables from the enclosing (outer) function's scope.

### Example:
```python
def outer_function():
    def inner_function():
        return "Hello from inner function"
    print(inner_function())

outer_function()  # Output: Hello from inner function
```

While nested functions are useful, they are usually used for specific tasks like closures, which will be covered later.

