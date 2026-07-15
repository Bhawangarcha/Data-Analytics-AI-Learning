# Guided Pandas 

### Assignment 1 – Load Dataset

### Question:
Load the employees.csv dataset and display the first 5 rows, last 5 rows, shape, and column names.

### Code:

import pandas as pd

df = pd.read_csv("employees.csv")

print(df.head())
print(df.tail())
print(df.shape)
print(df.columns)

 ### Output
 
<img width="780" height="403" alt="image" src="https://github.com/user-attachments/assets/fbc463a3-f95a-4d4c-a1f9-5bc24d18f175" />
<img width="827" height="480" alt="image" src="https://github.com/user-attachments/assets/72b11716-76f4-4fff-95b0-de86a5fd9969" />

---

### Assignment 2 – Dataset Information

### Question:
Display the data types, missing values, and duplicate rows in the dataset.

### Code:

print(df.info())
print(df.isnull().sum())
print(df.duplicated().sum())

### Output

<img width="708" height="706" alt="image" src="https://github.com/user-attachments/assets/0b79e5f3-fc96-4f88-abde-0e0bbd5cc49e" />

---

### Assignment 3 – Basic Statistics

### Question:
Find the average salary, maximum salary, minimum salary, and average performance score.

### Code:

print(df["Salary"].mean())
print(df["Salary"].max())
print(df["Salary"].min())
print(df["PerformanceScore"].mean())

### Output
<img width="457" height="430" alt="image" src="https://github.com/user-attachments/assets/1f84c0bd-aefc-4f80-b81b-5589f7a45870" />

---

### Assignment 4 – Filtering Data

### Question:
Display employees with salary above 80,000, employees from the IT department, and employees with more than 10 years of experience.

### Code:

print(df[df["Salary"] > 80000])
print(df[df["Department"] == "IT"])
print(df[df["Experience"] > 10])

### Output
<img width="861" height="662" alt="image" src="https://github.com/user-attachments/assets/774a3019-a2ae-4b72-83bd-15982cd4fc56" />
<img width="732" height="596" alt="image" src="https://github.com/user-attachments/assets/572d0f4e-dc1f-4547-b89d-c274171bb22e" />
<img width="827" height="512" alt="image" src="https://github.com/user-attachments/assets/392630fe-9de9-434c-92a2-74c7953852a1" />

---

### Assignment 5 – Multiple Conditions

### Question:
Find employees from the IT department with salary greater than 70,000 and employees from the HR department with a performance score greater than 8.5.

### Code:

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

### Output
<img width="796" height="702" alt="image" src="https://github.com/user-attachments/assets/8a27ee32-882b-40b7-be64-faf8290a9d1e" />

---

### Assignment 6 – Sorting Data

### Question:
Sort employees by salary in descending order and by experience in ascending order.

### Code:

print(df.sort_values(by="Salary", ascending=False))
print(df.sort_values(by="Experience"))

### Output
<img width="941" height="697" alt="image" src="https://github.com/user-attachments/assets/cdbc4271-c846-408a-ad5f-8c4ea11eb970" />
<img width="811" height="701" alt="image" src="https://github.com/user-attachments/assets/1bdc3da6-69d1-47f4-a1a5-b338b853f4c1" />

---

### Assignment 7 – Top and Bottom Employees

### Question:
Display the top 5 highest-paid employees and the bottom 5 lowest-paid employees.

### Code:

print(df.sort_values(by="Salary", ascending=False).head(5))

print(df.sort_values(by="Salary").head(5))

### Output
<img width="751" height="701" alt="image" src="https://github.com/user-attachments/assets/385d06af-6a53-4b72-80ec-16a9a73a5294" />

---

### Assignment 8 – Create New Columns

### Question:
Create Bonus (10% of Salary) and TotalSalary (Salary + Bonus) columns.

### Code:

df["Bonus"] = df["Salary"] * 0.10
df["TotalSalary"] = df["Salary"] + df["Bonus"]

print(df.head())

### Output
<img width="815" height="413" alt="image" src="https://github.com/user-attachments/assets/1d888a66-92a9-4fa0-810f-a64b8719f05f" />

---

### Assignment 9 – Performance Category

### Question:
Create a PerformanceCategory column based on the PerformanceScore.

### Code:

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

### Output
<img width="656" height="680" alt="image" src="https://github.com/user-attachments/assets/1d8a6a72-b1ef-4cfb-9837-ddb8d8a87698" />

---

### Assignment 10 – GroupBy Operations

### Question:
Find department-wise average salary, maximum salary, and employee count.

### Code:

print(df.groupby("Department")["Salary"].mean())

print(df.groupby("Department")["Salary"].max())

print(df.groupby("Department")["EmployeeID"].count())

### Output
<img width="647" height="588" alt="image" src="https://github.com/user-attachments/assets/4c4c6358-c0de-48be-93aa-e44f540e4de9" />

---

### Assignment 11 – Aggregate Functions

### Question:
Find department-wise average experience and total projects completed.

### Code:

print(df.groupby("Department")["Experience"].mean())

print(df.groupby("Department")["ProjectsCompleted"].sum())

### Output
<img width="702" height="455" alt="image" src="https://github.com/user-attachments/assets/81caefdb-737a-406e-86df-20838574a1f8" />

---

### Assignment 12 – Value Counts

### Question:
Count the number of employees in each department.

### Code:

print(df["Department"].value_counts())

### Output
<img width="502" height="273" alt="image" src="https://github.com/user-attachments/assets/9e2e3e2c-a485-4206-9e97-60e4925b6ed1" />

---

### Assignment 13 – Employees Above Average Salary

### Question:
Display employees earning more than the average salary.

### Code:

avg_salary = df["Salary"].mean()

print(df[df["Salary"] > avg_salary])

### Output
<img width="863" height="712" alt="image" src="https://github.com/user-attachments/assets/0990ac94-2557-416d-ac0a-ebec1ff51968" />

---

### Assignment 14 – Ranking Employees

### Question:
Add a Rank column based on salary.

### Code:

df["Rank"] = df["Salary"].rank(ascending=False)

print(df.head())

### Output
<img width="687" height="535" alt="image" src="https://github.com/user-attachments/assets/f132de48-bc36-4740-ab13-4d8af5e5cc07" />

---

### Assignment 15 – Correlation

### Question:
Find the correlation between Salary, Experience, PerformanceScore, and ProjectsCompleted.

### Code:

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

### Output
<img width="846" height="190" alt="image" src="https://github.com/user-attachments/assets/75d7e534-c76f-4945-a07f-7d159c4bf5e9" />

---

### Assignment 16 – Export Updated Dataset

### Question:
Save the updated dataset into a new CSV file.

### Code:

df.to_csv("processed_employees.csv", index=False)

### Output
<img width="667" height="68" alt="image" src="https://github.com/user-attachments/assets/cd93c512-3c3f-46f4-943d-a3c8f521fa9f" />

---

### Assignment 17 – Find Best Employee

### Question:
Find the employee with the highest salary and the highest performance score.

### Code:

highest_salary = df.loc[df["Salary"].idxmax()]

best_performance = df.loc[df["PerformanceScore"].idxmax()]

print(highest_salary)
print(best_performance)

### Output
<img width="713" height="457" alt="image" src="https://github.com/user-attachments/assets/fc629755-8525-4ed7-9044-e9c53279c497" />

---

### Assignment 18 – Department-wise Highest Salary Employee

### Question:
Find the highest-paid employee in each department.

### Code:

result = df.loc[
    df.groupby("Department")["Salary"].idxmax()
]

print(result)

### Output
<img width="927" height="612" alt="image" src="https://github.com/user-attachments/assets/f18dc05b-e38c-457f-aa2a-84b22f280b54" />

---

### Assignment 19 – Employees with More Projects

### Question:
Display employees who completed more than 15 projects.

### Code:

print(df[df["ProjectsCompleted"] > 15])

### Output
<img width="817" height="752" alt="image" src="https://github.com/user-attachments/assets/4417877a-4e07-4ceb-aaae-04c71381a8ab" />

---

### Assignment 20 – Mini Project

### Question:
Create an Employee Management Report System that loads the dataset, calculates bonus, categorizes performance, ranks employees, performs department-wise salary analysis, and exports the final report.

### Code:

import pandas as pd

df = pd.read_csv("employees.csv")

df["Bonus"] = df["Salary"] * 0.10
df["TotalSalary"] = df["Salary"] + df["Bonus"]

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

df["Rank"] = df["Salary"].rank(ascending=False)

dept_analysis = df.groupby("Department")["Salary"].mean()

print(dept_analysis)

df.to_csv("final_employee_report.csv", index=False)

print("Report Generated Successfully")

### Output
<img width="311" height="163" alt="image" src="https://github.com/user-attachments/assets/2b6abcb5-4a92-4fb9-a24e-b9d49e1188a8" />

