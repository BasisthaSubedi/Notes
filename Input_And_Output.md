# Input and Output in Python

Understanding input and output operations is fundamental to Python programming. With the `print()` function, we can display output in various formats, while the `input()` function enables interaction with users by gathering input during program execution.

## Printing Output using `print()` in Python

At its core, printing output in Python is straightforward, thanks to the `print()` function. This function allows us to display text, variables, and expressions on the console. Let’s begin with the basic usage of the `print()` function:

### Example:
```python
print("Hello, World!")
```
## Printing Single and Multiple Variables in Python

We can use the `print()` function to print single and multiple variables. We can print multiple variables by separating them with commas.

### Example:

```python
# Single variable
s = "Bob"
print(s)

# Multiple Variables
s = "Alice"
age = 25
city = "New York"
print(s, age, city)
```
### Output
```python
Bob
Alice 25 New York
```
## Output Formatting in Python

Output formatting in Python can be achieved using various techniques including the `format()` method, manipulation of the `sep` and `end` parameters, f-strings, and the versatile `%` operator. These methods allow precise control over how data is displayed, enhancing the readability and effectiveness of your Python programs.

### Example 1: Using `format()`

```python
amount = 150.75
print("Amount: ${:.2f}".format(amount))
```
### Output:
```python
Amount: $150.75
```

### Example 3: Using f-string

```python
name = 'Basistha'
age = 18
print(f"Hello, My name is {name} and I'm {age} years old.")
```
### Output:
```python
Hello, My name is Basistha and I'm 18 years old.
```
### Example 4: Using `%` Operator

We can use the `%` operator to format strings. Values are replaced with zero or more elements. The formatting using `%` is similar to the `printf` function in the C programming language.

- `%d` – integer
- `%f` – float
- `%s` – string
- `%x` – hexadecimal
- `%o` – octal

### Example: Taking Input from the User

```python
# Taking input from the user
num = int(input("Enter a value: "))

add = num + 5

# Output
print("The sum is %d" % add)
```
### Output:
```python
Enter a value: 50
The sum is 55
```
## Take Multiple Input in Python

We can take multiple inputs from the user in a single line by using the `split()` method to separate the values entered by the user into distinct variables. Based on the number of inputs provided, we can then print the corresponding values with labels.

### Example 1: Taking Two Inputs at a Time

```python
# taking two inputs at a time
x, y = input("Enter two values: ").split()
print("Number of boys: ", x)
print("Number of girls: ", y)
```
## Output
```python
Enter two values: 5 10
Number of boys:  5
Number of girls:  10

```
```python
# taking three inputs at a time
x, y, z = input("Enter three values: ").split()
print("Total number of students: ", x)
print("Number of boys is : ", y)
print("Number of girls is : ", z)
```
## Output:
```python
Enter three values: 5 10 15
Total number of students:  5
Number of boys is :  10
Number of girls is :  15
```
## Taking Input in Python

The `input()` function in Python is used to take user input. By default, it returns the user input as a string.

### Syntax:
```python
input(prompt)
```
```python
name = input("Enter your name: ")
print("Hello,", name, "! Welcome!")
```
## Output:
```python
Enter your name: Basistha
Hello, Basistha ! Welcome!
```
## How to Print Numbers in Python

The `input()` function can be used to take input from the user. When we need to work with numbers, we can convert the input to the desired numeric type using typecasting. Below, the input is converted to an integer using `int()`, and then the number is printed.

### Example: Taking Input as Integer

```python
# Taking input as int
# Typecasting to int
n = int(input("How many roses?: "))
print(n)
```
## Output:
```python
How many roses?: 8
8

```
## Find DataType of Input in Python

In Python, we can determine the type of an object using the `type()` function. The `type()` function returns the type of the variable or object passed to it.

### Example:

```python
a = "Hello World"
b = 10
c = 11.22
d = ("Geeks", "for", "Geeks")
e = ["Geeks", "for", "Geeks"]
f = {"Geeks": 1, "for": 2, "Geeks": 3}

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
print(type(f))
```
## Output:
```python
<class 'str'>
<class 'int'>
<class 'float'>
<class 'tuple'>
<class 'list'>
<class 'dict'>
```
