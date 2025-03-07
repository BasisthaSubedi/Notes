# Data Types in Python

In Python, data types are used to define the type of a variable. A data type determines what kind of value a variable can hold, such as integers, strings, or floating-point numbers. Understanding data types is crucial because they determine the operations that can be performed on variables and the kind of data that can be stored.

### 1. **Basic Data Types in Python**

Python has several built-in data types that fall into different categories. Here are the most commonly used ones:

- **Numeric Types**
  - `int` (Integer): Whole numbers, both positive and negative.
  - `float` (Floating-Point): Decimal numbers.
  - `complex`: Complex numbers (real + imaginary).

- **Sequence Types**
  - `str` (String): A sequence of characters.
  - `list`: An ordered collection of items, which can be of different types.
  - `tuple`: An ordered, immutable collection of items.

- **Mapping Type**
  - `dict` (Dictionary): A collection of key-value pairs.

- **Set Types**
  - `set`: A collection of unique items.
  - `frozenset`: An immutable version of a set.

- **Boolean Type**
  - `bool`: Represents `True` or `False`.

- **Binary Types**
  - `bytes`: Immutable sequence of bytes.
  - `bytearray`: Mutable sequence of bytes.
  - `memoryview`: A memory view object.

### 2. **Numeric Data Types**

- **int**: Represents whole numbers without a fractional component.
  
  Example:
  ```python
  x = 10
  print(type(x))  # Output: <class 'int'>
  ```

- **float**: Represents decimal or floating-point numbers.
  
  Example:
  ```python
  y = 3.14
  print(type(y))  # Output: <class 'float'>
  ```

- **complex**: Represents complex numbers, which have a real and imaginary part.
  
  Example:
  ```python
  z = 1 + 2j
  print(type(z))  # Output: <class 'complex'>
  ```

### 3. **String (str)**

Strings are sequences of characters. They are enclosed in either single quotes (' ') or double quotes (" ").

Example:
```python
name = "Alice"
print(type(name))  # Output: <class 'str'>
```

### 4. **List (list)**

A list is an ordered, mutable collection that can hold items of different types. Lists are enclosed in square brackets `[]`.

Example:
```python
numbers = [1, 2, 3, 4]
print(type(numbers))  # Output: <class 'list'>
```

### 5. **Tuple (tuple)**

A tuple is similar to a list, but it is immutable, meaning you cannot change its values once it's created. Tuples are enclosed in parentheses `()`.

Example:
```python
coordinates = (10, 20)
print(type(coordinates))  # Output: <class 'tuple'>
```

### 6. **Dictionary (dict)**

A dictionary is a collection of key-value pairs. Keys are unique, and values can be of any type. Dictionaries are enclosed in curly braces `{}`.

Example:
```python
person = {"name": "Alice", "age": 25}
print(type(person))  # Output: <class 'dict'>
```

### 7. **Set (set)**

A set is an unordered collection of unique items. Sets are enclosed in curly braces `{}`.

Example:
```python
fruits = {"apple", "banana", "cherry"}
print(type(fruits))  # Output: <class 'set'>
```

### 8. **Frozen Set (frozenset)**

A frozenset is an immutable version of a set. Once created, you cannot change the elements of a frozenset.

Example:
```python
frozen_fruits = frozenset(["apple", "banana", "cherry"])
print(type(frozen_fruits))  # Output: <class 'frozenset'>
```

### 9. **Boolean (bool)**

A boolean data type has only two possible values: `True` or `False`. It is often used in conditional statements.

Example:
```python
is_active = True
print(type(is_active))  # Output: <class 'bool'>
```

### 10. **Type Conversion**

In Python, you can convert one data type to another using type casting. This is useful when you need to perform operations on different data types.

Example:
```python
x = "10"  # x is a string
y = int(x)  # Converting x to an integer
print(type(y))  # Output: <class 'int'>
```

### 11. **Checking Data Type**

You can check the type of a variable using the `type()` function.

Example:
```python
x = 10
print(type(x))  # Output: <class 'int'>
```