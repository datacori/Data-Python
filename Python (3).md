## Python Fundamentals Study (2025-12-12)

# Learning Goals (2025-12-12)

- Python list data type
- Indexing and slicing
- Operators
- Modifying and deleting elements
- Practice with related functions and modules

---

## Python List

A **list** is a data structure that allows you to store and manage multiple values in a single variable.

- Lists can contain different data types
- Lists are ordered and mutable
- Elements are stored sequentially

---

## List Declaration

To create a list in Python, use square brackets `[]` and separate elements with commas.

- Each item inside a list is called an **element**

### Example

```python
my_list = [1, 3.5, 0, 'happy', [5, 6, [7, 8]]]
print(my_list)
```

Output

```text
[1, 3.5, 0, 'happy', [5, 6, [7, 8]]]
```

## Notes

A list can contain integers, floats, strings, and even other lists

Nested lists allow you to represent complex data structures

---

## Indexing

**Indexing** is an operation used to access a specific element inside a data structure such as a list or a string.

- Indexing starts from `0`
- You can access nested elements by chaining indexes

---

### Example List

```python
my_list = [1, 3.5, 0, 'happy', [5, 6, [7, 8]]]
```
---
## Accessing Elements by Index

1. Access the first element
```python
print(my_list[0])
```
```text
1
```
This prints the element at index 0
---

2. Access a nested list
```python
print(my_list[4][2])
```
```text
[7, 8]
```
---

3. Access a value inside a nested list
```python
print(my_list[4][2][0])
```
```text
7
```
---

## Notes

Indexing allows precise access to elements

Nested indexing is useful for working with complex data structures

---

## Slicing

**Slicing** is an operation used to extract a specific range of elements from a list or a string.

- Slicing uses the format `[start:end]`
- The `start` index is inclusive
- The `end` index is exclusive

---

### Example List

```python
my_list = [1, 3.5, 0, 'happy', [5, 6, [7, 8]]]
```

## Slicing a list
```python
print(my_list[2:4])
```
```text
[0, 'happy']
```
## Explanation

my_list[2:4] selects elements from index 2 up to (but not including) index 4
This returns the elements at index 2 and 3

---

## Notes

Slicing is commonly used for data extraction

It works on lists, strings, and other sequence types

Understanding slicing helps when processing subsets of data

---

## Indexing and Slicing (Combined Example)

This example demonstrates how **indexing and slicing** can be used together to access deeply nested elements in a list.

---

### Example List Structure

```python
my_list = [1, 5.2, 2*3, ['콜라', '벽', ['수박', '바닐라']]]
```
## Index reference:

my_list[3] → ['콜라', '벽', ['수박', '바닐라']]

my_list[3][2] → ['수박', '바닐라']

my_list[3][2][0] → '수박'

---

## Indexing + Slicing
```python
print(my_list[3][2][0][:2])
```
```text
수박
```
## Explanation

my_list[3] accesses the 4th element of the list

my_list[3][2] accesses the nested list

my_list[3][2][0] accesses the first string element

[:2] slices the first two characters of the string
---

## Notes

Indexing and slicing can be combined for precise data access

This approach is useful when working with nested and structured data

---


## List Operators

Python provides several operators and built-in functions for working with lists.

---

### Common List Operations

- `+` : Concatenates lists
- `*` : Repeats a list
- `len()` : Returns the number of elements in a list

---

### Example

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

print(list1 * 2 + list2)
print(len(list1 * 2 + list2))
```
## Output

```text
[1, 2, 3, 1, 2, 3, 4, 5, 6]
9
```

## Notes

List concatenation creates a new list

The len() function is commonly used to validate list size

These operations are frequently used in real-world data processing 

---

## Modifying and Deleting List Elements

Lists in Python are **mutable**, which means their elements can be changed or removed after creation.

---

### Example List

```python
my_list = [1, 5.2, 2*3, ['콜라', '벽', ['수박', '바닐라']]]
print(my_list)
```
```text
[1, 5.2, 6]
3
```

## Explanation

del removes the element at the specified index

After deletion, the list size decreases

---
## Notes
Lists allow in-place modification

Deleting elements changes both the content and length of a list

Careful index management is important when modifying lists

---

## Common List Methods

Python provides several built-in methods to manipulate and manage lists efficiently.

---

### Example List

```python
my_list = [1, 5, 4, 5, 8, 4]
```
---

## sort() — Sort the List
```python
my_list.sort()
print(my_list)
```
```text
[1, 4, 5, 5, 4, 8]
```
Sorts the list in ascending order in place

---
## reverse() — Reverse the List
```python
my_list.reverse()
print(my_list)
```
```text
[8, 5, 4, 5, 4, 1]
```
Reverses the order of elements in place

---
## append() — Add an Element
```python
my_list.append(6)
print(my_list)
```
```text
[8, 5, 4, 5, 4, 1, 6]
```

```python
my_list.append([7, 9])
print(my_list)
```
```text
[8, 5, 4, 5, 4, 1, 6, [7, 9]]
```

append() adds one element to the end of the list
(even if that element is another list)

---

## extend() - Extend the List
```python
my_list.extend([2, 3])
print(my_list)
```
```text
[8, 5, 4, 5, 4, 1, 6, [7, 9], 2, 3]
```

extend() adds each element of the iterable individually

---
## Notes

sort() and reverse() modify the original list

append() adds a single element

extend() expands the list with multiple elements

Understanding the difference between append() and extend() is essential

---

## Inserting and Removing Elements

Python lists provide several methods to insert and remove elements at specific positions.

---

### insert() — Insert an Element at a Specific Position

```python
my_list.insert(0, "number")
print(my_list)
```
```text
['number', 8, 5, 4, 5, 4, 1, 6, [7, 9], 2, 3]
```

## Explanation

insert(a, b) inserts element b at index a

Existing elements are shifted to the right

---

## remove() -  Remove an Element by Value
```python
my_list.remove(2)
print(my_list)
```
```text
['number', 8, 5, 4, 5, 4, 1, 6, [7, 9], 3]
```
## Explantion

Removes the first occurrence of the specified value

Raises an error if the value does not exist

---

## pop() - Remove and Return an Element

1. Remove the last element

```python
last_word = my_list.pop()
print(my_list)
print(last_word)
```

2. Remove an element at a specific index

```python 
last_word = my_list.pop(2)
print(my_list)
print(last_word)
```
```text
['number', 8, 5.4, 5, 4, 1, 6, [7, 9], 3]
['number', 8, 5.4, 5, 4, 1, 6, [7, 9]]
3
['number', 8, 5, 4, 1, 6, [7, 9]]
5.4
```

## Explantion

pop() removes and returns the last element

pop(index) removes and returns the element at the given index

Useful when you need both the removed value and the updated list

---
## Notes

insert() modifies the list in place

remove() works by value, not by index

pop() is commonly used in stack-like operations

---

## count() — Count Occurrences of an Element

The `count()` method returns the number of times a specific element appears in a list.

---

### Example

```python
print(my_list)
print(my_list.count(1))
```
```text
['number', 8, 5, 4, 1, 6, [7, 9]]
1
```
---
## Explanation

count(x) counts how many times x appears in the list

The method does not modify the original list

Useful for frequency checks and simple data analysis

---

## Notes

Works only for exact value matches

Commonly used in validation and preprocessing tasks

---

## Key Learnings
- Understanding the Python list data structure
- Improving problem-solving skills through hands-on practice

---

## Reflections
- Compared indexing and slicing between string and list data types
- Gained familiarity with using and organizing code on GitHub
- Found that documenting learning on both a blog and GitHub reinforced understanding
- No need to hesitate before trying — **keep going!**

---

## Resources
- *Handbook_Python_Final.pdf*
- *Fast Campus – Practical Python Data Analysis for Beginners*

---

## Author

**RYU YEJIN**  
Aspiring Data Analyst
Documenting Python fundamentals and real-world projects  

📧 Email: datacon00@gmail.com
Blog : https://blog.naver.com/datacori/224107074666
