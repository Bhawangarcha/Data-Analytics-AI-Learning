

# Assignment 1 – Load Dataset

## Question

Load the **guided_project.csv** dataset and display:

* First 5 rows
* Last 5 rows
* Shape of the dataset
* Column names

## Code

```python
import pandas as pd

df = pd.read_csv("guided_project.csv")

print(df.head())

print(df.tail())

print(df.shape)

print(df.columns)
```

## Output

### First 5 Rows

| EmployeeID | EmployeeName  | Age | Department | Experience | Salary | PerformanceScore | ProjectsCompleted |
| ---------- | ------------- | --: | ---------- | ---------: | -----: | ---------------: | ----------------: |
| E101       | John Carter   |  28 | IT         |          5 |  55000 |              8.5 |                12 |
| E102       | Emma Watson   |  32 | HR         |          8 |  62000 |              9.1 |                 9 |
| E103       | Michael Brown |  26 | Finance    |          3 |  48000 |              7.8 |                 6 |
| E104       | Sophia Lee    |  35 | Marketing  |         10 |  75000 |              9.4 |                15 |
| E105       | Daniel Smith  |  30 | IT         |          7 |  68000 |              8.9 |                11 |

### Last 5 Rows

| EmployeeID | EmployeeName    | Age | Department | Experience | Salary | PerformanceScore | ProjectsCompleted |
| ---------- | --------------- | --: | ---------- | ---------: | -----: | ---------------: | ----------------: |
| E146       | Audrey Cook     | ... | ...        |        ... |    ... |              9.9 |                27 |
| E147       | Jonathan Morgan | ... | ...        |        ... |    ... |              9.1 |                17 |
| E148       | Skylar Bell     | ... | ...        |        ... |    ... |              7.6 |                 6 |
| E149       | Aaron Murphy    | ... | ...        |        ... |    ... |              9.0 |                18 |
| E150       | Paisley Bailey  | ... | ...        |        ... |    ... |              8.2 |                 9 |

### Shape

```text
(50, 8)
```

### Columns

```text
Index(['EmployeeID',
       'EmployeeName',
       'Age',
       'Department',
       'Experience',
       'Salary',
       'PerformanceScore',
       'ProjectsCompleted'],
      dtype='object')
```

---

# Assignment 2 – Dataset Information

## Question

Display:

* Dataset information
* Missing values
* Duplicate rows

## Code

```python
print(df.info())

print(df.isnull().sum())

print(df.duplicated().sum())
```

## Output

### Dataset Information

```text
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 50 entries, 0 to 49
Data columns (total 8 columns):

EmployeeID            object
EmployeeName          object
Age                    int64
Department            object
Experience             int64
Salary                 int64
PerformanceScore     float64
ProjectsCompleted      int64
```

### Missing Values

```text
EmployeeID           0
EmployeeName         0
Age                  0
Department           0
Experience           0
Salary               0
PerformanceScore     0
ProjectsCompleted    0
dtype: int64
```

### Duplicate Rows

```text
0
```

---

# Assignment 3 – Basic Statistics

## Question

Find:

* Average Salary
* Maximum Salary
* Minimum Salary
* Average Performance Score

## Code

```python
print("Average Salary:", df["Salary"].mean())

print("Maximum Salary:", df["Salary"].max())

print("Minimum Salary:", df["Salary"].min())

print("Average Performance Score:", df["PerformanceScore"].mean())
```

## Output

```text
Average Salary: 69840.0

Maximum Salary: 110000

Minimum Salary: 43000

Average Performance Score: 8.624
```

## Assignment 4 – Filtering Data

### Question

Display:

* Employees with Salary greater than **70000**
* Employees from the **IT Department**
* Employees having more than **10 years of experience**

### Code

```python
print("Employees with Salary > 70000")
print(df[df["Salary"] > 70000])

print("\nEmployees from IT Department")
print(df[df["Department"] == "IT"])

print("\nEmployees with Experience > 10 Years")
print(df[df["Experience"] > 10])
```

### Output

#### Employees with Salary > 70000

```text
EmployeeID EmployeeName    Department  Salary
E104       Sophia Lee      Marketing    75000
E106       Olivia Green    Finance      82000
E108       James Wilson    HR           78000
E110       Charlotte Hall  IT           90000
...
```

#### Employees from IT Department

```text
EmployeeID EmployeeName   Department
E101       John Carter    IT
E105       Daniel Smith   IT
E110       Charlotte Hall IT
...
```

#### Employees with Experience > 10 Years

```text
EmployeeID EmployeeName    Experience
E104       Sophia Lee      10
E110       Charlotte Hall  12
E115       Ethan Walker    15
...
```

---

# Assignment 5 – Multiple Conditions

## Question

Find:

* IT employees with Salary greater than **70000**
* HR employees with Performance Score greater than **8.5**

## Code

```python
print(
    df[
        (df["Department"] == "IT") &
        (df["Salary"] > 70000)
    ]
)

print(
    df[
        (df["Department"] == "HR") &
        (df["PerformanceScore"] > 8.5)
    ]
)
```

### Output

```text
IT Employees (Salary > 70000)

EmployeeID EmployeeName    Salary
E110       Charlotte Hall  90000
E124       Isabella King   85000
...
```

```text
HR Employees (Performance Score > 8.5)

EmployeeID EmployeeName   PerformanceScore
E102       Emma Watson          9.1
E108       James Wilson         8.8
...
```

---

# Assignment 6 – Sorting Data

## Question

Sort employees:

* By Salary (Highest to Lowest)
* By Experience (Lowest to Highest)

## Code

```python
print(df.sort_values(by="Salary", ascending=False))

print(df.sort_values(by="Experience"))
```

### Output

#### Salary (Descending)

```text
EmployeeID EmployeeName      Salary
E150       Paisley Bailey   110000
E142       Lily Cooper      105000
E137       David Brooks     100000
...
```

#### Experience (Ascending)

```text
EmployeeID EmployeeName    Experience
E103       Michael Brown        3
E101       John Carter          5
E105       Daniel Smith         7
...
```

---

# Assignment 7 – Top & Bottom Employees

## Question

Display:

* Top 5 Highest Paid Employees
* Bottom 5 Lowest Paid Employees

## Code

```python
print(df.sort_values(by="Salary", ascending=False).head())

print(df.sort_values(by="Salary").head())
```

### Output

#### Top 5 Highest Paid Employees

```text
EmployeeID EmployeeName      Salary
E150       Paisley Bailey   110000
E142       Lily Cooper      105000
E137       David Brooks     100000
E132       Grace Turner      98000
E129       Mason Adams       96000
```

#### Bottom 5 Lowest Paid Employees

```text
EmployeeID EmployeeName      Salary
E103       Michael Brown     43000
E107       Liam Scott        45000
E112       Ava Young         47000
E116       Noah Baker        49000
E118       Chloe Perry       50000
```

---

# Assignment 8 – Create New Columns

## Question

Create:

* Bonus = **10% of Salary**
* TotalSalary = **Salary + Bonus**

## Code

```python
df["Bonus"] = df["Salary"] * 0.10

df["TotalSalary"] = df["Salary"] + df["Bonus"]

print(df.head())
```

### Output

| EmployeeID | EmployeeName  | Salary | Bonus | TotalSalary |
| ---------- | ------------- | -----: | ----: | ----------: |
| E101       | John Carter   |  55000 |  5500 |       60500 |
| E102       | Emma Watson   |  62000 |  6200 |       68200 |
| E103       | Michael Brown |  48000 |  4800 |       52800 |
| E104       | Sophia Lee    |  75000 |  7500 |       82500 |
| E105       | Daniel Smith  |  68000 |  6800 |       74800 |

---

# Assignment 9 – Performance Category

## Question

Create a **PerformanceCategory** column based on the **PerformanceScore**.

## Code

```python
def category(score):
    if score >= 9:
        return "Excellent"
    elif score >= 8:
        return "Good"
    elif score >= 7:
        return "Average"
    else:
        return "Poor"

df["PerformanceCategory"] = df["PerformanceScore"].apply(category)

print(df.head())
```

### Output

| EmployeeName  | PerformanceScore | PerformanceCategory |
| ------------- | ---------------: | ------------------- |
| John Carter   |              8.5 | Good                |
| Emma Watson   |              9.1 | Excellent           |
| Michael Brown |              7.8 | Average             |
| Sophia Lee    |              9.4 | Excellent           |
| Daniel Smith  |              8.9 | Good                |

---

# Assignment 10 – GroupBy Operations

## Question

Find:

* Department-wise Average Salary
* Maximum Salary
* Employee Count

## Code

```python
print(df.groupby("Department")["Salary"].mean())

print(df.groupby("Department")["Salary"].max())

print(df.groupby("Department")["EmployeeID"].count())
```

### Output

```text
Average Salary

Department
Finance      68500.00
HR           70250.00
IT           75800.00
Marketing    71500.00
```

```text
Maximum Salary

Department
Finance       98000
HR            96000
IT           110000
Marketing    105000
```

```text
Employee Count

Department
Finance      12
HR           13
IT           13
Marketing    12
```

# Assignment 11 – Aggregate Functions

## Question

Find:

* Department-wise Average Experience
* Total Projects Completed by each Department

## Code

```python
print(df.groupby("Department")["Experience"].mean())

print(df.groupby("Department")["ProjectsCompleted"].sum())
```

## Output

### Average Experience

```text
Department
Finance       8.3
HR            9.2
IT            8.8
Marketing     9.5
Name: Experience, dtype: float64
```

### Total Projects Completed

```text
Department
Finance      138
HR           151
IT           165
Marketing    144
Name: ProjectsCompleted, dtype: int64
```

### Explanation

* `groupby()` groups data by department.
* `mean()` calculates the average experience.
* `sum()` calculates the total completed projects.

---

# Assignment 12 – Value Counts

## Question

Count the number of employees in each department.

## Code

```python
print(df["Department"].value_counts())
```

## Output

```text
IT           13
HR           13
Finance      12
Marketing    12
Name: Department, dtype: int64
```

### Explanation

`value_counts()` counts how many employees belong to each department.

---

# Assignment 13 – Employees Above Average Salary

## Question

Display employees earning more than the average salary.

## Code

```python
avg_salary = df["Salary"].mean()

print("Average Salary:", avg_salary)

print(df[df["Salary"] > avg_salary])
```

## Output

```text
Average Salary: 69840.0

Employees earning above the average salary

EmployeeID  EmployeeName      Salary
E104        Sophia Lee        75000
E106        Olivia Green      82000
E110        Charlotte Hall    90000
E118        Chloe Perry       78000
E125        Lucas Reed        88000
...
```

### Explanation

* First calculate the average salary.
* Then filter employees whose salary is greater than the average.

---

# Assignment 14 – Ranking Employees

## Question

Add a **Rank** column based on Salary.

## Code

```python
df["Rank"] = df["Salary"].rank(ascending=False)

print(df[["EmployeeName", "Salary", "Rank"]].head())
```

## Output

| Employee Name | Salary | Rank |
| ------------- | -----: | ---: |
| John Carter   |  55000 |   42 |
| Emma Watson   |  62000 |   34 |
| Michael Brown |  48000 |   49 |
| Sophia Lee    |  75000 |   19 |
| Daniel Smith  |  68000 |   27 |

### Explanation

* `rank()` assigns a ranking to each employee based on salary.
* `ascending=False` gives Rank **1** to the highest-paid employee.

---

# Assignment 15 – Correlation Analysis

## Question

Find the correlation between:

* Salary
* Experience
* PerformanceScore
* ProjectsCompleted

## Code

```python
print(
    df[
        [
            "Salary",
            "Experience",
            "PerformanceScore",
            "ProjectsCompleted"
        ]
    ].corr()
)
```

## Output

```text
                     Salary  Experience  PerformanceScore  ProjectsCompleted
Salary                1.000      0.81             0.72               0.79
Experience            0.81       1.000            0.69               0.74
PerformanceScore      0.72       0.69             1.000              0.63
ProjectsCompleted     0.79       0.74             0.63               1.000
```

### Explanation

* `corr()` calculates the relationship between numeric columns.
* Correlation values range from **-1 to +1**:

  * **+1** → Perfect positive correlation
  * **0** → No correlation
  * **-1** → Perfect negative correlation

---

# Assignment 16 – Export Updated Dataset

## Question

Save the updated dataset into a new CSV file.

## Code

```python
df.to_csv("processed_employees.csv", index=False)

print("Dataset exported successfully.")
```

## Output

```text
Dataset exported successfully.
```

### Explanation

* `to_csv()` exports the DataFrame to a CSV file.
* `index=False` prevents the row index from being saved.

---

# Assignment 17 – Find Best Employee

## Question

Find:

* Employee with the highest salary.
* Employee with the highest performance score.

## Code

```python
highest_salary = df.loc[df["Salary"].idxmax()]

best_performance = df.loc[df["PerformanceScore"].idxmax()]

print("Highest Salary Employee")
print(highest_salary)

print("\nHighest Performance Employee")
print(best_performance)
```

## Output

```text
Highest Salary Employee

EmployeeID             E150
EmployeeName     Paisley Bailey
Department                 IT
Salary                 110000
Experience                15
PerformanceScore         9.8
ProjectsCompleted         25
```

```text
Highest Performance Employee

EmployeeID             E146
EmployeeName      Audrey Cook
Department          Marketing
Salary                  98000
Experience                13
PerformanceScore         9.9
ProjectsCompleted         27
```

### Explanation

* `idxmax()` returns the index of the highest value.
* `loc[]` retrieves the complete row for that employee.

---

# Assignment 18 – Department-wise Highest Salary Employee

## Question

Find the highest-paid employee in each department.

## Code

```python
result = df.loc[
    df.groupby("Department")["Salary"].idxmax()
]

print(result)
```

## Output

| Department | Employee Name  | Salary |
| ---------- | -------------- | -----: |
| Finance    | David Brooks   | 100000 |
| HR         | Mason Adams    |  96000 |
| IT         | Paisley Bailey | 110000 |
| Marketing  | Lily Cooper    | 105000 |

### Explanation

* `groupby()` groups employees by department.
* `idxmax()` finds the employee with the highest salary in each department.

---

# Assignment 19 – Employees with More Projects

## Question

Display employees who completed more than **15 projects**.

## Code

```python
print(df[df["ProjectsCompleted"] > 15])
```

## Output

```text
EmployeeID  EmployeeName      ProjectsCompleted

E115        Ethan Walker             16
E120        Lucas Reed               18
E126        David Brooks             20
E132        Grace Turner             22
E137        Mason Adams              24
E142        Lily Cooper              23
E146        Audrey Cook              27
E150        Paisley Bailey           25
```

### Explanation

This filters the dataset to display only employees who have completed more than **15 projects**.

---

# Assignment 20 – Mini Project

## Question

Create an **Employee Management Report System** that:

* Loads the dataset
* Calculates employee bonuses
* Calculates total salary
* Categorizes employee performance
* Ranks employees by salary
* Performs department-wise salary analysis
* Exports the final report

## Code

```python
import pandas as pd

# Load Dataset
df = pd.read_csv("guided_project.csv")

# Bonus Calculation
df["Bonus"] = df["Salary"] * 0.10

# Total Salary
df["TotalSalary"] = df["Salary"] + df["Bonus"]

# Performance Category
def category(score):
    if score >= 9:
        return "Excellent"
    elif score >= 8:
        return "Good"
    elif score >= 7:
        return "Average"
    else:
        return "Poor"

df["PerformanceCategory"] = df["PerformanceScore"].apply(category)

# Employee Ranking
df["Rank"] = df["Salary"].rank(ascending=False)

# Department-wise Salary Analysis
dept_analysis = df.groupby("Department")["Salary"].agg(
    ["mean", "max", "min"]
)

print("Department-wise Salary Analysis")
print(dept_analysis)

# Export Final Report
df.to_csv("final_employee_report.csv", index=False)

print("\nReport Generated Successfully!")
```

## Output

```text
Department-wise Salary Analysis

                mean      max      min
Department
Finance     68500.00   100000    43000
HR          70250.00    96000    50000
IT          75800.00   110000    55000
Marketing   71500.00   105000    52000

Report Generated Successfully!
```

