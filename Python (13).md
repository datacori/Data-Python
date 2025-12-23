# Python Fundamentals study (2025-12-22)
---

## Learning Goals
- Understand different types of errors in Python
  - Syntax Errors
  - Runtime Errors
- Learn exception handling techniques
  - `try / except / else / finally`
- Practice writing functions and organizing code into modules

---

## Syntax Errors

A **syntax error** occurs **before the program is executed**.  
Since the program cannot run at all, syntax errors **cannot be handled using exception handling**.

- Occurs during code parsing
- Must be fixed by correcting the code itself
- Prevents the program from running

### Example

```python
print("Hello)
```
```text
SyntaxError: unterminated string literal
```
```python
print("Hello")
```
```text
Hello
```

Syntax errors should always be resolved by fixing the code structure, not by using try-except.

---

## Runtime Errors

A **runtime error** occurs **while the program is running**.  
Unlike syntax errors, runtime errors happen after the code has passed syntax checking and **can be handled using exception handling**.

- Occurs during program execution
- Can be prevented or handled using `try-except`
- Common examples: `IndexError`, `ZeroDivisionError`, `TypeError`

### Example: IndexError

```python
my_list = [1, 2, 3, 4]
my_list[7]
```
```text
IndexError: list index out of range
```
```python
my_list = [1, 2, 3, 4]
my_list[3]
```
```text
4
```

### Exception handling
Exception handling allows a program to continue running normally even when an error occurs.
- Prevents program crashes
- Improves program stability
- Makes error handling explicit and readable
Runtime errors can be safely managed using exception handling blocks such as try and except.

---

## try - except - else - finally Statement

The `try-except-else-finally` structure is used to **handle exceptions safely** while controlling program flow.

### Structure

```python
try:
    # Code that may raise an exception
except:
    # Code executed if an exception occurs
else:
    # Code executed if no exception occurs
finally:
    # Code that always executes, regardless of exceptions
```

## Explanation
- try : Contains code that may raise an error.
- except : Executes when an exception occurs in the try block
- else : Executes only if no exception occurs in the try block
- finally : Executes no matter what - whether an exception occurrred or not.            Commonly used for cleaup tasks

### Example - Invalid input (Exception occurs)
```python
try:
    number = int(input("Write number: "))
except:
    print("An error has occurred")
else:
    print("It is", number, "typed number")
finally:
    print("finally statement")
```
```text
Cori
```
```text
An error has occurred
finally statement
```

### Example - Valid input (No exception)
```python
try:
    number = int(input("Write number: "))
except:
    print("An error has occurred")
else:
    print("It is", number, "typed number")
finally:
    print("finally statement")
```
```text
3
```
```text
It is 3 typed number
finally statement
```
- else runs only when no exception occurs
- finally runs always
- This structure makes programs robust and predictable

---

## Key Learnings

- Understanding the difference between **syntax errors** and **runtime errors**
- Learning Python **exception handling** using `try - except - else - finally`

---

## Reflections

- Completed **Python Basics – Part 1**
- While coding, I encountered many errors and spent time identifying their causes.  
  This helped me revisit and better understand weak areas.
- The fundamentals are complete, and now it is time to move on to **practical applications**
- Keep going!

---

## Resources

- *Handbook_Python_Final.pdf*
- *Fast Campus – Python Data Analysis for Practical Work*

---

## Author

**RYU YEJIN**

Record of learning data analysis

from Python fundamentals to real-world projects  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224114599769
