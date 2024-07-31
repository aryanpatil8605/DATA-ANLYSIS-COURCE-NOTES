# DATA ANALYSIS COURCE NOTES

---

## Python Basics

### Introduction to Python for Data Analytics
Python is a powerful, versatile programming language widely used in data analytics due to its simplicity and the vast array of libraries available for data manipulation and visualization, such as Pandas, NumPy, and Matplotlib.

### Python Installation in Windows
1. Download the Python installer from the official Python website (https://www.python.org/).
2. Run the installer and follow the instructions. Ensure to check "Add Python to PATH" during installation.
3. Verify installation by opening Command Prompt and typing:
   ```bash
   python --version
   ```

### Python IDE (Pycharm)
PyCharm is a popular IDE for Python. To install:
1. Download PyCharm from the official JetBrains website (https://www.jetbrains.com/pycharm/).
2. Run the installer and follow the instructions.
3. Create a new project and start coding.

### First Program in Python
Open your IDE or a text editor, write the following code, and save it as `hello.py`:
```python
print("Hello, World!")
```
Run the script by typing `python hello.py` in the terminal.

### Comments, Variables, Datatypes, User-Inputs
- **Comments**: 
  ```python
  # This is a single-line comment
  ```
- **Variables**: 
  ```python
  name = "Alice"
  age = 25
  ```
- **Datatypes**: 
  ```python
  integer_var = 10  # int
  float_var = 10.5  # float
  string_var = "Hello"  # str
  ```
- **User-Inputs**:
  ```python
  name = input("Enter your name: ")
  print("Hello, " + name)
  ```

### TypeCasting, Subtypes, Problem-Solving
- **TypeCasting**:
  ```python
  x = int("10")
  y = float("10.5")
  z = str(123)
  ```
- **Subtypes**:
  Subtypes refer to types derived from primary types, such as lists, tuples, dictionaries, etc.
  ```python
  lst = [1, 2, 3]  # list
  tpl = (1, 2, 3)  # tuple
  dct = {"one": 1, "two": 2}  # dictionary
  ```

### Operators and Operands
- **Arithmetic Operators**:
  ```python
  a = 10
  b = 5
  print(a + b)  # Addition
  print(a - b)  # Subtraction
  print(a * b)  # Multiplication
  print(a / b)  # Division
  print(a % b)  # Modulus
  ```
- **Comparison Operators**:
  ```python
  print(a == b)  # Equal to
  print(a != b)  # Not equal to
  print(a > b)   # Greater than
  print(a < b)   # Less than
  print(a >= b)  # Greater than or equal to
  print(a <= b)  # Less than or equal to
  ```

### Conditional Statements
- **If-Else**:
  ```python
  age = 18
  if age >= 18:
      print("Adult")
  else:
      print("Minor")
  ```
- **Elif**:
  ```python
  marks = 85
  if marks >= 90:
      print("Grade A")
  elif marks >= 75:
      print("Grade B")
  else:
      print("Grade C")
  ```

---

## Python - Loops and Lists

### Introduction to Loops
Loops are used to execute a block of code repeatedly.

### For Loop, While Loop, Nested Loops
- **For Loop**:
  ```python
  for i in range(5):
      print(i)
  ```
- **While Loop**:
  ```python
  count = 0
  while count < 5:
      print(count)
      count += 1
  ```
- **Nested Loops**:
  ```python
  for i in range(3):
      for j in range(2):
          print(i, j)
  ```

### For Loop with Conditional Statements
```python
for i in range(10):
    if i % 2 == 0:
        print(i, "is even")
    else:
        print(i, "is odd")
```

### Break and Continue Statement
- **Break**:
  ```python
  for i in range(10):
      if i == 5:
          break
      print(i)
  ```
- **Continue**:
  ```python
  for i in range(10):
      if i % 2 == 0:
          continue
      print(i)
  ```

### Loops Problem Solving
**Example**: Print all prime numbers up to 20.
```python
for num in range(2, 21):
    is_prime = True
    for i in range(2, num):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        print(num)
```

### Introduction to Lists
Lists are ordered collections of items.
```python
fruits = ["apple", "banana", "cherry"]
print(fruits)
```

### Lists Slicing, Iteration, Functions
- **Slicing**:

 ```python
# Given list
my_list = [10, 20, 30, 40, 50, 60, 70]

# Slice from index 1 to 4
print(my_list[1:5])  # Output: [20, 30, 40, 50]

# Slice from beginning to index 3
print(my_list[:4])  # Output: [10, 20, 30, 40]

# Slice from index 3 to end
print(my_list[3:])  # Output: [40, 50, 60, 70]

# Slice with step 2
print(my_list[::2])  # Output: [10, 30, 50, 70]

# Reverse the list
print(my_list[::-1])  # Output: [70, 60, 50, 40, 30, 20, 10]
  ```

- **Iteration**:

  ```python
  for fruit in fruits:
      print(fruit)
  ```
  
- **Functions**:
Common List Functions and Methods
1. len(list): Returns the number of items in the list.
2. max(list): Returns the largest item in the list.
3. min(list): Returns the smallest item in the list.
4. sum(list): Returns the sum of all items in the list.
5. list.append(x): Adds an item x to the end of the list.
6. list.insert(i, x): Inserts an item x at position i.
7. list.remove(x): Removes the first occurrence of x from the list.
8. list.pop([i]): Removes and returns the item at position i (default is the last item).
9. list.sort(): Sorts the items of the list in place.
10. list.reverse(): Reverses the elements of the list in place.
11. list.index(x): Returns the index of the first occurrence of x in the list.
12. list.count(x): Returns the number of occurrences of x in the list.
13. list.clear(): Removes all items from the list.
14. list.extend(iterable): Extends the list by appending all items from the iterable.

 ```python
# List operations
my_list = [1, 2, 3, 4, 5]

# Length of the list
print(len(my_list))  # Output: 5

# Maximum value in the list
print(max(my_list))  # Output: 5

# Minimum value in the list
print(min(my_list))  # Output: 1

# Sum of all items in the list
print(sum(my_list))  # Output: 15

# Append an item to the list
my_list.append(6)
print(my_list)  # Output: [1, 2, 3, 4, 5, 6]

# Insert an item at a specific position
my_list.insert(0, 0)
print(my_list)  # Output: [0, 1, 2, 3, 4, 5, 6]

# Remove an item from the list
my_list.remove(3)
print(my_list)  # Output: [0, 1, 2, 4, 5, 6]

# Pop an item from the list
popped_item = my_list.pop()
print(popped_item)  # Output: 6
print(my_list)      # Output: [0, 1, 2, 4, 5]

# Sort the list
my_list.sort()
print(my_list)  # Output: [0, 1, 2, 4, 5]

# Reverse the list
my_list.reverse()
print(my_list)  # Output: [5, 4, 2, 1, 0]

# Index of an item
print(my_list.index(4))  # Output: 1

# Count occurrences of an item
print(my_list.count(2))  # Output: 1

# Clear the list
my_list.clear()
print(my_list)  # Output: []

# Extend the list
my_list.extend([1, 2, 3])
print(my_list)  # Output: [1, 2, 3] 
```

### List Comprehension, Problem Solving
- **List Comprehension**:
  ```python
  squares = [x**2 for x in range(10)]
  print(squares)
  ```
- **Problem Solving**:
  **Example**: Filter even numbers from a list.
  ```python
  numbers = [1, 2, 3, 4, 5, 6]
  evens = [num for num in numbers if num % 2 == 0]
  print(evens)
  ```

---

## Tuples, Dictionaries, and Sets in Python

### Introduction to Tuples
Tuples are immutable ordered collections of items.
```python
colors = ("red", "green", "blue")
print(colors)
```

### Tuples Slicing, Iteration, Functions, Problem Solving
- **Slicing**:
  ```python
  print(colors[0:2])
  ```
- **Iteration**:
  ```python
  for color in colors:
      print(color)
  ```
- **Functions**:
  ```python
  print(len(colors))
  print(colors.count("red"))
  ```

### Introduction to Dictionaries
Dictionaries are collections of key-value pairs.
```python
student = {"name": "John", "age": 25, "grades": [85, 90, 92]}
print(student)
```

### Iteration, Functions, Nested Dictionaries, Problem Solving
- **Iteration**:
  ```python
  for key, value in student.items():
      print(key, value)
  ```
- **Functions**:
  ```python
  student["age"] = 26
  student["address"] = "123 Main St"
  print(student)
  ```
- **Nested Dictionaries**:
  ```python
  students = {
      "student1": {"name": "John", "age": 25},
      "student2": {"name": "Jane", "age": 22}
  }
  print(students)
  ```
- **Problem Solving**:
  **Example**: Merge two dictionaries.
  ```python
  dict1 = {"a": 1, "b": 2}
  dict2 = {"b": 3, "c": 4}
  merged = {**dict1, **dict2}
  print(merged)
  ```

### Introduction to Sets
Sets are unordered collections of unique items.
```python
fruits = {"apple", "banana", "cherry"}
print(fruits)
```

### Set Methods, Problem Solving
- **Methods**:
  ```python
  fruits.add("orange")
  fruits.remove("banana")
  print(fruits)
  ```
- **Problem Solving**:
  **Example**: Find the union of two sets.
  ```python
  set1 = {1, 2, 3}
  set2 = {3, 4, 5}
  union_set = set1.union(set2)
  print(union_set)
  ```

---

## Python Functions and Modules

### Introduction to Functions
Functions are blocks of reusable code.
```python
def greet(name):
    return "Hello, " + name

print(greet("Alice"))
```

### Parameters, Arguments, Return Statement, Recursion
- **Parameters and Arguments**:
  ```python
  def add(a, b):
      return a + b

  print(add(5, 3))
  ```
- **Return Statement**:
  ```python
  def square(x):
      return x * x

  print(square(4))
  ```
- **Recursion**:
  ```python
  def factorial(n):
      if n == 1:
          return 1
      else:
          return n * factorial(n-1)

  print(factorial(5))
  ```

### Lambda Function, Local and Global Variables
- **Lambda

 Function**:
  ```python
  square = lambda x: x * x
  print(square(5))
  ```
- **Local and Global Variables**:
  ```python
  x = "global"

  def foo():
      x = "local"
      print(x)

  foo()
  print(x)
  ```

### Functions Problem Solving
**Example**: Calculate the sum of a list using a function.
```python
def sum_list(numbers):
    total = 0
    for num in numbers:
        total += num
    return total

print(sum_list([1, 2, 3, 4]))
```

### Introduction to Modules, In-built Modules
- **Introduction**:
  Modules are files containing Python code.
  ```python
  import math
  print(math.sqrt(16))
  ```
- **In-built Modules**:
  ```python
  import random
  print(random.randint(1, 10))
  ```

### Creation of Modules, Project Random Module
- **Creation**:
  Create a file `mymodule.py`:
  ```python
  def greet(name):
      return "Hello, " + name
  ```
  Use the module in another script:
  ```python
  import mymodule
  print(mymodule.greet("Alice"))
  ```
- **Project Random Module**:
  ```python
  import random

  def roll_dice():
      return random.randint(1, 6)

  print(roll_dice())
  ```

---

## Numpy and Data Manipulation

### Introduction to Numpy
NumPy is a library for numerical computations in Python.

### Installation of Jupyter Notebook
1. Install Jupyter Notebook via pip:
   ```bash
   pip install jupyter
   ```
2. Start Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

### Creation, Indexing, and Slicing of Numpy Arrays
- **Creation**:
  ```python
  import numpy as np
  arr = np.array([1, 2, 3, 4])
  print(arr)
  ```
- **Indexing**:
  ```python
  print(arr[2])
  ```
- **Slicing**:
  ```python
  print(arr[1:3])
  ```

### Mathematical Operations, Combining and Splitting Arrays
- **Mathematical Operations**:
  ```python
  arr1 = np.array([1, 2, 3])
  arr2 = np.array([4, 5, 6])
  print(arr1 + arr2)
  print(arr1 * arr2)
  ```
- **Combining**:
  ```python
  combined = np.concatenate((arr1, arr2))
  print(combined)
  ```
- **Splitting**:
  ```python
  split = np.array_split(combined, 2)
  print(split)
  ```

### Search, Sort, Filter Arrays, Aggregating Functions
- **Search**:
  ```python
  index = np.where(arr1 == 2)
  print(index)
  ```
- **Sort**:
  ```python
  sorted_arr = np.sort(arr1)
  print(sorted_arr)
  ```
- **Filter**:
  ```python
  filtered = arr1[arr1 > 1]
  print(filtered)
  ```
- **Aggregating Functions**:
  ```python
  print(np.sum(arr1))
  print(np.mean(arr1))
  ```

### Statistical Functions in Arrays
```python
data = np.array([1, 2, 3, 4, 5])
print(np.median(data))
print(np.std(data))
```

---

## Pandas for Data Analysis

### Introduction to Pandas
Pandas is a library for data manipulation and analysis.

### Creation of Data Frames, Exploring Data
- **Creation**:
  ```python
  import pandas as pd
  data = {
      "Name": ["Alice", "Bob", "Charlie"],
      "Age": [25, 30, 35]
  }
  df = pd.DataFrame(data)
  print(df)
  ```
- **Exploring**:
  ```python
  print(df.head())
  print(df.describe())
  ```

### Dealing with Duplicate values, Missing Data
- **Duplicate Values**:
  ```python
  df.drop_duplicates(inplace=True)
  ```
- **Missing Data**:
  ```python
  df.fillna(0, inplace=True)
  ```

### Column Transformation in Pandas, GroupBy
- **Column Transformation**:
  ```python
  df['Age'] = df['Age'] + 1
  ```
- **GroupBy**:
  ```python
  grouped = df.groupby('Age').mean()
  print(grouped)
  ```

### Merge, Concatenate, Join in Pandas
- **Merge**:
  ```python
  df1 = pd.DataFrame({'key': ['A', 'B', 'C'], 'value': [1, 2, 3]})
  df2 = pd.DataFrame({'key': ['B', 'C', 'D'], 'value': [4, 5, 6]})
  merged = pd.merge(df1, df2, on='key')
  print(merged)
  ```
- **Concatenate**:
  ```python
  concatenated = pd.concat([df1, df2])
  print(concatenated)
  ```
- **Join**:
  ```python
  joined = df1.join(df2.set_index('key'), on='key', lsuffix='_left', rsuffix='_right')
  print(joined)
  ```

### Pivoting and Melting Dataframes
- **Pivoting**:
  ```python
  pivoted = df.pivot(index='Name', columns='Age', values='Age')
  print(pivoted)
  ```
- **Melting**:
  ```python
  melted = pd.melt(df, id_vars=['Name'], value_vars=['Age'])
  print(melted)
  ```

---

## Matplotlib for Data Visualization

### Introduction to Matplotlib
Matplotlib is a library for creating static, animated, and interactive visualizations.

### Bar, Line, Scatter, Pie, Box, Histogram, Violin, Stem plots
- **Bar Plot**:
  ```python
  import matplotlib.pyplot as plt
  plt.bar(['A', 'B', 'C'], [10, 20, 30])
  plt.show()
  ```
- **Line Plot**:
  ```python
  plt.plot([1, 2, 3], [10, 20, 30])
  plt.show()
  ```
- **Scatter Plot**:
  ```python
  plt.scatter([1, 2, 3], [10, 20, 30])
  plt.show()
  ```
- **Pie Chart**:
  ```python
  plt.pie([10, 20, 30], labels=['A', 'B', 'C'])
  plt.show()
  ```
- **Box Plot**:
  ```python
  plt.boxplot([10, 20, 30])
  plt.show()
  ```
- **Histogram**:
  ```python
  plt.hist([10, 20, 30])
  plt.show()
  ```
- **Violin Plot**:
  ```python
  plt.violinplot([10, 20, 30])
  plt.show()
  ```
- **Stem Plot**:
  ```python
  plt.stem([1, 2, 3], [10, 20, 30])
  plt.show()
  ```

### Stack Plot, Step Chart, Legends, Subplot
- **Stack Plot**:
  ```python
  plt.stackplot([1, 2, 3], [10, 20, 30], [5, 10, 15])
  plt.show()
  ```
- **Step Chart**:
  ```python
  plt.step([1, 2, 3], [10, 20, 30])
  plt.show()
  ```
- **Legends**:
  ```python
  plt.plot([1, 2, 3], label='Line 1')
  plt.legend()
  plt.show()
  ```
- **Subplot**:
  ```python
  plt.subplot(1, 2, 1)
  plt.plot([1, 2, 3])

  plt.subplot(1, 2, 2)
  plt.plot([3, 2, 1])

  plt.show()
  ```

### Save a Chart Using Matplotlib
```python
plt.plot([1, 2, 3])
plt.savefig('plot.png')
```

### Data Visualization in Seaborn
```python
import seaborn as sns
sns.set(style="darkgrid")
tips = sns.load_dataset("tips")
sns.relplot(x="total_bill", y="tip", hue="smoker", data=tips)
plt.show()
```

### Seaborn Project
**Example**: Visualize the relationship between total_bill and tip in the tips dataset.
```python
sns.scatterplot(x="total_bill", y="tip", data=tips)
plt.show()
```

---

## MySQL for Data Analytics

### Introduction to MySQL
MySQL is a relational database management system.

### Installation, Importing Data
- **Installation**: Follow instructions from the official MySQL website.
- **Importing Data**:
  ```sql
  LOAD DATA INFILE 'path/to/data.csv'
  INTO TABLE table_name
  FIELDS TERMINATED BY ','
  LINES TERMINATED BY '\n'
  IGNORE 1 LINES;
  ```

### Select Query, Where Clause
- **Select Query**:
  ```sql


  SELECT * FROM table_name;
  ```
- **Where Clause**:
  ```sql
  SELECT * FROM table_name WHERE column_name = 'value';
  ```

### AND, OR, NOT Operators, Like Operator
- **AND, OR, NOT**:
  ```sql
  SELECT * FROM table_name WHERE column1 = 'value1' AND column2 = 'value2';
  SELECT * FROM table_name WHERE column1 = 'value1' OR column2 = 'value2';
  SELECT * FROM table_name WHERE NOT column1 = 'value1';
  ```
- **Like Operator**:
  ```sql
  SELECT * FROM table_name WHERE column_name LIKE 'pattern%';
  ```

### Order By, Limit, Between
- **Order By**:
  ```sql
  SELECT * FROM table_name ORDER BY column_name ASC;
  ```
- **Limit**:
  ```sql
  SELECT * FROM table_name LIMIT 10;
  ```
- **Between**:
  ```sql
  SELECT * FROM table_name WHERE column_name BETWEEN value1 AND value2;
  ```

### IN, NOT IN operator, String Functions
- **IN, NOT IN**:
  ```sql
  SELECT * FROM table_name WHERE column_name IN ('value1', 'value2');
  SELECT * FROM table_name WHERE column_name NOT IN ('value1', 'value2');
  ```
- **String Functions**:
  ```sql
  SELECT CONCAT(first_name, ' ', last_name) AS full_name FROM table_name;
  ```

### Data Aggregation, Numeric Functions
- **Data Aggregation**:
  ```sql
  SELECT COUNT(*), AVG(column_name) FROM table_name;
  ```
- **Numeric Functions**:
  ```sql
  SELECT ROUND(column_name, 2) FROM table_name;
  ```

### Date Functions, Case Operator
- **Date Functions**:
  ```sql
  SELECT CURDATE(), NOW() FROM table_name;
  ```
- **Case Operator**:
  ```sql
  SELECT column_name,
  CASE
      WHEN condition1 THEN 'result1'
      WHEN condition2 THEN 'result2'
      ELSE 'result3'
  END AS alias_name
  FROM table_name;
  ```

### Group By, Having Clause
- **Group By**:
  ```sql
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
  ```
- **Having Clause**:
  ```sql
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > 1;
  ```

### Joins, Set Operators, Subqueries, Views
- **Joins**:
  ```sql
  SELECT * FROM table1
  JOIN table2 ON table1.column_name = table2.column_name;
  ```
- **Set Operators**:
  ```sql
  SELECT column_name FROM table1
  UNION
  SELECT column_name FROM table2;
  ```
- **Subqueries**:
  ```sql
  SELECT * FROM table_name WHERE column_name IN (SELECT column_name FROM table_name);
  ```
- **Views**:
  ```sql
  CREATE VIEW view_name AS
  SELECT * FROM table_name;
  ```

### Stored Procedure, Window Functions
- **Stored Procedure**:
  ```sql
  DELIMITER //
  CREATE PROCEDURE procedure_name()
  BEGIN
      SELECT * FROM table_name;
  END //
  DELIMITER ;
  ```
- **Window Functions**:
  ```sql
  SELECT column_name,
  ROW_NUMBER() OVER(PARTITION BY column_name ORDER BY column_name) AS row_num
  FROM table_name;
  ```

---

## Excel for Data Analytics

### Introduction to MS Excel
Excel is a spreadsheet program for data analysis.

### Basic Functions, Data Validation
- **Basic Functions**:
  ```excel
  =SUM(A1:A10)
  ```
- **Data Validation**:
  Data > Data Validation > Settings > Allow > List > Source: A1:A10

### Data Connectors, Conditional Formatting
- **Data Connectors**:
  Data > Get Data > From Other Sources
- **Conditional Formatting**:
  Home > Conditional Formatting > Highlight Cell Rules

### Basics of Formatting, Sorting, Filtering Data
- **Formatting**:
  Home > Number > Format Cells
- **Sorting**:
  Data > Sort
- **Filtering**:
  Data > Filter

### Dealing with Null Values, Duplicate Values
- **Null Values**:
  ```excel
  =IF(ISBLANK(A1), "No Data", A1)
  ```
- **Duplicate Values**:
  Data > Remove Duplicates

### Trimming Whitespaces, Text Functions
- **Trimming Whitespaces**:
  ```excel
  =TRIM(A1)
  ```
- **Text Functions**:
  ```excel
  =LEFT(A1, 5)
  =MID(A1, 2, 3)
  =RIGHT(A1, 5)
  ```

### IF, AND, OR Functions, Date & Time Functions
- **IF, AND, OR Functions**:
  ```excel
  =IF(A1 > 10, "Yes", "No")
  =AND(A1 > 10, B1 < 5)
  =OR(A1 > 10, B1 < 5)
  ```
- **Date & Time Functions**:
  ```excel
  =TODAY()
  =NOW()
  ```

### COUNTIF, SUMIF Functions, Xlookup
- **COUNTIF, SUMIF**:
  ```excel
  =COUNTIF(A1:A10, ">5")
  =SUMIF(A1:A10, ">5", B1:B10)
  ```
- **Xlookup**:
  ```excel
  =XLOOKUP("search_value", search_array, return_array)
  ```

### Power Query, Cleaning and Transformation
- **Power Query**:
  Data > Get Data > Launch Power Query Editor
- **Cleaning and Transformation**:
  Power Query Editor > Home > Remove Rows, Replace Values

### Creating a Dashboard in Excel, myExcel Project
- **Creating a Dashboard**:
  Insert > Chart, PivotTable
- **myExcel Project**:
  Create a comprehensive dashboard using various charts, tables, and slicers.

---

## Power BI Essentials

### Introduction to Power Bi
Power BI is a business analytics tool by Microsoft.

### Installation of Power Bi Desktop
1. Download and install Power BI Desktop from the official Power BI website.
2. Launch Power BI Desktop.

### Data Connectors, Basic Transformations
- **Data Connectors**:
  Home > Get Data > Choose a data source
- **Basic Transformations**:
  Transform Data > Power Query Editor

### Format Tool, Pivoting, Unpivoting of data
- **Format Tool**:
  Visualizations > Format
- **Pivoting**:
  Transform > Pivot Column
- **Unpivoting**:
  Transform > Unpivot Columns

### Adding Conditional Columns, Merge queries
- **Conditional Columns**:
  Add Column > Conditional Column
- **Merge queries**:
  Home > Merge Queries

### Data model, Relationship Management
- **Data model**:
  Model > Manage Relationships
- **Relationship Management**:
  Model > Create relationships between tables

### Introduction to DAX, Calculated Columns, Measures
- **Introduction to DAX**:
  DAX (Data Analysis Expressions) is a formula language in Power BI.
- **Calculated Columns**:
  Data > New Column
- **Measures**:
  Modeling > New Measure

### DAX Functions, Visualizations, Filters
- **DAX Functions**:
  ```dax
  Total Sales = SUM(Sales[Amount])
  ```
- **Visualizations**:
  Visualizations pane > Choose a visualization type
- **Filters**:
  Visualizations pane > Filters

### Creating Reports, Custom Visuals
- **Creating Reports**:
  Visualizations > Add visuals to the report
- **Custom Visuals**:
  Import from marketplace

### Designing for Phone vs Desktop Report Viewers
- **Designing for Phone**:
  View > Phone Layout
- **Desktop Report Viewers**:
  Standard desktop layout

### Publishing Reports to Power BI Services
1. File > Publish > Publish to Power BI
2. Log in to Power BI service and access the published report.
