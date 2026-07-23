# Pandas Assignments on Student Marks Dataset

---

## Assignment 1 – Load Dataset

### Question:

Load the `student_marks.csv` dataset using Pandas and display:

* First 5 rows
* Last 5 rows
* Shape of the dataset
* Column names

### Code:

```python
import pandas as pd

df = pd.read_csv("/content/student_data_converted.csv")

print(df.head())
print(df.tail())
print(df.shape)
print(df.columns)
```

---

## Assignment 2 – Dataset Information

### Question:

Check the following information in the dataset:

* Missing values
* Duplicate rows
* Data types of all columns

### Code:

```python
print(df.isnull().sum())

print(df.duplicated().sum())

print(df.info())
```

---

## Assignment 3 – Create Total Marks

### Question:

Create a new column named **Total** by adding the marks of:

* Maths
* Science
* English
* History

### Code:

```python
df["Total"] = (
    df["Maths"] +
    df["Science"] +
    df["English"] +
    df["History"]
)

print(df["Total"])
```

---

## Assignment 4 – Calculate Average

### Question:

Create a new column named **Average** using the total marks.

### Code:

```python
df["Average"] = df["Total"] / 4

print(df["Average"])
```

---

## Assignment 5 – Calculate Percentage

### Question:

Create a new column named **Percentage**, assuming total marks are out of **400**.

### Code:

```python
df["Percentage"] = (df["Total"] / 400) * 100

print(df["Percentage"])
```

---

## Assignment 6 – Highest and Lowest Marks

### Question:

Find:

* Highest marks in each subject
* Lowest marks in each subject

### Code:

```python
print("Highest Marks")

print("Maths:", df["Maths"].max())
print("Science:", df["Science"].max())
print("English:", df["English"].max())
print("History:", df["History"].max())

print()

print("Lowest Marks")

print("Maths:", df["Maths"].min())
print("Science:", df["Science"].min())
print("English:", df["English"].min())
print("History:", df["History"].min())
```

---

## Assignment 7 – Highest and Lowest Scoring Students

### Question:

Find the student who scored:

* Highest Total marks
* Lowest Total marks

### Code:

```python
print("Highest Scoring Student")

print(df[df["Total"] == df["Total"].max()])

print()

print("Lowest Scoring Student")

print(df[df["Total"] == df["Total"].min()])
```

> **Correction:** This displays the complete student record instead of only the highest and lowest total values.

---

## Assignment 8 – Filter Students

### Question:

Display:

* Students who scored above 90 in Maths
* Students who scored below 75 in Science
* Students who scored above 85 in all subjects

### Code:

```python
print(df[df["Maths"] > 90])

print()

print(df[df["Science"] < 75])

print()

print(
    df[
        (df[["Maths", "Science", "English", "History"]] > 85)
        .all(axis=1)
    ]
)
```

---

## Assignment 9 – Sort Students

### Question:

Sort the students:

* By Total marks (Descending)
* By Age (Ascending)

### Code:

```python
print(df.sort_values(by="Total", ascending=False))

print()

print(df.sort_values(by="Age", ascending=True))
```

---

## Assignment 10 – Top and Bottom Students

### Question:

Display:

* Top 5 students based on Total marks
* Bottom 5 students based on Total marks

### Code:

```python
print("Top 5 Students")

print(df.sort_values(by="Total", ascending=False).head(5))

print()

print("Bottom 5 Students")

print(df.sort_values(by="Total", ascending=True).head(5))
```
Perfect! Here is the **corrected Part 2 (Assignments 11–20)** in the same format.

---

# Assignment 11 – Assign Grades

### Question:

Create a new column named **Grade** using the following criteria:

* A → 90 and above
* B → 75–89
* C → 60–74
* D → Below 60

### Code:

```python

# Grade Function
def category(percentage):
    if percentage >= 90:
        return "Grade A"
    elif percentage >= 75:
        return "Grade B"
    elif percentage >= 60:
        return "Grade C"
    else:
        return "Grade D"

df["Grade"] = df["Percentage"].apply(category)

print(df["Grade"])
```

---

# Assignment 12 – Pass/Fail Result

### Question:

Create a new column named **Pass/Fail** using the following criteria:

* Pass if Average ≥ 40
* Fail otherwise

### Code:

```python

def result(average):
    if average >= 40:
        return "Pass"
    else:
        return "Fail"

df["Pass/Fail"] = df["Average"].apply(result)

print(df["Pass/Fail"])
```

---

# Assignment 13 – Student Count

### Question:

Find:

* Total number of students
* Number of students age-wise
* Number of students in each grade

### Code:

```python

print("Total Students =", len(df))

print()

print("Students Age-wise")
print(df["Age"].value_counts())

print()

print("Students Grade-wise")
print(df["Grade"].value_counts())
```

---

# Assignment 14 – Subject-wise Average

### Question:

Find the average marks of:

* Maths
* Science
* English
* History

### Code:

```python

print("Maths Average =", df["Maths"].mean())

print("Science Average =", df["Science"].mean())

print("English Average =", df["English"].mean())

print("History Average =", df["History"].mean())
```

---

# Assignment 15 – Correlation

### Question:

Find the correlation between all subject marks.

### Code:

```python

print(df[["Maths","Science","English","History"]].corr())
```

---

# Assignment 16 – Filter Students by Performance

### Question:

Display:

* Students whose Total marks are above the class average
* Students whose Percentage is above 85%

### Code:

```python

class_average = df["Total"].mean()

print("Students Above Class Average")

print(df[df["Total"] > class_average])

print()

print("Students Above 85%")

print(df[df["Percentage"] > 85])
```

---

# Assignment 17 – Subject Toppers

### Question:

Find:

* Topper in each subject
* Overall class topper

### Code:

```python

print("Maths Topper")
print(df[df["Maths"] == df["Maths"].max()])

print()

print("Science Topper")
print(df[df["Science"] == df["Science"].max()])

print()

print("English Topper")
print(df[df["English"] == df["English"].max()])

print()

print("History Topper")
print(df[df["History"] == df["History"].max()])

print()

print("Overall Class Topper")
print(df[df["Total"] == df["Total"].max()])
```

---

# Assignment 18 – Student Ranking

### Question:

Create a new column named **Rank** based on Total marks.

### Code:

```python

df["Rank"] = df["Total"].rank(ascending=False, method="dense")

print(df[["Name","Total","Rank"]])
```

---

# Assignment 19 – Export Dataset

### Question:

Export the updated dataset into a new CSV file named **processed_students.csv**.

### Code:

```python

df.to_csv("processed_students.csv", index=False)

print("Dataset Exported Successfully!")
```

---

# Assignment 20 – Mini Student Report System

### Question:

Create a Student Report System that:

* Loads the student dataset
* Calculates Total, Average and Percentage
* Assigns Grades
* Assigns Pass/Fail
* Ranks students
* Exports the final report as **final_student_report.csv**

### Code:

```python

import pandas as pd

# Load Dataset
df = pd.read_csv("/content/student_data_converted.csv")

# Total
df["Total"] = df["Maths"] + df["Science"] + df["English"] + df["History"]

# Average
df["Average"] = df["Total"] / 4

# Percentage
df["Percentage"] = (df["Total"] / 400) * 100

# Grade
def grade(percentage):
    if percentage >= 90:
        return "Grade A"
    elif percentage >= 75:
        return "Grade B"
    elif percentage >= 60:
        return "Grade C"
    else:
        return "Grade D"

df["Grade"] = df["Percentage"].apply(grade)

# Pass/Fail
def result(average):
    if average >= 40:
        return "Pass"
    else:
        return "Fail"

df["Pass/Fail"] = df["Average"].apply(result)

# Rank
df["Rank"] = df["Total"].rank(ascending=False, method="dense")

# Display Final Report
print(df)

# Export Final Report
df.to_csv("final_student_report.csv", index=False)

print("Final Student Report Exported Successfully!")
```
---

