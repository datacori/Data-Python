# Python fundamenatals study (2025-12-20)
---

## Learning Goals
- Classes and Objects
- Object Instances
- Methods
- Constructors
- Inheritance

---

## Class

- A **design blueprint** used to create multiple objects with the same structure and behavior
- Defines attributes (data) and methods (functions) that the objects will share
- Helps organize code and improve reusability

---

## Object

- An **instance created from a class**
- Represents a concrete entity based on the class definition
- Each object can have different values for the same attributes

---

## Objects Created from a Class

- Each object has its **own unique characteristics**
- Objects created from the same class **do not affect each other**
- Each instance maintains its own state independently

---

## Class Definition

- A class is defined using the `class` keyword
- The class name is typically written in **CamelCase**
- The class body contains attributes and methods

### Syntax
```python
class ClassName:
    # class body
```

---

### Example
```python
class CannedFood:
    pass
```
The pass keyword is used as a placeholder when no attributes or methods are defined yet

---

## Instance

- An **object created based on a class**
- Each instance represents a concrete entity derived from the class definition
- Multiple instances can be created from the same class, and each instance is independent

### Syntax
```python
instance_name = ClassName()
```

---

### Example
```python
red_bean = CannedFood()
green_bean = CannedFood()
black_bean = CannedFood()
```
Although these instances are created from the same class, they exist as separate objects

---

## Method

- A **function defined inside a class**
- Represents behaviors or actions that objects of the class can perform
- The **first parameter of a method must be `self`**
- `self` refers to the instance that is calling the method

### Why `self`?
- When an object calls a method, the object itself is automatically passed as the first argument
- This allows the method to access and modify the instance’s attributes

---

## Method Definition

### Syntax
```python
class ClassName:
    def method_name(self, additional_parameters):
        pass
```
---

### Example
```python
class CannedFood:
    def set_info(self, color, taste):
        self.color = color
        self.taste = taste

    def print_info(self):
        print("==========")
        print("color :", self.color)
        print("taste :", self.taste)
        print("==========")
```
---

## Creating and Using an Object

### Step 1. Create an Object (Instance)
```python
black_bean = CannedFood()
```

### Step 2. Set Attributes Using a Method
```python
black_bean.set_info("black", "nutty")
```

### Step 3. Access Object Attributes
```python
print(black_bean.color)
print(black_bean.taste)
```
```text
black
nutty
```

### Step 4. Call an Instance Method
```python
black_bean.print_info()
```
```text
==========
color : black
taste : nutty
==========
```
---

## Constructor (`__init__`)

### What is a Constructor?
- A constructor is a special method that is **automatically executed when an instance is created**
- In Python, the constructor method is called `__init__`
- It initializes the object with required data at creation time

---

### Constructor Syntax
```python
class ClassName:
    def __init__(self, parameters):
        pass
```
- self refers to the instance being created
- Parameters allow passing initial values to the object

---

### Example: Defining a Constructor
```python
class CannedFood:
    def __init__(self, color, taste):
        self.color = color
        self.taste = taste
```

### Creating Multiple Objects with a Constructor
```python
beans = [
    CannedFood("red", "healthy"),
    CannedFood("green", "fresh"),
    CannedFood("black", "nutty")
]
```
- Objects are created with different values
- The constructor ensures consistent initialization

### Accessing Object Attributes
```python
print(beans[0].color)
print(beans[0].taste)
```
```text
red
healthy
```
- Objects stored in a list can be accessed by index
- Each instance maintains its own independent state

---

## Inheritance

### What is Inheritance?
- Inheritance allows a new class to **reuse and extend the functionality of an existing class**
- It helps reduce code duplication and improves code reusability
- A child class automatically inherits attributes and methods from its parent class

---

### Class Terminology
- **Parent Class** (Super Class): the class being inherited from
- **Child Class** (Sub Class): the class that inherits from another class

---

### Inheritance Syntax
```python
class ChildClass(ParentClass):
    pass
```
- The parent class name is passed inside parentheses
- The child class gains access to all public methods and attributes of the parent class

---

## Why Use Inheritance?
- Promotes code reuse
- Makes code easier to maintain and extend
- Represents real-world hierarchical relationships

---

### Multiple Inheritance
- A child class can inherit from multiple parent classes
- There is no limit to the number of parent classes

### Syntax
```python
class ChildClass(ParentClass1, ParentClass2):
    pass
```
- The child class inherits features from all specified parent classes
- Should be used carefully to avoid complexity and ambiguity

---

## Method Overriding

### What is Method Overriding?
- Method overriding means **redefining a method from a parent class in a child class**
- The child class provides its own implementation of a method that already exists in the parent class
- It allows child classes to customize or extend inherited behavior

---

### Parent Class Example
```python
class Bean:
    def __init__(self, color, taste):
        self.color = color
        self.taste = taste

    def print_info(self):
        print("parent class")
        print("good bean")
```

### Child Class Overriding the Methold
```python
class CannedFood(Bean):
    def print_info(self):
        print("child class")
        print("tasty bean")
        print("taste :", self.taste)
        print("color :", self.color)
```
- print_info() completely overrides the parent class methold
- The parent implementation is not executed

### Using super() in Method Overriding
```python
class TastyBean(Bean):
    def print_info(self):
        super().print_info()
        print("child class")
        print("lovely bean")
        print("taste :", self.taste)
        print("color :", self.color)
```
- super() calls the parent class method
- Allows reuse of parent logic while adding child-specific behavior

---

## Object Creation with Inheritance

This section demonstrates how **parent and child class objects behave differently**
when calling overridden methods.

---

### Creating a Parent Class Object
```python
red_bean = Bean("red", "healthy")
red_bean.print_info()
```
```text
parent class
good bean
```
- Calls the method defined in the parent class
- No method overriding involved

### Creating a Child Class Object (Overridden Method)
```python
green_bean = CannedFood("green", "fresh")
green_bean.print_info()
```
```text
child class
tasty bean
taste : fresh
color : green
```
- Child class overrides print_info()
- Parent method is not executed

### Creating a Child Class Object Using super()
```python
black_bean = TastyBean("black", "nutty")
black_bean.print_info()
```
```text
parent class
good bean
child class
lovely bean
taste : nutty
color : black
```
- super().print_info() executes the parent class methold
- Child class extends the behavior instead of replacing it

---

## Key Learnings

- Classes, Objects, and Instances
- Methods
- Constructors (`__init__`)
- Inheritance and Method Overriding

---

## Reflections

- I finally feel like I am starting Python properly from the class-based programming section.
- I got a bit confused during the method overriding part, but repeated practice helped.
- I should trust myself and keep moving forward.
- Keep going!

---

## Resources

- Handbook_Python_Final.pdf
- Fast Campus – *Python Data Analysis from Zero to Practice*

---

## Author

**RYU YEJIN**

Recording my journey in data analysis learning  

From Python fundamentals to real-world projects

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224112044141
