# Tuples in Python

Tuples are another fundamental data structure in Python. They are similar to lists, but unlike lists, tuples are immutable, meaning their contents cannot be changed once they are created. Tuples are useful when you need a collection of items that should not be modified.

## 1. Creating Tuples

Tuples are created by placing elements inside parentheses (`()`), separated by commas. You can store any data type inside a tuple, including integers, strings, and even other tuples.

### Example:
```python
fruits = ("apple", "banana", "cherry")
numbers = (1, 2, 3, 4, 5)
mixed_tuple = ("apple", 2, 3.5, True)
```

For a tuple with a single element, a trailing comma is required.

### Example of Single-Element Tuple:
```python
single_element_tuple = (5,)
print(single_element_tuple)  # Output: (5)
```

## 2. Accessing Tuple Elements

Just like lists, tuples support indexing and negative indexing. You can access individual elements or slices of a tuple using indices.

### Example:
```python
fruits = ("apple", "banana", "cherry")
print(fruits[0])   # Output: apple
print(fruits[-1])  # Output: cherry (negative indexing)
```

## 3. Tuple Slicing

You can slice tuples to access a subset of elements. This is similar to how slicing works with lists.

### Example:
```python
numbers = (1, 2, 3, 4, 5, 6)
subtuple = numbers[1:4]  # Elements from index 1 to 3
print(subtuple)  # Output: (2, 3, 4)

# Slicing with step
step_slice = numbers[::2]  # Every second element
print(step_slice)  # Output: (1, 3, 5)
```

## 4. Modifying Tuples

Since tuples are immutable, you cannot modify their elements after creation. You cannot use operations like `.append()`, `.remove()`, or reassign individual elements.

### Example:
```python
# This will raise an error
fruits[1] = "orange"  # TypeError: 'tuple' object does not support item assignment
```

However, you can create a new tuple by concatenating or combining existing tuples.

### Example:
```python
fruits = ("apple", "banana", "cherry")
new_fruits = fruits + ("kiwi",)
print(new_fruits)  # Output: ('apple', 'banana', 'cherry', 'kiwi')
```

## 5. Tuple Methods

Although tuples are immutable, they do support two built-in methods:

- `.count()` - Counts how many times an element appears in the tuple
- `.index()` - Finds the index of the first occurrence of an element

### Example:
```python
numbers = (1, 2, 3, 1, 4, 1)
print(numbers.count(1))  # Output: 3
print(numbers.index(3))  # Output: 2
```

## 6. Tuple Packing and Unpacking

Tuples can be packed, meaning multiple values are assigned to a tuple, and unpacked, meaning a tuple can be decomposed into individual variables.

### Example of Packing:
```python
person = ("Alice", 30, "Engineer")  # Packing
```

### Example of Unpacking:
```python
name, age, profession = person  # Unpacking
print(name)      # Output: Alice
print(age)       # Output: 30
print(profession)  # Output: Engineer
```

