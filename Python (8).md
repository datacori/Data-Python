# Python fundamentals study (2025-12-17)
---
## Learning Goals 

Understand conditional logic in Python

Use if, elif, and else statements

Apply membership operators: in / not in

Learn the purpose of the pass keyword

Practice relational and logical operators

---
## if statement

A conditional statement executes code only when a condition evaluates to True.

If condition is False, the code block is skipped (or handled by else / elif)

### syntax
if condition :

    # code executed when condition is true

### Example - basic
```python
cori_study = True


if cori_study:
print("We can learn Python.")
```
```text
We can learn Python.
```

### Example - multiple statements
```python
caffeine = True


if caffeine:
print("green tea")
print("latte")
print("chocolate")
```
```text
green tea
latte
chocolate
```

Every if statement must be followed by a colon (:)

Indentation is mandatory in Python

Conditions typically evaluate to True or False

---
## else statement

The else statement is used after an if statement and runs when the if condition evaluates to False

### Syntax

if condition:

    # code executed when condition is True

else:

    # code executed when condition is False

### Example
```python
cori_study = False


if cori_study:
print("We can learn python")
else:
print("I don't know anything")
```
```text
I don't know anything
```
---

## elif statement

The elif statement is used to check multiple conditions sequentially. 

It allows you to handle more than two possible cases in a clean and readable way.

### Example
```python
score = "B"


if score == "A":
print("A class")
elif score == "B":
print("B class")
elif score == "C":
print("C class")
else:
print("D class")
```
```text
B class
```
---

## in / not in operators

The in and not in operators are used to a check specific value exists within a data structure such as string, list tuple, or set.

### Example -  Using not in with a string
```python
if "k" not in "data":
print(True)
else:
print(False)
```
```text
True
```
---

## pass keyword

The pass keyword is used as a placeholder when a statement is syntactically required but no action should be performed

### Example
```python
basket = ['blueberry', 'orange']


if 'butter' not in basket:
pass
```

The condition is checked, but no operation is executed

This prevents syntax errors while keeping the code structure intact.

---

## Relational operators
Relational operators are used to compare two values and determine whether the condition is True or False.

They are commonly used in conditional statements such as if, elif, and while

### Example
```python
a = 5
b = 3


print(a == b) # False
print(a != b) # True
print(a < b) # False
print(a > b) # True
print(a <= b) # False
print(a >= b) # True
```
---

## logical operators

Logical operators are used to combine or invert boolean values (True / False)
They are commonly used in conditional statements.

---
## not operator
The not operator reverses the boolean value of a condition.

```python
print(not True)
print(not False)
```
```text
False
True
```
---
## and operator
The and operator returns True only if all conditions are True

```python
print(True and True)
print(True and False)
print(False and True)
print(False and False)
```
```text
True
False
False
False
```
---
## or operator
The or operator returns False only when both conditions are False

In all other cases, it returns True

```python
print(True or True)
print(True or False)
print(False or True)
print(False or False)

```
```text
True
True
True
False
```
---
## Key Learning

Learned conditional statements (if / else / elif)

Practiced using operators and Python keywords

Improved problem-solving and function-writing skills

---

## Reflections

Writing conditional logic in Python feels a bit unfamiliar compared to Excel formulas, but it is easier to understand logically

Python is more fun than expected once I start practicing

I will keep studying consistently to reach my bootcamp goals

Keep going!

---

## Resources

Handbook_Python_Final.pdf

Fast Campus – Python Data Analysis for Beginners (Practical Guide)

---

## Author

**RYU YEJIN**

Aspiring Data Analyst

Documenting my journey from Python fundamentals to real-world data analysis projects

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224109677752
