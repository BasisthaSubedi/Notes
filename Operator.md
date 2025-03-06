# Operators in Python

Operators in Python are special symbols that perform operations on variables and values. They are used to manipulate data and variables in various ways, such as performing arithmetic calculations, comparing values, or combining multiple conditions.

### 1. **Types of Operators in Python**

Python supports several types of operators, which can be broadly categorized as follows:

- **Arithmetic Operators**
- **Comparison Operators**
- **Logical Operators**
- **Assignment Operators**
- **Bitwise Operators**
- **Membership Operators**
- **Identity Operators**

### 2. **Arithmetic Operators**

These operators are used to perform basic mathematical operations.

| Operator | Description  | Example  |
|----------|--------------|----------|
| `+`      | Addition     | `a + b`  |
| `-`      | Subtraction  | `a - b`  |
| `*`      | Multiplication | `a * b` |
| `/`      | Division     | `a / b`  |
| `//`     | Floor Division (returns integer) | `a // b` |
| `%`      | Modulus (remainder) | `a % b` |
| `**`     | Exponentiation | `a ** b` |

### Example:
```python
a = 10
b = 5
print(a + b)  # Output: 15
print(a - b)  # Output: 5
```

### 3. **Comparison Operators**

These operators are used to compare two values and return a boolean result (`True` or `False`).

| Operator | Description      | Example      |
|----------|------------------|--------------|
| `==`     | Equal to         | `a == b`     |
| `!=`     | Not equal to     | `a != b`     |
| `>`      | Greater than     | `a > b`      |
| `<`      | Less than        | `a < b`      |
| `>=`     | Greater than or equal to | `a >= b` |
| `<=`     | Less than or equal to    | `a <= b` |

### Example:
```python
a = 10
b = 5
print(a == b)  # Output: False
print(a > b)   # Output: True
```

### 4. **Logical Operators**

Logical operators are used to combine conditional statements.

| Operator | Description           | Example        |
|----------|-----------------------|----------------|
| `and`    | Returns True if both conditions are true | `a > b and b < 10` |
| `or`     | Returns True if either condition is true | `a > b or b > 10`  |
| `not`    | Reverses the result, returns True if the condition is false | `not(a > b)` |

### Example:
```python
a = 10
b = 5
print(a > b and b < 10)  # Output: True
```

### 5. **Assignment Operators**

Assignment operators are used to assign values to variables.

| Operator | Description  | Example   |
|----------|--------------|-----------|
| `=`      | Assign value | `a = 10`  |
| `+=`     | Add and assign | `a += 5` (equivalent to `a = a + 5`) |
| `-=`     | Subtract and assign | `a -= 3` (equivalent to `a = a - 3`) |
| `*=`     | Multiply and assign | `a *= 2` (equivalent to `a = a * 2`) |
| `/=`     | Divide and assign | `a /= 2` (equivalent to `a = a / 2`) |

### Example:
```python
a = 10
a += 5  # a = a + 5
print(a)  # Output: 15
```

### 6. **Bitwise Operators**

Bitwise operators perform bit-level operations on binary numbers.

| Operator | Description          | Example    |
|----------|----------------------|------------|
| `&`      | AND                  | `a & b`    |
| `|`      | OR                   | `a | b`    |
| `^`      | XOR (exclusive OR)   | `a ^ b`    |
| `~`      | NOT (inverts bits)   | `~a`       |
| `<<`     | Left shift           | `a << 2`   |
| `>>`     | Right shift          | `a >> 2`   |

### 7. **Membership Operators**

Membership operators are used to test if a value is found in a sequence (such as a list, tuple, or string).

| Operator | Description   | Example        |
|----------|---------------|----------------|
| `in`     | Returns True if a value is found in the sequence | `x in y`      |
| `not in` | Returns True if a value is not found in the sequence | `x not in y`  |

### Example:
```python
a = [1, 2, 3, 4]
print(3 in a)  # Output: True
print(5 not in a)  # Output: True
```

### 8. **Identity Operators**

Identity operators are used to compare the memory location of two objects.

| Operator | Description        | Example          |
|----------|--------------------|------------------|
| `is`     | Returns True if both variables point to the same object | `a is b`    |
| `is not` | Returns True if both variables do not point to the same object | `a is not b` |

### Example:
```python
a = [1, 2, 3]
b = a
print(a is b)  # Output: True
```
