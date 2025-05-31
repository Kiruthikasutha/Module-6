# 🐍 Python OOP: Abstract Class & Method Example

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

## 💻 Program
```
class Beans:
    def type(self):
        print("Vegetable")
    def color(self):
        print("Green")

class Mango:
    def type(self):
        print("Fruit")
    def color(self):
        print("Yellow")

def func(obj):
    obj.type()
    obj.color()

bean = Beans()
mango = Mango()

func(bean)
func(mango)
```

## Output
![image](https://github.com/user-attachments/assets/d1c6cba6-f55b-4ea2-9bf6-44e92fd34944)

## Result
Thus,the program is executed sucessfully
# 🐍 Python OOP: Operator Overloading (Less Than `<`)

## 🎯 AIM

To write a Python program that demonstrates **operator overloading** by overloading the **less than (`<`)** operator using a custom class.

---

## 🧠 ALGORITHM

1. **Create Class `A`**:
   - Define the `__init__()` method to initialize the object with a value `a`.

2. **Overload the `<` Operator**:
   - Define the `__lt__()` method with logic:
     - If `self.a < o.a`, return `"ob1 is less than ob2"`
     - Else, return `"ob2 is less than ob1"`

3. **Create Objects**:
   - Instantiate two objects `ob1` and `ob2` with values.

4. **Use `<` Operator**:
   - Use `print(ob1 < ob2)` to trigger the overloaded behavior.

---

## 💻 Program
```
class A:
    def __init__(self, a):
        self.a = a

    def __lt__(self, o):
        if self.a < o.a:
            return "ob1 is less than ob2"
        else:
            return "ob2 is less than ob1"

ob1 = A(10)
ob2 = A(20)

print(ob1 < ob2)
```
## Output
![image](https://github.com/user-attachments/assets/ef8fb744-04b1-4749-b351-144a7d3619b6)


## Result
Thus,the program is executed successfully

# 🐍 Python OOP: Abstract Class & Method Example

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

## 💻 Program
```
from abc import ABC, abstractmethod
import math

class Shape(ABC):
    @abstractmethod
    def calculate_area(self):
        pass

class Rectangle(Shape):
    def __init__(self, length=1, breadth=1):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth

class Circle(Shape):
    def __init__(self, radius=1):
        self.radius = radius

    def calculate_area(self):
        return math.pi * self.radius * self.radius

rectangle = Rectangle(5, 3)
circle = Circle(4)

print("Rectangle Area:", rectangle.calculate_area())
print("Circle Area:", circle.calculate_area())
```
## Output
![image](https://github.com/user-attachments/assets/afe759ca-669b-4568-aa89-e5827d70455c)


## Result
Thus,the program is executed successfully

# 🐍 Python OOP: Encapsulation with Private Members

## 🎯 AIM

To implement **Encapsulation** in Python by defining a class `Rectangle` with **private member variables** `__length` and `__breadth`.

---

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

## 💻 Program
```
class Rectangle:
    def __init__(self, length, breadth):
        self.__length = length
        self.__breadth = breadth
        print("Length:", self.__length)
        print("Breadth:", self.__breadth)

rectangle = Rectangle(10, 5)
```
## Output
![image](https://github.com/user-attachments/assets/94950f1a-fefc-4aad-a525-f6cf1eb2f684)


## Result
Thus,the program is executed sucessfully

# 🐟 Method Overriding-Fish and Shark Class Inheritance in Python

## 🧠 AIM:
To write a Python program that demonstrates class inheritance by creating a parent class `Fish` with a method `type`, and a child class `Shark` that overrides the `type` method.

## 📋 ALGORITHM:

1. Define the `Fish` class with a method named `type()` that prints `"fish"`.
2. Define the `Shark` class as a subclass of `Fish`, and override the `type()` method to print `"shark"`.
3. Create an instance of the `Fish` class named `obj_goldfish`.
4. Create an instance of the `Shark` class named `obj_hammerhead`.
5. Use a `for` loop to iterate over both objects.
6. Within the loop, call the `type()` method using the loop variable.
7. Output will demonstrate method overriding: printing `"fish"` and `"shark"` accordingly.

## 💻 PROGRAM:
```
class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
    def type(self):
        print("shark")

obj_goldfish = Fish()
obj_hammerhead = Shark()

for fish in (obj_goldfish, obj_hammerhead):
    fish.type()
```
## OUTPUT
![image](https://github.com/user-attachments/assets/db88c4a8-8b86-4b05-b614-b209286090cd)


## RESULT
Thus,the program is executed sucessfully
