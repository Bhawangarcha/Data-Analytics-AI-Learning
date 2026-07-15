### Pandas Assignments on Student Marks Dataset 

### Assignment 1 – Load Dataset

### Question:
Load the student_marks.csv dataset using Pandas and display:
- First 5 rows
- Last 5 rows
- Shape of the dataset
- Column names

### Code: 
import pandas as pd
df = pd.read_csv("/content/student_data_converted.csv")
print(df.head())
print(df.tail())
print(df.shape)
print(df.columns)

### Output
<img width="846" height="727" alt="image" src="https://github.com/user-attachments/assets/13bd13fa-63e8-40ab-b069-f0e94cec2062" />

---

### Assignment 2 – Dataset Information

### Question:
Check the following information in the dataset:
- Missing values
- Duplicate rows
- Data types of all columns

### Code:
print(df.isnull().sum())
print(df.duplicated().sum())
print(df.info())

### Output
<img width="616" height="598" alt="image" src="https://github.com/user-attachments/assets/917f2b45-a14e-4057-bf9f-6d30335f0a79" />

---

### Assignment 3 – Create Total Marks

### Question:
Create a new column named Total by adding the marks of the following subjects:
- Maths

- Science

- English

- History

### Code:
df["Total"]= df["Maths"] + df["Science"] + df["English"] + df["History"]
print(df["Total"])

### Output
<img width="707" height="731" alt="image" src="https://github.com/user-attachments/assets/6d2a61ab-4965-4acf-9a91-6c7ba9c37d08" />

---

### Assignment 4 – Calculate Average

### Question:
Create a new column named Average using the total marks obtained by each student.

### Code:
df["Average"] = df["Total"]/4
print(df["Average"])

### Output
<img width="567" height="750" alt="image" src="https://github.com/user-attachments/assets/1f3fb937-2ba4-4e1d-a7c9-7dfd925c162b" />

---

### Assignment 5 – Calculate Percentage

### Question:
Create a new column named Percentage, assuming the total marks are out of 400.

### Code:
df["Percentage"] = (df["Total"]/400)*100
print(df["Percentage"])

### Output
<img width="500" height="752" alt="image" src="https://github.com/user-attachments/assets/7eac78d8-90a6-4146-aa61-4fd180000d5d" />

---

### Assignment 6 – Highest and Lowest Marks

### Question:
Find:
- The highest marks in each subject
- The lowest marks in each subject

### Code: 
print(df["Maths"].max())
print(df["Science"].max())
print(df["English"].max())
print(df["History"].max())
print(df["Maths"].min())
print(df["Science"].min())
print(df["English"].min())
print(df["History"].min())

### Output
<img width="402" height="365" alt="image" src="https://github.com/user-attachments/assets/0758e506-b910-48bf-8567-1b068e334360" />

---

### Assignment 7 – Highest and Lowest Scoring Students

### Question:
Find the student who scored:
- The highest total marks
- The lowest total marks

### Code:
print(df["Total"].max())
print(df["Total"].min())

### Output
<img width="412" height="147" alt="image" src="https://github.com/user-attachments/assets/01b4cce2-1d83-4388-ba5b-0d40f7423902" />

---

### Assignment 8 – Filter Students

### Question:
Display:
- Students who scored above 90 in Maths
- Students who scored below 75 in Science
- Students who scored above 85 in all subjects

### Code:
print(df[df["Maths"]>90])
print(df[df["Science"]<75])
print(df[(df[["Maths", "Science", "English", "History"]]>85).all(axis=1)])

### Output

<img width="692" height="583" alt="image" src="https://github.com/user-attachments/assets/f6d495a8-1f86-4fe4-b223-39b85c35d64d" />

<img width="670" height="677" alt="image" src="https://github.com/user-attachments/assets/002059d4-4a85-4208-9b10-74a9e0ed3b7c" />

---

### Assignment 9 – Sort Students

### Question:
Sort the students:
- By Total marks in descending order
- By Age in ascending order

### Code:
print(df.sort_values(by="Total", ascending=False))
print(df.sort_values(by=("Age"), ascending=True))

### Output

<img width="722" height="700" alt="image" src="https://github.com/user-attachments/assets/e3e6c5d4-8378-4696-8233-99824c05bd06" />

<img width="725" height="733" alt="image" src="https://github.com/user-attachments/assets/7e57d89a-250a-4b00-ab0b-bbc63f8553e2" />

---

### Assignment 10 – Top and Bottom Students

### Question:
Display:
- Top 5 students based on total marks
- Bottom 5 students based on total marks

### Code:
print(df.sort_values(by="Total", ascending=True).head())
print(df.sort_values(by="Total", ascending=False).tail(5))

### Output

<img width="683" height="558" alt="image" src="https://github.com/user-attachments/assets/fcb8b32d-c89b-4029-91c3-e20f16ab2716" />

---

### Assignment 11 – Assign Grades

### Question:
Create a new column named Grade using the following criteria:

- A → 90 and above
- B → 75–89
- C → 60–74
- D → Below 60

### Code:
def category(Total):
  if Total >= 90:
    return "Grade A"
  elif Total >= 75 or Total<=89 :
    return "Grade B"
  elif Total >= 60 & Total <= 74:
    return "Grade C"
  else:
    return "Fail"
df["Grade"] = df["Total"].apply(category)
print(df["Grade"])

### Output

<img width="652" height="738" alt="image" src="https://github.com/user-attachments/assets/406fc1b2-4b8d-4b77-9587-4c8a3b9bfd19" />

---

### Assignment 12 – Pass/Fail Result

Question:
Create a new column named Result using the following criteria:
- Pass if Average ≥ 40
- Fail otherwise

### Code:
def category(Average):
  if Average >= 40:
    return "Pass"
  else:
    return "Fail"
df["Pass/Fail"] = df["Average"].apply(category)
print(df["Pass/Fail"])

### Output

<img width="991" height="760" alt="image" src="https://github.com/user-attachments/assets/dc04bad6-e9ef-4f84-be37-af23deb6753c" />

---

### Assignment 13 – Student Count

Question:
Find:
- Total number of students
- Number of students age-wise
- Number of students in each grade

### Code:
print(df["Grade"].value_counts())
print(df["Pass/Fail"].value_counts())
print(df["Age"].value_counts())

### Output

<img width="495" height="275" alt="image" src="https://github.com/user-attachments/assets/19065a7f-11db-4b29-ad56-4b0fcfd9df11" />

---

Assignment 14 – Subject-wise Average

Question:
Find the average marks of the following subjects:

Maths

Science

English

History



---

Assignment 15 – Correlation

Question:
Find the correlation between all subject marks.


---

Assignment 16 – Filter Students by Performance

Question:
Display:

Students whose total marks are above the class average

Students whose percentage is above 85%



---

Assignment 17 – Subject Toppers

Question:
Find:

The topper in each subject

The overall class topper



---

Assignment 18 – Student Ranking

Question:
Create a new column named Rank based on students' total marks.


---

Assignment 19 – Export Dataset

Question:
Export the updated dataset into a new CSV file named processed_students.csv.


---

Assignment 20 – Mini Student Report System

Question:
Create a Student Report System that:

Loads the student dataset

Calculates Total, Average, and Percentage

Assigns Grades

Assigns Pass/Fail status

Ranks students based on Total marks

Exports the final report as a CSV file named final_student_report.csv
