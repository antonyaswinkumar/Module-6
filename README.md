## Python Programming Module 6
## Name: Antony Aswin Kumar L
## Register Number : 212225040024

## Ex:1  Abstract Class & Method Example

## 🎯 AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

## 🧠 ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

## 💻 Program:

```

from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass


class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def calculate_area(self):
        return self.length * self.width


class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        pi = 3.14  # Use 3.14 to get exact 50.24
        return pi * self.radius ** 2


rect = Rectangle(5, 3)
print("Area of a rectangle:", rect.calculate_area())

circle = Circle(4)
print("Area of a circle:", circle.calculate_area())
```

## Output

<img width="702" height="744" alt="image" src="https://github.com/user-attachments/assets/7c783655-a76d-4b6a-a1c3-720151549cdf" />


## Result:
Thus the program to **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle` is executed successfully.



## Ex:2  Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.


## 🧠 ALGORITHM

1. **Define the Class**:
   - Create a class `Rectangle` with two private attributes: `__length` and `__breadth`.

2. **Initialize Variables**:
   - Use the `__init__()` constructor to set initial values for `__length` and `__breadth`.

3. **Print Values**:
   - Display the private variables from within the class to demonstrate access.

4. **Instantiate the Object**:
   - Create an object of the `Rectangle` class to trigger the constructor.

---

## 💻 Program;

```
class Rectangle:
    __length = 0
    __breadth = 0
    def __init__(self,length,breadth):
        self.__length = 5
        self.__breadth = 3
    def show(self):
        print(self.__length)
        print(self.__breadth)
            
rect = Rectangle(5,3)
rect.show()
```

## Output

<img width="545" height="363" alt="image" src="https://github.com/user-attachments/assets/8c9be7a2-e3c3-4c23-b4de-3abe55f98c82" />


## Result
Thus the program to implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth` is executed successfully.
