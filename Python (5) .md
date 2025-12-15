# Python Fundamentals Study (2025-12-14)
---

## Learning Goals

Understand the Set data type

Understand the Boolean (bool) data type 

Practice writing functions and using modules

---

## Set Data Type (set)

A set is a built-in Python data type used to store multiple items in a single variable.

Key Characteristics of Sets

Created using the set keyword or curly braces {}

Duplicates are not allowed 

Unordered data structure (no index)

---

## Set Creation

### Creating a Set from a List

A set can be created by passing a list to the set() function.

Duplicate values are automatically removed.

```python
set1 = set([10, 20, 30])
print(set1)
print(type(set1))
```
```text
{10, 20, 30}
<class 'set'>
```
---

### Creating a Set from a String

When a string is passed to set(), each character becomes an element.

Duplicate characters are removed.

The order of elements is not preserved.

```python
set2 = set('hello')
print(set2)
print(type(set2))
```
```text
{'o', 'l', 'e', 'h'}
<class 'set'>
```
---
## Notes

Sets are unordered collections.
Sets do not allow duplicate elements.
Sets are useful for removing duplicates and membership testing.
---

## Set operations (Union, Intersection, Difference)

Set operations are useful for data comparison, filtering, and deduplication.

### Set Definition
```python
set1 = {1, 2, 3, 4, 5}
set2 = {1, 3, 5, 7, 9}
```
---
## Union (|)

Combines all unique elements from both sets.
```python
print(set1 | set2)
```
```text
{1, 2, 3, 4, 5, 7, 9}
```
---

## Intersection (&)

Returns elements that exist in both sets.
```python
print(set1 & set2)
```
```text
{3, 5, 7}
```
---
## Difference (-)

Returns elements that exist in one set but not in the other.

```python
print(set1 - set2)
print(set2 - set1)
```
```text
{2, 4}
{9, 7}
```
---
## Set Methods

### Set Initialization
```python
set1 = {1, 2, 3, 4, 5}
```
---

## add() — Add a Single Element

Adds one element to the set.
```python
set1. add(6)
print(set1)
```
```text
{1, 2, 3, 4, 5, 6}
```
---

## update() — Add Multiple Elements

Adds multiple elements to the set.

Accepts iterable objects such as lists, tuples, or sets.

```python
set1.update([6, 7])
print(set1)
```
```text
{1, 2, 3, 4, 5, 6, 7}
```
---

## remove() — Remove a Specific Element

Removes a specific element from the set.

Raises an error if the element does not exist.

```python
set1.remove(!)
print(set1)
```
```text
{2, 3, 4, 5, 6, 7}
```
---

## Boolean Data Type (bool)

The boolean data type represents True or False.

It is commonly used as the result of conditional expressions and comparisons.

---

## String Comparison
```python
"Cori" == "Cori"
```
```text
True
```
---

## Numeric Comparison
``` python
1<5
```
```text
True
```

```python
1>5
```
```text
False
```
---

## Conditional Evaluation (Truthy & Falsy)

In Python, values are automatically evaluated as True or False in conditional statements.

Empty values are evaluated as False.

Non-empty values are evaluated as True.

---

## Non-Empty String (Truthy)
```python
if "python" :
  print("True")
else :
  print("False")
```
```text
True
```
---
## Empty List (Falsy)
```python
if []:
    print("True")
else:
    print("False")
```
```text
False
```
---

## Boolean Evaluation of Numbers

In Python, integers are evaluated as boolean values in conditional statements.

1 is evaluated as True. 

0 is evaluated as False.

---
## Integer 1 (Truthy)
```python
Integer 1 (Truthy)
```
```text
True
```

## Integer 0 (Falsy)
```python
if 0:
    print("True")
else:
    print("False")
```
```text
False
```
---
## Notes

Any non-zero number is evaluated as True.
0 is the only integer value evaluated as False.
This behavior is commonly used in conditions and loop control.
---

## bool() Function

The bool() function converts a value into a boolean value.

It returns False if the value is empty.

It returns True if the value exists (is non-empty).

## Empty Value (Falsy)
```python
bool("")
```
```text
False
```

## Non-Empty Value (Truthy)
```python
bool([1, 2, 3])
```
```text
True
```

bool( ) is useful for explicitly checking truthy/falsy values.

---

## Key Learnings

Learned the characteristics of the set data type (no duplicate values).

Practiced using the boolean (bool) data type in conditional expressions.

---

## Reflections

Gained a clearer understanding of variables and basic data types.

Became more familiar with fundamental Python built-in functions.

Practiced logical thinking through boolean-based conditions.

Keep going!

---
## Resources

Handbook_Python_Final.pdf
Fast Campus - Python Data Anlysis Fundamentals without Failure

---
## Author

**RYU YEJIN**
Learning Data Analysis
From Python basics to practical projects
📧 Email: datacori00@gmail.com
Blog : https://blog.naver.com/datacori/224108412952


