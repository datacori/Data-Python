# Python Fundamentals study (2025-12-21)
---

## Learning Goals
- Internal modules: `import`, `from`, `as`
- External modules: `seaborn`
- Practice modularization and data visualization
- Creating modules and packages

---

## What is a Module?
- A module is a collection of variables and functions.
- It helps organize code into reusable components.

---

## Internal Modules
- Internal modules are modules that come pre-installed with Python.
- They can be used without additional installation.

---

## `import` Statement
- Used when importing an entire module.
- Syntax:
  ```python
  import module_name
```
```
Functions or variables inside the module are accessed using dot notation.

### Example
```python
import math

print(math.floor(1.2))
print(math.ceil(1.2))
```
```text
1
2
```
- floor() rounds a number down
- ceil() rounds a number up

---

## `from` Statement
- Used when you only need specific functions or variables from a module.
- This allows cleaner code without using the module name every time.

### Syntax
```python
from module_name import function1, function2
```

### Example
```python
from math import floor, ceil

print(floor(1.2))
print(ceil(1.2))
```
```text
1
2
```

### Importing all objects
- To import everything from a module, use `*`
- This is generally not recommended because it can cause name conflicts
```python
from module_name import *
```
---

## `as` Statement
- Used to assign an alias to a module
- Helps shorten long module names and improve readability

### Example
```python
import math as m

print(m.floor(1.2))
print(m.ceil(1.2))
```
```text
1
2
```
math is now referenced as m
Commonly used in data anlysis libraries

---

## External Modules
- External modules are **not included by default in Python**.
- They are created and distributed by third parties.
- Most data analysis and visualization libraries fall into this category.

---

## Seaborn Module
- Seaborn is a **data visualization library** built on top of Matplotlib.
- It provides a **high-level interface** for creating attractive and informative statistical graphics.

---

### Installing Seaborn
- Seaborn must be installed as a package before use.

```bash
pip install seaborn
```
 ### Importing Seaborn
 - Commonly imported using an alias for convenience

```python
import seaborn as sns
```

### Loading Sample Datasets
- Seaborn provides built-in datasets for practice and visualization
- Use the load_dataset() function to load them

```python
titanic = sns.load_dataset("titanic")
```
## Data Exploration

### Previewing the Data
- Use the `head()` function to quickly inspect the dataset.
- By default, it displays the **first 5 rows**.

```python
titanic.head()
```

### Dataset Overview
- Use the info() function to check the overall structure of the dataset
- Key information provided :
   - Number of rows and columns
   - Column names
   - Non-null counts
   - Data types
   - Memory usage
 
---

### Observations
- The Titanic dataset contains 891 rows and 15 columns.

- Some columns (e.g. age, deck) contain missing values.

---

## Data Visualization

### Swarm Plot
- `swarmplot()` visualizes data points while preventing overlap.
- It is useful for **exploratory data analysis (EDA)** when comparing distributions.

#### Key Parameters
- `x` : Categorical variable (e.g. passenger class)
- `y` : Numerical variable (e.g. age)
- `data` : Dataset to visualize
- `hue` : Additional categorical variable for grouping (e.g. sex)

```python
sns.swarmplot(
    x='class',
    y='age',
    data=titanic,
    hue='sex'
)
```
### Interpretation
- Each dot represents an individual passenger
- Passenger age distrubution differs by class
- Gender-based differences can be observed within each class
- Swarm plots help identify : Distribution patterns / Density differences / Outliers

---

## Creating Custom Modules

### Module Structure
- A module is created by organizing Python files inside a folder.
- This improves code reusability and project structure.

module_folder/
├── main.py
└── module1.py


---

### Defining a Module
- Functions are defined inside a `.py` file.
- Example: `module1.py`

```python
def add(x, y, z):
    return x + y + z
```

### Using the Module
- Import the custom module into another Python file
- Example : main.py

```python
import module1

result = module1.add(1, 2, 3)
print(result)
```

### Executing the Script
- Run the main file from a notebook or terminal
```python
!python /content/module_folder/main.py
```
```text
6
```
- Custom modules help organize code logically
- Functions defined in one file can be reused across multiple files
- Proper module structure improves readability and maintainability

---

## Packages

### What is a Package?
- A package is a collection of related modules organized into a directory.
- Packages help manage large Python projects by structuring modules logically.

---

### Why Use Packages?
- Improve code organization and readability
- Enable scalable project structure
- Allow easy import and reuse of modules

---

### Package Structure Example
- A package is typically a folder containing multiple modules.
- The folder can be treated as a package when used with imports.

my_package/
├── init.py
├── module1.py
└── module2.py

---

## Key Learnings
- Understanding internal and external Python modules
- Data visualization using the seaborn library
- Creating custom modules and adding executable code

---

## Reflections
- Learned how to visualize data within 12 days of starting Python
- Data visualization feels challenging but very interesting
- Started following SQL lectures in parallel
- Keep going!

---

## Resources
- Handbook_Python_Final.pdf
- Fast Campus: *Python Data Analysis for Complete Beginners*

---

## Author
**RYU YEJIN**  

Aspiring Data Analyst  

Documenting Python fundamentals to practical projects  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224113334247
