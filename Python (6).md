# Python Fundamentals – Daily Study Log (251215)
---
## Learning Goals

Practice user input using the input() function

Learn output formatting with print()

Improve function writing and modularization skills

---

## User Input (input())

The input( ) function is used to receive input from the user.
The text inside the parentheses is displayed as a prompt message.
The function returns the user input as a string.

### Example
```python
input("Write your name : ")
```
```text
Write your name : Cori
Cori
```
---
All values returned by input() are of type str.
To use numeric input, type conversion is required. - int(), float()

---
## Variable Assignment with input()

The value returned by input() can be assigned to a variable.
Regardless of what the user enters, the returned value is always a string(str).

### Assigning user input to a variable
```python
name =input("Write your name: ")
print(type(name))
```
```text
Write your name: Cori
<class 'str'>
```

### Numeric input is still a string
```python
number = input("Write your favorite number: ")
print(type(number))
```
```text
Write your favorite number: 1
<class 'str'>
```
---
str stands for sting data type.
Even if a number is entered, input() returns a string
Type conversion is required to use numeric values. - int(number)

---

## Type conversion : String to number

Values returned by input() are always of type str.
To perform numeric calculations, type conversion is required.
int() converts a sting to an integer.
float() converts a string to a floating-point number.

### String vs Integer Addition
```python
string1 = input("1 type: ")
int1 = int(string1)

string2 = input("2 type: ")
int2 = int(string2)

# String concatenation (not numeric addition)
print(string1 + string2)

# Integer addition (numeric calculation)
print(int1 + int2)
```
```text
1 type: 1
2 type: 2
12
3
```
---
string1 + string2 performs string concatenation, resulting in 12.
int1 + int2 performs numeric addition, resulting in 3.
Proper type conversion is essential when working with user input.

---

## Converting numbers to strings

The str() function is used to convert numeric values into strings.
This conversion is useful when combining numbers with text or formatting output.

### Example : integer to string conversion
```python
int1 = 123
print(int1)
print(type(int1))

str1 = str(int1)
print(str1)
print(type(str1))
```
```text
123
<class 'int'>
123
<class 'str'>
```

int 1 is an integer value. 
After applying str(), the value remains visually the same, but its data type changes from int to str.
This allows the value to be used in string concatenation or text-based output.

---
## Output with print()

The print() function is used to display output to the console.
Strings enclosed in quotation marks "" placed next to each other behave the same as using the + operator.

### Example: String concatenation
```python
print("eat""sleep""life")
print("eat" + "sleep" + "life")
```
```text
eatsleeplife
eatsleeplife
```

Both methods produce the same result.

---
## Using commas in print()

Commas are used to separate values and automaticall insert spaces between them.

### Example : Printing with commas
```python
print("eat", "sleep", "life")
```
```text
eat sleep life
```
--- 
## Key differences
```text
"a""b""c" -> abc
"a"+"b"+"C" -> abc
"a", "b", "c" -> a b c
```
---

## Key Learnings

User input handling with input()

Output formatting using print()

---
## Reflections

When errors occur while assigning user input to variables or writing functions, I am practicing the habit of reviewing the code carefully from the beginning.

I now have a much clearer understanding of how the print() function works.

I am becoming more familiar and comfortable with Google Colab.

Keep going!

---

## Resources

Handbook_Python_Final.pdf

Fast Campus – Python Data Analysis for Beginners (Practice-Oriented)

---

## Author

**RYU YEJIN**
Learning Data Analysis 
Recording my journey from Python basics to real-world projects
📧 Email: datacori00@gmail.com
Blog : https://blog.naver.com/datacori/224108597681
