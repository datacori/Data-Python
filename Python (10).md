# Python fundamentals study (2025-12-19)
---
## Learning Goals
- Understand functions in Python
- Learn how to use parameters
- Learn how to pass arguments to functions
- Understand return values

---

## Function Basics

### Overview
Functions are used to **organize reusable code** and perform repetitive tasks efficiently.  
They help improve code readability, modularity, and maintainability.

In Python, functions are defined using the `def` keyword.

---

### Basic Function Structure
```python
def function_name(parameters):
    # statement 1
    # statement 2
    return result
```

---
### Example
```python
def add(x, y):
    return x + y

z = add(3, 6)
print(z)
```
```text
9
```

- Functions help avoid code duplication

- Parameters allow functions to accept input values

- return provides output from a function

---

## Parameters

### Overview
A **parameter** is a variable that receives a value passed into a function.  
Parameters allow functions to work with different input values.

---

### Default Parameters
A **default parameter** is assigned a default value.  

If no argument is provided for that parameter, the default value is used automatically.

Default parameters must be placed **after** non-default parameters.

---

### Example
```python
def add(x, y=3):
    return x + y

z = add(3)
print(z)
```
```text
6
```

- Parameters receive input values in functions

- Default parameters simplify function calls

- Parameter order matters when using default values

---

## Variable-Length Parameters (`*args`)

### Overview
Variable-length parameters allow a function to accept **any number of arguments**.  
By placing an asterisk (`*`) before a parameter name, multiple arguments are collected into a tuple.

---

### Example
```python
def musical(*values):
    print("What is Cori's favorite musical?")

    for value in values:
        print(value)

musical("Hades Town", "Moulin Rouge", "Frankenstein", "Hedwig")
```
```text
What is Cori's favorite musical?
Hades Town
Moulin Rouge
Frankenstein
Hedwig
```

- `args` enables flexible function calls

- All arguments are stored as a tuple

- Commonly used in reusable and generic functions

---


---

## Keyword Arguments

### Overview
**Keyword arguments** allow values to be passed to a function by explicitly specifying parameter names.  
This makes function calls clearer and removes dependency on parameter order.

---

### Example
```python
def add(x=1, y=2, z=3):
    return x + y + z

result = add(y=5, z=5, x=2)
print(result)
```
```text
12
```

- Keyword arguments improve code readability

- They allow flexible and explicit function calls

- Especially useful when functions have many parameters

---

## Arguments

### Overview
**Arguments** are the actual values passed to a function when it is called.  
They are assigned to the function’s parameters during execution.

---

### Example
```python
def add(x, y):
    return x + y

result = add(3, 6)
print(result)
```
```text
9
```

- Arguments are inputs provided at function call time

- They are mapped to parameters in order (unless keyword arguments are used)

- Understanding this distinction is essential for writing clear functions

---

## Return

### Overview
The `return` statement sends a result value back to the place where the function was called.  
Once `return` is executed, the function immediately stops running.

---

### Returning a Single Value
```python
def return_test():
    return "Love"

value = return_test()
print(value)
```
```text
Love
```

---

### Returning Multiple Values
```python
def return_test():
    a = 3
    b = 4
    return a, b

value1, value2 = return_test()
print(value1)
print(value2)
```
```text
3
4
```

- `return` sends the result back to the function caller

- A function can return one or multiple values

- Code after return will not be executed

- Returning multiple values improves function flexibility

---

## Key Learnings
- Basic structure of Python functions
- Parameters (default, variable-length, keyword)
- Arguments
- Return values

---

## Reflections
- Learned how to define reusable logic using `def` and functions
- Realized that SQL concepts will require more practice alongside Python
- Consistently building and updating my GitHub portfolio
- Keep going!

---

## Resources
- Handbook_Python_Final.pdf
- Fast Campus – *Practical Python Data Analysis from Basics to Real-World Applications*

---

## Author

**RYU YEJIN**  

Data Analysis Learning Log 

From Python fundamentals to practical projects  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224111673652
