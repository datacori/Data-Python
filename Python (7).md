# Python Fundamentals Study (2025-12-14)
---
## Learning Goals (251216)

File input/output operations

Opening files using open()

Writing data to files

Closing files safely

Reading data from files

---
## Opening a File (open)

Use the open() function to open or create a file.

A file object is created using the syntax:

```python
myfile = open("python.txt", "w")
```

Clicking the file icon on the left panel allows you to verify that python.txt has been successfully created.

---

## Writing to a File (write)

Use the write() method to write content to a file

Syntax: file_object.write("string")

Data must be written as a string

```python
myfile = open("python.txt", "w")
myfile.write("data!")
myfile.close()
```
```text
data!
```
Always remember to close the file after writing to ensure that the data is safely stored.

---

## Reading a File (read)

Open a file in read mode ("r") to read its contents

Python provides multiple methods for reading files:

readline() : reads one line at a time

readlines() : reads all lines and returns them as a list

strip() : removes whitespace characters such as \n

---
### readline()
```python
myfile = open("Python.read.txt", "r")
line = myfile.readline()
print(line)
myfile.close()
```

### readlines()
```python
myfile = open("Python.read.txt", "r")
lines = myfile.readlines()
print(lines)
myfile.close()
```

### strip()
```python
myfile = open("Python.read.txt", "r")

for line in myfile.readlines():
    print(line.strip())

myfile.close()
```
---

## Example - Creating and reading a file with 3 lines
```python
myfile = ```open("Python.read.txt", "w")
myfile.write("data! \n programming \n funny")
myfile.close()
```
```text
data!
programming
funny
```
---

## Reading a file line by line - readline()

### open the file in read mode

read_file = open ("Python.read.txt", "r")

```python
text = read_file.readline()
print(text)
```
```text
data!
```
First line is returned

```python
text = read_file.readline()
print(text)
```
```text
programming
```
Second line is returned

---

## Reading files - readlines()
### Open a file in read mode

read_file = open("Python.read.txt", "r")

```python
all_text = read_file.readlines()
print(all_text)
```
```text
['data!\n', 'programming\n', 'funny']
```
---

## Using strip() to Remove Newline Characters

When reading a file line by line, each line usually ends with a newline character (\n). 

The strip() method removes leading and trailing whitespace, including newline characters.

```python
text_strip = read_file.readlines() . strip()
print(text_strip)
```
---

## Key Learnings

Improved understanding of file input/output operations

Practiced core file handling methods: open, write, close, read

---

## Reflections

Learned that files must be explicitly closed after use

Understood the difference between write mode and read mode, and why each is needed

Becoming more familiar with organizing learning content on GitHub

Keep going!

---

## Resources

Handbook_Python_Final.pdf

Fast Campus – Practical Python Data Analysis Without Failure

---

## Author

**RYU YEJIN**
Data Analysis Learning Journey 
From Python Basics to Real-World Projects
📧 Email: datacori00@gmail.com
Blog : https://blog.naver.com/datacori/224108640902

