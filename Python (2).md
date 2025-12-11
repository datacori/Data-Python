## Python Strings — Study Notes (2025-12-11)

## Learning Goals

Understanding string data types

Working with escape characters

Indexing and slicing

String formatting

Practicing related string functions

---

🔤 String Data Type — Creating Strings
1. Creating a String with Double Quotes

```python
word = "hi"
print(word) 
# hi
```

2. Creating a String with Single Quotes
```python
   print('hi')
# hi
```

3. Using Single Quotes Inside Double Quotes
```python
print("I'm Korean")
# I'm Korean
```

4. Using Escape Characters (\) Inside Strings
```python
print('Cori는 \"데이터분석 프로그램\" 강의를 듣는다.')
# Cori는 "데이터분석 프로그램" 강의를 듣는다.
```

5. Creating Multiline Strings — Using """ or '''
```python
sentence = """
I want to eat
some pizza, chicken,
and hamburger.
"""

print(sentence)
```
```css
I want to eat
some pizza, chicken,
and hamburger.
```

6. Creating Multiline Strings Without Line Breaks — Using """\ or '''\
```python
sentence = """\
I want to eat
some pizza, chicken,
and hamburger.\
"""

print(sentence)
```
```css
I want to eat
some pizza, chicken,
and hamburger.
```

---
## String Type — Escape Characters in Python
Escape Characters (Using Backslash \)
Escape Code	Meaning
\n	New line
\t	Tab
\\	Backslash
\'	Single quote
\"	Double quote

Example Code
```python
sentence1 = "3\n5"
sentence2 = "6\t7"
sentence3 = "\"데이터\" 출력"
sentence4 = "\'분석\'출력"

print(sentence1)
print(sentence2)
print(sentence3)
print(sentence4)
```
```bash
3
5
6	7
"데이터" 출력
'분석'출력
```

---
## String Operators in Python

String Concatenation Operator (+)
```python
a = "Hi. "
b = "How are u?"
print(a + b)
```
```sql
Hi. How are u?
```

String Repetition Operator (*)
```python
equal = "=" * 30
sentence = equal + "\n Let's grab some coffee! \n" + equal
print(sentence)
```
```markdown
==============================
 Let's grab some coffee!
==============================
```
---

## String Indexing in Python


String indexing allows you to select a single character from a string using square brackets [].

Inside [], you specify the character position (index).

Index numbers start at 0 from the left.

Negative indexing starts at -1 from the right
---
Example: Variable Declaration
```python
# String Indexing Example
#  012 3 4567 8 910111213
#        -2 -1
sentence = '파이썬 단기간에 마무리!'
```

Accessing Characters

```python
# Forward index: starts from 0
# Reverse index: starts from -1

print(sentence)
print(sentence[0])   # forward index
print(sentence[-1])  # reverse index
```
```diff
파이썬 단기간에 마무리!
파
!
```
---
## String Slicing in Python

String slicing allows you to extract a specific range of characters from a string using the slice operator :.

Written as string[start:end]

Extracts characters from start index to end index - 1
---

Example
```python
print(sentence)
print(sentence[4:8])

# 파이썬 단기간에 마무리!
단기간에
```
---

## String Formatting in Python
Formatting with the % Operator

You can insert values into a string using the percent formatting operator %.

Format specifiers:

%d — integer

%f — float

%c — single character

%s - string

---

Example 1 — Insert an Integer
```python
sentence = "나는 %d호선을 타고 뮤지컬보러가." % 4
print(sentence)

#나는 4호선을 타고 뮤지컬보러가.
```

Example 2 — Insert Multiple Values
```python
a = 4
b = "공연장"
sentence = "나는 %d 호선을 타고 뮤지컬을 보러 %s에 가" % (a, b)
print(sentence)

#나는 4 호선을 타고 뮤지컬을 보러 공연장에 가
```
---

## String Formatting — format() Function
 Using the format() Function

Python’s format() function allows you to insert values into a string by placing {} placeholders inside the text.

## Key Points

Write {} inside the string, then call .format(value) after the string.

The number of {} placeholders must match the number of values passed into format().

You can use positional indexes like {0} to specify which argument goes where.

---

Example
```python
print("나는 {}호선을 타고 다녀.".format(1))
print("나는 {0}호선을 타고 다녀.".format(1))

# 나는 1호선을 타고 다녀.
# 나는 1호선을 타고 다녀.
```
---

## Useful String Functions in Python

## len(x) — Get String Length

Returns the number of characters in the string.
```python
sentence1 = "코리가 만든 트리가 반짝반짝 빛나"
print(len(sentence1))
# 18
```

## split() — Split a String

Splits the string into a list, using spaces as the default separator.
```python
print(sentence1.split())
```
```css
['코리가', '만든', '트리가', '반짝반짝', '빛나']
```

## count(x) — Count Occurrences

Counts how many times a specific substring appears in the string.
```python
print(sentence1.count('반짝'))
# 2
```

## replace(a, b) — Replace Substring

Replaces all occurrences of substring a with substring b.
```python
sentence2 = sentence1.replace('반짝반짝', '초롱초롱')
print(sentence1)
print(sentence2)

# 코리가 만든 트리가 반짝반짝 빛나
# 코리가 만든 트리가 초롱초롱 빛나
```

## find(a) — Find Position of a Substring

Returns the index of the first occurrence of the substring.
If not found, returns -1.
```python
file_name = 'London vlog.png'
print(file_name.find('.'))
print(file_name.split('.'))
```
```css
11
['London vlog', 'png']
```

## upper() — Convert to Uppercase

Converts all characters in the string to uppercase.
```python
print(file_name.upper())

# LONDON VLOG.PNG
```

## lower() — Convert to Lowercase

Converts all characters in the string to lowercase.
```python
print(file_name.lower())
# london vlog.png
```

join(x) — Insert a Separator Between Characters

Inserts a specified separator between each element of the string (or iterable).
```python
sentence = '.'.join('opqrstu')
print(sentence)

# o.p.q.r.s.t.u
```
---

# Key Learnings
- String data type
- Improved ability to write functions

---

# Reflections
- Day 2 of study: Became more familiar with using the `print()` function  
- Learned a bit about how to use GitHub  
- Still getting used to putting variables into functions  
- Never give up before trying! Keep going!  

---

# Resources
- Handbook_Python_Final.pdf  
- Fast Campus – Complete Python Data Analysis for Beginners  

---

# Author
**RYU YEJIN**  
Currently studying data analysis 
Recording progress from Python basics to real-world projects  
E-mail : datacori00@gmail.com

