# Python fundamentals study (2025-12-18)
---
## Learning Goals
- Practice `for` loops
- Practice `while` loops
- Practice writing functions and modularizing code

---

## For Loop

### Overview
A for loop is used when you want to repeat a specific block of code multiple times.  
It is commonly used to iterate over iterable objects such as lists, tuples, strings, or ranges.

### Syntax
```python
for variable in iterable:
    # code to execute repeatedly
```

### Example
```python
for i in range (5) :
   print("I love you")
```
```text
I love you
I love you
I love you
I love you
I love you
```
range(5) generates numbers from 0 to 4

---

## Iterating Over a String

### Overview
In Python, strings are iterable objects.  
This means you can use a for loop to access each character in a string one by one.

Strings can be defined using single quotes (`' '`), double quotes (`" "`), or triple quotes (`''' '''`).

### Example
```python
my_list = "Korea"

for char in my_list:
    print(char)
```
```text
K
o
r
e
a
```
Each character is processed sequentially from left to right

---

## Iterating Over a List

### Overview
A list is a data structure that can store multiple values, even of different data types.  
Each value inside a list is called an **element**, and its position is represented by an **index**.

### Example
```python
my_list = ["Korea", "USA", "Australia", "UK"]

for country in my_list:
    print(country)
```
```text
Korea
USA
Australia
UK
```
### Key concepts

- List: A data type that stores multiple values

- Element: An individual item inside a list

- Index: The position of an element within a list (starts from 0)

---

## Iterating Over a Dictionary

### Overview
A dictionary is a data structure that stores data in **key–value pairs**.  
Keys are used to access corresponding values, making dictionaries useful for structured and labeled data.

### Dictionary Creation
```python
my_dictionary = {
    "name": "Cori",
    "job": "data analyst"
}
```
### Example
```python
for key in my_dictionary:
    print(key, ":", my_dictionary[key])
```
```text
name : Cori
job : data analyst
```
### Key concepts

- Dictionary: A data type that stores data based on keys

- Key: Used to access values inside a dictionary

- Value: The data associated with each key

---

## Range-Based Iteration

### Overview
The `range()` function is commonly used to generate a sequence of numbers for iteration.  
It is often combined with `for` loops to repeat a block of code a specific number of times.

---

### Using the `range()` Function
```python
print(range(5))
```
```text
range(0, 5)
```
The range() function generates numbers starting from 0 up to (but not including) the given value.

---

### Converting 'range()' to a list
```python
print(list(range(5)))
print(list(range(5, 10)))
print(list(range(5, 10, 2)))
```
```text
[0, 1, 2, 3, 4]
[5, 6, 7, 8, 9]
[5, 7, 9]
```
---

### Iterating with 'for' and 'range()'
```python
for i in range(5):
    print(i)
```
```text
0
1
2
3
4
```
```python
for i in range(3, 20, 4):
    print(i)
```
```text
3
7
11
15
19
```
---

## While Loop

### Overview
A `while` loop repeatedly executes a block of code **as long as a condition is true**.  
Unlike a `for` loop, a `while` loop is typically used when the number of iterations is not fixed in advance.

---

### Example
```python
count = 0

while count < 5:
    print("count", count)
    count = count + 1
```
```text
count 0
count 1
count 2
count 3
count 4
```
### Notes

- while loops depend on a condition rather than a fixed sequence

- They are useful for condition-based repetition

- Careful condition control is essential to avoid infinite loops

---

## Break Statement

### Overview
The `break` keyword is used to **immediately exit a loop**, even if the loop condition is still true.  
It is commonly used to stop infinite loops or terminate a loop when a specific condition is met.

---

### Example
```python
a = 10
count = 0

while a > 3:
    count = count + 1
    a = a + 1

    if count > 20:
        break

    print("a =", a, "\tcount =", count)

print("The end")
```
```text
a = 11 	count = 1
a = 12 	count = 2
a = 13 	count = 3
a = 14 	count = 4
a = 15 	count = 5
a = 16 	count = 6
a = 17 	count = 7
a = 18 	count = 8
a = 19 	count = 9
a = 20 	count = 10
a = 21 	count = 11
a = 22 	count = 12
a = 23 	count = 13
a = 24 	count = 14
a = 25 	count = 15
a = 26 	count = 16
a = 27 	count = 17
a = 28 	count = 18
a = 29 	count = 19
a = 30 	count = 20
The end
```
---
## Continue Statement

### Overview
The `continue` keyword is used to **skip the current iteration** of a loop and move directly to the next iteration.  
It does not terminate the loop; it only skips the remaining code in the current cycle.

---

### Example
```python
num = 0

while num < 10:
    num = num + 1

    if num <= 5:
        continue

    print(num)
```
```text
6
7
8
9
10
```
---
## Key Learnings
- Gained a solid understanding of `for` loops and `while` loops
- Improved ability to write and structure functions
- Developed confidence in using loops to automate repetitive tasks

---

## Reflections
- Clearly understood the differences between `for` loops and `while` loops, especially the risk of infinite loops
- Applied various built-in functions within loops to reinforce learning
- Built solutions step by step, starting from simple logic
- Stay consistent and keep going 🚀

---

## Resources
- Handbook_Python_Final.pdf
- Fast Campus – Python Data Analysis from Basics to Practice

---

## Author

**RYU YEJIN**  

Aspiring Data Analyst  

Python Learning Journey from Basics to Practice  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224110534068


