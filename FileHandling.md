# File Handling in Python: An Overview

File handling in Python refers to the process of reading from and writing to files. Python provides built-in functions and methods to perform various file operations such as opening, reading, writing, and closing files. With file handling, you can work with external data sources, manipulate files, and store information persistently.

Python makes file handling easy and efficient through its `open()` function, which returns a file object that can be used to perform operations on the file.

## File Handling Basics

In Python, files are handled through the **file object**, which is returned by the `open()` function. The basic syntax for opening a file is:

```python
file = open('filename', 'mode')
```

Where:
- `'filename'` is the name of the file to be opened (can include the full path).
- `'mode'` is the mode in which the file should be opened (read, write, append, etc.).

### File Modes
Here are the common modes used when opening files:
- `'r'`: Read mode (default). Opens the file for reading only. If the file does not exist, it raises a `FileNotFoundError`.
- `'w'`: Write mode. Opens the file for writing. If the file already exists, it truncates (empties) the file; if the file doesn’t exist, it creates a new one.
- `'a'`: Append mode. Opens the file for appending (writing at the end of the file). If the file doesn’t exist, it creates a new one.
- `'b'`: Binary mode. Opens the file in binary format (e.g., for reading images or non-text data).
- `'x'`: Exclusive creation mode. Creates a new file but fails if the file already exists.
- `'t'`: Text mode (default). Opens the file in text mode (usually used with `'r'`, `'w'`, `'a'`).

### Example of Opening a File

```python
# Open file in read mode
file = open("example.txt", "r")
```

## Reading Files

Once a file is opened in read mode (`'r'`), you can read its contents using various methods:

### 1. **`read()`** Method

The `read()` method reads the entire content of the file as a string.

```python
file = open("example.txt", "r")
content = file.read()  # Read the entire file content
print(content)
file.close()
```

### 2. **`readline()`** Method

The `readline()` method reads the file line by line and returns a string containing one line. It’s useful when working with large files that you don't want to load entirely into memory.

```python
file = open("example.txt", "r")
line = file.readline()  # Reads one line at a time
print(line)
file.close()
```

### 3. **`readlines()`** Method

The `readlines()` method reads the entire file and returns a list of lines.

```python
file = open("example.txt", "r")
lines = file.readlines()  # Returns a list of lines in the file
for line in lines:
    print(line.strip())  # .strip() removes the trailing newline character
file.close()
```

### Example: Read File in a `for` Loop

Instead of using `readlines()`, you can iterate over the file object itself, which will read the file line by line.

```python
with open("example.txt", "r") as file:
    for line in file:
        print(line.strip())
```

Here, the `with` statement ensures that the file is properly closed after the block is executed, even if an exception occurs.

## Writing to Files

To write to a file, the file must be opened in write (`'w'`), append (`'a'`), or exclusive creation (`'x'`) mode. If you use `'w'` mode, it will overwrite the file, while `'a'` will append data to the existing file.

### 1. **`write()`** Method

The `write()` method writes a string to the file. It does not add a newline by default.

```python
file = open("output.txt", "w")
file.write("Hello, world!\n")
file.write("Python is great.")
file.close()
```

### 2. **`writelines()`** Method

The `writelines()` method is used to write a list of strings to the file. Each string in the list is written consecutively.

```python
lines = ["Line 1\n", "Line 2\n", "Line 3\n"]
file = open("output.txt", "w")
file.writelines(lines)
file.close()
```

### Example: Writing to File Using `with`

Using the `with` statement ensures that the file is automatically closed after writing, which is a cleaner and safer way to handle file operations.

```python
with open("output.txt", "w") as file:
    file.write("This is a test.")
```

## File Closing

After you are done working with a file, it’s important to close it using the `close()` method. This ensures that any changes made to the file are saved, and system resources are freed up.

```python
file = open("example.txt", "r")
content = file.read()
file.close()  # Always close the file after operations
```

Alternatively, using the `with` statement automatically closes the file for you:

```python
with open("example.txt", "r") as file:
    content = file.read()
# The file is automatically closed here
```

## File Handling with `with` Statement

The `with` statement is the recommended way to handle files in Python. It ensures that the file is properly closed when the block inside the `with` statement is done executing, even if an error occurs.

```python
with open("example.txt", "r") as file:
    content = file.read()
# No need to manually close the file; it's automatically closed
```

### Why Use `with`?
- It automatically takes care of closing the file.
- It reduces the chance of file corruption or memory leaks due to forgetting to close the file.
- It’s more concise and easier to read.

## File Handling Modes: Read, Write, and Append

### Read Mode (`'r'`)

Used to read an existing file.

```python
with open("file.txt", "r") as file:
    content = file.read()
```

If the file does not exist, a `FileNotFoundError` will be raised.

### Write Mode (`'w'`)

Used to write to a file. It creates a new file if the file doesn’t exist and overwrites the file if it already exists.

```python
with open("file.txt", "w") as file:
    file.write("Hello, world!")
```

### Append Mode (`'a'`)

Used to append data to an existing file. It creates a new file if the file doesn’t exist.

```python
with open("file.txt", "a") as file:
    file.write("This will be appended.\n")
```

### Binary Mode (`'b'`)

Used to open a file in binary mode (e.g., for reading or writing non-text files like images or audio).

```python
with open("image.jpg", "rb") as file:
    content = file.read()
```

## File Operations: Moving, Renaming, Deleting

You can perform operations such as moving, renaming, or deleting files using the `os` and `shutil` modules.

### Example: Renaming a File

```python
import os
os.rename("old_file.txt", "new_file.txt")
```

### Example: Deleting a File

```python
import os
os.remove("file_to_delete.txt")
```

### Example: Moving a File

```python
import shutil
shutil.move("source.txt", "destination_folder/")
```

## Working with Directories

Python also provides methods for working with directories, like creating, removing, and listing files within a directory.

### Example: Create a Directory

```python
import os
os.mkdir("new_directory")
```

### Example: List Files in a Directory

```python
import os
files = os.listdir("directory_name")
print(files)
```