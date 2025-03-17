# Polymorphism in Python: An Overview

Polymorphism is one of the key principles of Object-Oriented Programming (OOP). It allows objects of different classes to be treated as objects of a common superclass. The term "polymorphism" comes from Greek, meaning "many shapes." In Python, polymorphism is typically achieved through method overriding and duck typing.

## What is Polymorphism?

Polymorphism allows for methods to behave differently based on the object that is calling them. In simpler terms, polymorphism allows the same method to work with objects of different types.

### Types of Polymorphism in Python

There are two types of polymorphism commonly used in Python:
1. **Method Overriding**: When a subclass provides its specific implementation of a method that is already defined in its superclass.
2. **Duck Typing**: Python’s dynamic nature allows objects to be used interchangeably if they implement the same methods, even if they don't share a common superclass.

## Method Overriding

Method overriding is a core feature of polymorphism in object-oriented programming. It allows a subclass to provide a specific implementation of a method that is already defined in its superclass. This ensures that the subclass can modify or extend the behavior of the inherited method.

### Example: Method Overriding

```python
class Animal:
    def speak(self):
        print("Animal speaks")

class Dog(Animal):
    def speak(self):
        print("Woof! Woof!")

class Cat(Animal):
    def speak(self):
        print("Meow!")

# Creating instances of Dog and Cat
dog = Dog()
cat = Cat()

# Calling the overridden method
dog.speak()  # Outputs: Woof! Woof!
cat.speak()  # Outputs: Meow!
```

In this example, both `Dog` and `Cat` override the `speak` method of the `Animal` class. Even though both `Dog` and `Cat` are instances of the `Animal` class, each has a different implementation of the `speak` method.

### Key Points:
- **Override**: The subclass method provides its own implementation of a method defined in the superclass.
- **Dynamic Dispatch**: When a method is called on an object, Python dynamically chooses the correct method to call based on the object's class.

## Duck Typing

Python uses a concept called **duck typing**, where the focus is on whether an object can perform the required behavior rather than its class or inheritance. In duck typing, if an object can respond to a method or attribute (even if it’s not a subclass of the expected class), it can be treated as if it is an instance of the expected type.

The name "duck typing" comes from the phrase: "If it looks like a duck, swims like a duck, and quacks like a duck, it probably is a duck."

### Example: Duck Typing

```python
class Dog:
    def speak(self):
        print("Woof!")

class Cat:
    def speak(self):
        print("Meow!")

class Bird:
    def speak(self):
        print("Chirp!")

def make_animal_speak(animal):
    animal.speak()  # Calling the 'speak' method on any object

# Objects of different classes
dog = Dog()
cat = Cat()
bird = Bird()

# Passing objects of different classes to the same function
make_animal_speak(dog)   # Outputs: Woof!
make_animal_speak(cat)   # Outputs: Meow!
make_animal_speak(bird)  # Outputs: Chirp!
```

Here, the `make_animal_speak()` function accepts any object that has a `speak` method. Even though `Dog`, `Cat`, and `Bird` are different classes, they all have a `speak()` method, so they can be passed into the same function. This is an example of duck typing in action.

### Key Points:
- **Behavior over Class**: The type of object doesn’t matter as long as it implements the required method.
- **Flexible**: Duck typing allows for a more flexible, less rigid system because we don't need to worry about object inheritance or explicit type checks.

## Polymorphism with Inheritance and Interfaces

Polymorphism is often used in combination with inheritance and interfaces. In Python, we don't have interfaces in the traditional sense (like Java or C#), but we can achieve similar behavior using abstract base classes.

### Example: Polymorphism with Inheritance

```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

# Polymorphic behavior
def print_area(shape):
    print(f"Area: {shape.area()}")

# Creating instances
circle = Circle(5)
rectangle = Rectangle(4, 6)

# Passing different types of objects to the same function
print_area(circle)      # Outputs: Area: 78.5
print_area(rectangle)   # Outputs: Area: 24
```

In the above code, we define an abstract base class `Shape` with an abstract method `area()`. Both `Circle` and `Rectangle` inherit from `Shape` and implement their own versions of the `area()` method. The `print_area()` function demonstrates polymorphism because it can handle both `Circle` and `Rectangle` objects, despite their differences.

### Key Points:
- **Abstract Base Class**: Used to define common interfaces that must be implemented by subclasses.
- **Polymorphism in Action**: Different classes can implement the same interface and be used interchangeably in polymorphic functions.

## Benefits of Polymorphism

1. **Code Reusability**: You can write functions or methods that work with objects of multiple types, reducing code duplication.
2. **Flexibility**: Code that uses polymorphism can easily work with new types of objects, as long as they implement the required methods.
3. **Extensibility**: Polymorphism allows you to extend the functionality of a program easily by adding new classes without modifying existing code.
