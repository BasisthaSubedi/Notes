

# Understanding Loops in Python

Loops are one of the most essential control structures in programming. They allow for the repeated execution of a block of code as long as a certain condition is met. Python provides two primary types of loops: the `for` loop and the `while` loop. Both are widely used for iterating over sequences or repeating actions until a specific condition is satisfied.

## 1. The `for` Loop

The `for` loop in Python is generally used to iterate over a sequence (like a list, tuple, or string) or any other iterable object. The syntax for a `for` loop is as follows:

```python
for item in iterable:
    # Do something with item
```

### Example:
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
This will output:
```
apple
banana
cherry
```

In this example, the `for` loop iterates over each item in the `fruits` list and prints each element.

You can also use the `range()` function with `for` loops to generate a sequence of numbers. The `range()` function can accept up to three arguments: `start`, `stop`, and `step`.

### Example with `range()`:
```python
for i in range(1, 6):
    print(i)
```
This will output:
```
1
2
3
4
5
```

## 2. The `while` Loop

The `while` loop is used when you want to repeat a block of code as long as a specific condition is true. The syntax for a `while` loop is:

```python
while condition:
    # Do something
```

### Example:
```python
count = 0
while count < 5:
    print(count)
    count += 1
```
This will output:
```
0
1
2
3
4
```

In this example, the loop continues to execute as long as the condition `count < 5` is true. Once `count` reaches 5, the condition becomes false, and the loop terminates.

### Infinite Loop:
A `while` loop can result in an infinite loop if the condition never becomes false. For example:

```python
while True:
    print("This will run forever!")
```

To break out of such loops, you can use a `break` statement (as seen in the next section).

## 3. Loop Control Statements

### `break` Statement:
The `break` statement is used to exit the loop prematurely, regardless of whether the loop's condition has been met.

### Example:
```python
for i in range(10):
    if i == 5:
        break
    print(i)
```
This will output:
```
0
1
2
3
4
```
Here, the loop terminates when `i` equals 5, even though the loop was supposed to run for 10 iterations.

### `continue` Statement:
The `continue` statement is used to skip the current iteration and move to the next one.

### Example:
```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```
This will output:
```
0
1
3
4
```
When `i` equals 2, the `continue` statement skips the print statement for that iteration.
