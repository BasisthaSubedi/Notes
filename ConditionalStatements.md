# Conditional Statements in Python

Conditional statements allow your Python program to make decisions and execute specific blocks of code based on whether a condition is true or false. This is fundamental to control the flow of your program, enabling it to behave differently under various circumstances.

## Types of Conditional Statements

There are three primary conditional statements in Python:

1. **`if` statement**
2. **`elif` (else if) statement**
3. **`else` statement**

### 1. `if` Statement

The `if` statement is the simplest conditional statement. It evaluates a given condition and executes a block of code if the condition evaluates to `True`.

#### Syntax:
```python
if condition:
    # code block
```

- **Condition**: The expression inside the `if` statement must evaluate to `True` or `False` (Boolean value).
- **Code block**: If the condition is `True`, the indented block of code immediately following the `if` statement runs.

#### Example:
```python
age = 20

if age >= 18:
    print("You are an adult.")
```
In this case, the condition `age >= 18` evaluates to `True`, so the program prints `"You are an adult."`.

### 2. `elif` Statement

The `elif` (short for "else if") statement allows you to check multiple conditions. If the first `if` condition evaluates to `False`, the program checks the `elif` condition. You can have multiple `elif` branches.

#### Syntax:
```python
if condition_1:
    # code block 1
elif condition_2:
    # code block 2
```

- If the first `if` condition is `False`, the program checks the `elif` condition.
- You can have any number of `elif` statements to check multiple conditions sequentially.

#### Example:
```python
age = 16

if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
```
Here, `age = 16` evaluates to the second condition, and the output will be `"You are a teenager."`.

### 3. `else` Statement

The `else` statement is used as a "catch-all" option, where the program executes a block of code if none of the preceding conditions are `True`. The `else` block does not require a condition, and it will execute when all other conditions are `False`.

#### Syntax:
```python
if condition_1:
    # code block 1
elif condition_2:
    # code block 2
else:
    # code block 3
```

- The `else` block runs only if all preceding `if` and `elif` conditions fail.

#### Example:
```python
age = 10

if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```
In this case, since `age = 10`, both the `if` and `elif` conditions are false, so the program prints `"You are a child."`.

## Logical Operators

You can combine conditions using logical operators like:

- `and`: Returns `True` if **both** conditions are `True`.
- `or`: Returns `True` if **at least one** condition is `True`.
- `not`: Reverses the Boolean value of a condition (True becomes False and vice versa).

#### Example:
```python
age = 20
income = 3000

if age >= 18 and income > 2500:
    print("Eligible for the loan.")
```
Here, both conditions must be true for the block of code to execute.

## Nested Conditionals

You can nest one conditional statement inside another to check more complex conditions.

#### Example:
```python
x = 10

if x > 5:
    if x < 15:
        print("x is between 5 and 15")
```
