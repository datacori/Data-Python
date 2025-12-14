## Python Fundamentals Study (2025-12-13)

## Learning Goals 

- Tuple data type
  - Indexing, slicing, operators
  - Immutability (no modification or deletion)
- Dictionary data type
  - Declaration
  - Modifying and deleting elements
- Practice with related functions and modules

---

## Python Tuple

A **tuple** is a collection data type used to store multiple values.

- Tuples are created using parentheses `()`
- Tuples are **immutable**, meaning values cannot be added, removed, or changed after creation
- Tuples are useful for fixed data that should not be modified

---

## Creating Tuples

### Basic Tuple Creation

Tuples are created using parentheses and commas.

```python
my_tuple = (1, 2, 3)
```

---

## Tuple Creation Details

Tuples are defined using commas. Parentheses help readability, but the **comma is what actually creates a tuple**.

---

### Tuple vs Float

```python
tuple1 = (2, 3)
float1 = (2.3)

print(tuple1)
print(float1)

print(type(tuple1))
print(type(float1))
```

```text
(2, 3)
2.3
<class 'tuple'>
<class 'float'>
```

## Explanation

(2, 3) is a tuple containing two elements

(2.3) is interpreted as a float, not a tuple

The comma determines whether the value is treated as a tuple

---

## Single - Element Tuple

```python

single_tuple = (2,)
print(type(single_tuple))
```

```text
<class 'tuple'>
```
A trailing comma is required when creating a tuple with one element.


---

## Tuple Without Parentheses

In Python, tuples can be created **without parentheses** as long as elements are separated by commas.

---

### Example

```python
tuple2 = 1, 2, 3, 4, 5
print(tuple2)
print(type(tuple2))
```

```text
(1, 2, 3, 4, 5)
<class 'tuple'>
```

## Explanation

The comma , is what defines a tuple

Parentheses are optional but recommended for readability

This feature is commonly used in multiple assignment

---

## Notes

Tuples can be created implicitly

Using parentheses improves code clarity

Understanding this behavior helps avoid type-related bugs

---

## Tuple Indexing

**Indexing** is used to access a specific element in a tuple.

---

### Example

```python
tuple1 = (9, 8, 7, 6)
print(tuple1[0])
```
```text
9
```

## Explanation

Indexing starts at 0

The first element of the tuple is accessed using index 0

## Tuple Slicing

Slicing is used to extract a specific range of elements from a tuple.

## Example

```python
tuple2 = (5, 4, 3, 2)
print(tuple2[1:3])
```
```text
(4, 3)
```

## Explanation
tuple2[1:3] selects elements from index 1 to 2

The end index is not included

---
## Notes

Indexing and slicing work the same way as with lists

Tuples are immutable, but their elements can still be accessed

These operations do not modify the original tuple

---

## Tuple Operators

Tuples support several common operators similar to lists.

---

## Supported Operations

- `+` : Concatenate tuples
- `*` : Repeat a tuple
- `len()` : Get the number of elements in a tuple

---

### Example

```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)

print(tuple1 * 2 + tuple2)
print(len(tuple1 * 2 + tuple2))
```
```text
(1, 2, 3, 1, 2, 3, 4, 5, 6)
9
```
---

## Notes

Tuple operations create new tuples

Original tuples remain unchanged due to immutability

These operations are useful for combining fixed data

---

## Tuple Immutability (Modification and Deletion)

Tuples are **immutable**, which means their elements **cannot be modified or deleted** after creation.

Attempting to change or remove elements from a tuple will raise a `TypeError`.

---

## Attempting to Modify a Tuple

```python
tuple1 = (1, 2, 3, 4)
tuple1[0] = 3
```
```text
TypeError: 'tuple' object does not support item assignment
```

## Explanation

Tuples do not allow item assignment

This protects data from accidental modification

---

## Attempting to Delete a Tuple Element
```python
tuple2 = (1, 2, 3, 4)
del tuple2[0]
```
```text
TypeError: 'tuple' object does not support item deletion
```

## Explanation

Individual elements of a tuple cannot be deleted

Only the entire tuple can be deleted using del tuple2

---
## Notes

Tuples are designed for fixed, read-only data

Immutability improves data safety and performance

Use lists when frequent modification are required

---

## Python Dictionary

A **dictionary** is a data structure that stores data as **key–value pairs**.

- Each key is associated with a value
- Values are accessed using keys, not indexes
- Dictionaries are optimized for fast lookups

---

## Key Characteristics
- Keys must be unique
- Keys are typically strings or numbers
- Values can be of any data type

---

## Notes
- Dictionaries are useful for representing structured data
- They are commonly used in data processing and configuration handling

---

## Dictionary Declaration and Access

Dictionaries are created using curly braces `{}` with **key–value pairs**.

- Keys and values are connected using a colon `:`
- Keys are commonly strings

---

### Declaring a Dictionary

```python
my_dictionary = {
    "name": "Cori",
    "job": "data analyst"
}
```
---
## Accessing Values

Dictionary values are accessed using their keys.
```python
print(my_dictionary["name"])
print(my_dictionary["job"])
```
```text
Cori
data analyst
```
--- 
## Explanation

Each key maps to a specific value

Accessing a value by key returns the stored data

Using meaningful keys improves readability

---

## Notes

Accessing a non-existent key raises a KeyError


Dictionaries do not support index-based access


---

## Modifying and Deleting Dictionary Values

Unlike tuples, dictionaries are **mutable**, meaning their values can be changed or removed.

---

### Example Dictionary

```python
my_dictionary = {
    "name": "Cori",
    "job": "data analyst"
}
```
---
## Adding, Updating, and Deleting Dictionary Entries

Dictionaries allow dynamic updates by adding, modifying, or deleting key–value pairs.

---

## Adding a New Entry

```python
my_dictionary["grade"] = [92, 100, 98]
print(my_dictionary)
```
```text
{'name': 'Cori', 'job': 'data analyst', 'grade': [92, 100, 98]}
```

### Explanation

A new key–value pair is added using assignment

---

## Updating an Existing Entry
```python
my_dictionary["grade"] = [100, 96, 100]
print(my_dictionary)
```
```text
{'name': 'Cori', 'job': 'data analyst', 'grade': [100, 96, 100]}
```

### Explanation

Assigning a value to an existing key updates the stored value

The key remains unchanged

---

## Deleting an Entry
```python
del my_dictionary["grade"]
print(my_dictionary)
```
```text
{'name': 'Cori', 'job': 'data analyst'}
```

### Explanation

del removes the specified key and its value


The dictionary structure updates immediately


---

## Notes

Dictionaries are well-suited for structured and mutable data

Adding and updating entries use the same syntax


Care should be taken when deleting keys to avoid errors

---

## Dictionary Methods

Python dictionaries provide built-in methods to access keys, values, and key–value pairs efficiently.

---

## Example Dictionary

```python
my_dictionary = {
    "name": "Cori",
    "job": "data analyst",
    "grade": [100, 98, 95]
}

print(my_dictionary)
```
```text
{'name': 'Cori', 'job': 'data analyst', 'grade': [100, 98, 95]}
```

## keys() – Get All Keys
```python
print(my_dictionary.keys())
```
```text
dict_keys(['name', 'job', 'grade'])
```
---

## values() - Get All Values

```python
print(my_dictionary.values())
```
```text
dict_values(['Cori', 'data analyst', [100, 98, 95]])
```
---

## items() - Get Key-Value Pairs

```python
print(my_dictionary.items())
```
```text
dict_items([
    ('name', 'Cori'),
    ('job', 'data analyst'),
    ('grade', [100, 98, 95])
])
```
---

##  get() – Retrieve Value by Key

```python
print(my_dictionary.get('grade'))
print(my_dictionary.get('eat'))
```
```text
[100, 98, 95]
None
```
---

## in - Check if a Key Exists
```python
print('name' in my_dictionary)
print('eat' in my_dictionary)
```
```text
True
False
```
---

## clear() - Remove All Key-Value Pairs
```python
my_dictionary.clear()
print(my_dictionary)
```
```text
{}
```
---
## Notes

These methods allow structured access to dictionary contents
Especially useful for iteration and data inspection

---

## Key Learnings
- Learned tuple and dictionary data structures
- Improved ability to write and use built-in functions

---

## Reflections
- Tuples are similar to lists, but their values cannot be modified
- Successfully maintained a 3-day continuous study streak
- Learned how to organize and present code in a clean, readable format on GitHub
- Keep going!

---

## Resources
- *Handbook_Python_Final.pdf*
- Fast Campus – *Python Data Analysis from Basics to Practice*

---

## Author
**RYU YEJIN**  
Data Analysis Learning Journey 
Data Anlysis Learning Journey
From Python Basics to Practical Projects  
📧 Email: datacori00@gmail.com
Blog : https://blog.naver.com/datacori/224107416487



