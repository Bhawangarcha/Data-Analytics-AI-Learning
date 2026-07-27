# Assignment 1 – Import Libraries and Apply Style

## Question

Import the required libraries and apply the **whitegrid** style using Seaborn.

## Code

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

```

### Explanation

* `matplotlib.pyplot` is used to create plots.
* `seaborn` provides attractive visualization styles.

---

# Assignment 2 – Line Chart using Matplotlib

## Question

Create a line chart showing monthly sales using Matplotlib.

## Code

```python
days = [1,2,3,4,5]
temperature = [30,32,31,35,36]
plt.plot(days,temperature,marker='o',color='blue')
plt.title("Line Chart")
plt.xlabel("Days")
plt.ylabel("Temperature")
plt.grid(True)
plt.show()
```

## Output
<img width="837" height="530" alt="image" src="https://github.com/user-attachments/assets/b2268c0b-b43e-4ae5-b1bc-8b20799301b0" />



### Explanation

The `plot()` function is used to create a line graph. Titles, axis labels, and grid lines improve chart readability.

---

# Assignment 3 – Line Chart using Seaborn

## Question

Create the same line chart using Seaborn.

## Code

```python
months = ['Jan','Feb', 'Mar', 'Apr', 'May']
profit = [2000, 2500, 2200, 2800, 3000]
sns.lineplot(x = months, y = profit, marker = 'o')
plt.title("Seaborn Line Chart")
plt.show()
```

## Output
<img width="810" height="490" alt="image" src="https://github.com/user-attachments/assets/61f4f00e-4b43-4f67-8249-cf7fc91f10eb" />

### Explanation

`lineplot()` creates an attractive statistical line graph with minimal code.

---

# Assignment 4 – Multiple Line Chart

## Question

Plot two product sales on the same graph.

## Code

```python
# Q4
subjects = ['Maths', 'Science', 'English', 'Computer', 'History']
rahul = [78,85,80,90,75]
priya = [82,88,84,86,79]
plt.plot(subjects, rahul, label ='rahul', marker = 'o', color = 'blue')
plt.plot(subjects, priya, label = 'priya', marker = 'o', color = 'Purple')
plt.title("Line Chart")
plt.xlabel("Subjects")
plt.ylabel("Marks")
plt.legend()
plt.show()
```

## Output

<img width="812" height="525" alt="image" src="https://github.com/user-attachments/assets/99312205-e433-4612-85c8-25e23c2b9920" />

### Explanation

Multiple calls to `plot()` allow multiple datasets to be displayed on the same graph.

---

# Assignment 5 – Bar Chart using Matplotlib

## Question

Create a bar chart showing the number of students in different departments.

## Code

```python
products = ['Laptop', 'Mouse', 'Keyboard', 'Monitor']
sales = [90,85,95,88]
plt.bar(products, sales, color = 'green')
plt.title("Bar Chart")
plt.xlabel("Products")
plt.ylabel("Sales")
plt.show()
```

## Output

<img width="825" height="533" alt="image" src="https://github.com/user-attachments/assets/2854c8d5-3c87-4a3a-b4a5-26f484b94ca4" />


### Explanation

`bar()` creates vertical bars, making it easy to compare values across categories.

---

## Assignment 6 – Bar Chart using Seaborn

### Question

Create a **bar chart** showing the sales of different products using **Seaborn**.

### Code

```python
students = ['Aman', 'Riya', 'Karan', 'Siyal']
attendence = [90,85,95,88]
sns.barplot(x = students, y = attendence)
plt.title("Seaborn Bar Chart")
plt.show()
```

### Output

<img width="747" height="546" alt="image" src="https://github.com/user-attachments/assets/0331940e-d4a1-43bf-b442-9032310d25c5" />

### Explanation

* **`sns.barplot()` creates a bar chart to compare values across different categories.**

## Assignment 7 – Horizontal Bar Chart

### Question

Create a **horizontal bar chart** showing the marks obtained by students in different subjects using **Matplotlib**.

### Code

```python
cities = ['Delhi', 'Mumbai', 'Chandigarh', 'Jaipur']
population = [32, 20, 1.2, 4]
plt.barh(population, cities)
plt.title("Horizontal Bar Graph")
plt.xlabel(cities)
plt.ylabel(population)
plt.show()
```

### Output

<img width="703" height="542" alt="image" src="https://github.com/user-attachments/assets/dabef85c-19b5-4500-be7a-3daf86b402de" />

### Explanation

* **`plt.barh()` creates a horizontal bar chart, making it easier to compare categories with long labels.**

---

## Assignment 8 – Histogram using Matplotlib

### Question

Create a **histogram** to display the distribution of students' marks using **Matplotlib**.

### Code

```python
import numpy as np
import matplotlib.pyplot as plt
data = np.random.randn(100)
plt.hist(data, bins = 20, color = 'purple', edgecolor = 'black')
plt.title("Histogram")
plt.xlabel("Value")
plt.ylabel("Frequency")
plt.show()
```

### Output


<img width="742" height="537" alt="image" src="https://github.com/user-attachments/assets/9fe21717-5753-4089-bffc-f15994e52773" />

### Explanation

* **`plt.hist()` displays the frequency distribution of numerical data.**

---

# Assignment 9 – Histogram using Seaborn

### Question

Create a **histogram** using **Seaborn** to visualize the distribution of students' marks.

### Code

```python

import numpy as np
import matplotlib.pyplot as plt
data = np.random.randn(100)
plt.hist(data, bins = 20, color = 'purple', edgecolor = 'black')
plt.title("Histogram")
plt.xlabel("Value")
plt.ylabel("Frequency")
plt.show()
```

### Output


<img width="727" height="535" alt="image" src="https://github.com/user-attachments/assets/87dab32a-97c6-48c5-b474-b28d9d13c5dd" />

### Explanation

* **`sns.histplot()` creates a histogram with attractive default styling.**

---

# Assignment 10 – Seaborn Histogram

### Question

Create a **scatter plot** showing the relationship between students' study hours and marks.

### Code

```python
scores = [45,56,67,78,89,90,76,65,54,88,92,73,69,58]
sns.histplot(data, bins = 30, kde = True)
plt.title("Seaborn Histogram")
plt.show()
```

### Output


<img width="735" height="493" alt="image" src="https://github.com/user-attachments/assets/357793a4-cbcf-481d-9faa-a380d896cfa4" />

### Explanation

* **`plt.scatter()` displays the relationship between two numerical variables.**

---

# Assignment 11 – Scatter Plot using Matplotlib


### Code

```python
hours = [ 1,2,3,4,5,6,7]
marks = [40,45,50,60,65,70,80]
plt.scatter(hours, marks, marker = 'o', color = 'red')
plt.grid(True)
plt.title("Scatter Plot")
plt.xlabel("Hours")
plt.ylabel("Marks")
plt.show()
```

### Output


<img width="780" height="508" alt="image" src="https://github.com/user-attachments/assets/65954454-1531-495a-8726-c13de4b7ef93" />



---

# Assignment 12 – Scatter Plot using Seaborn



### Code

```python
advertising = [10, 20, 30, 40, 50]
sales = [100, 150, 200, 260, 300]
plt.scatter(advertising, sales, marker = 'o', color = 'blue')
plt.grid(True)
plt.title("Scatter Plot")
plt.xlabel("Advertising")
plt.ylabel("Sales")
plt.show()
```

### Output


<img width="847" height="521" alt="image" src="https://github.com/user-attachments/assets/71e34fcb-7dff-4c8d-b35c-55a07f782e98" />


---

# Assignment 13 –  Box Plot using Matplotlib


### Code

```python
salary = [25000, 27000, 29000, 31000, 33000, 35000, 100000]
plt.boxplot(salary, labels = ['Salary'])
plt.grid(True)
plt.title("Box Plot")
plt.ylabel("Salary")
plt.show()
```

### Output


<img width="822" height="525" alt="image" src="https://github.com/user-attachments/assets/2a0cba8c-fb92-4912-9d0d-0cf026ef1270" />


---

# Assignment 14 –Box Plot using Seaborn

### Code

```python
ages = [18, 19, 20, 21, 22, 23,24, 60]
sns.boxplot(data = ages)
plt.grid(True)
plt.title("Seaborn Box Plot")
plt.show()
```

### Output


<img width="736" height="482" alt="image" src="https://github.com/user-attachments/assets/74ab73e9-62e4-43ea-ad09-49817e45cc0c" />


---

# Assignment 15 – Heatmap using Seaborn


### Code

```python
matrix = [[5, 8, 2], [7, 3, 6], [9, 1, 4]]
sns.heatmap(matrix, annot = True, cmap = 'coolwarm', fmt = 'g')
plt.title("Seaborn Heatmap")
plt.show()
```

### Output


<img width="688" height="502" alt="image" src="https://github.com/user-attachments/assets/79291afb-b3fe-4d39-b6e1-7ca532511973" />

# Assignment 15 – Correlation Heatmap

### Code
```python
import pandas as pd
df = pd.DataFrame(np.random.rand(10, 10), columns=['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J'])
sns.heatmap(df.corr(), annot=True, cmap='viridis')
plt.title("Correlation Heatmap")
plt.show()
```

### Output'
<img width="740" height="493" alt="image" src="https://github.com/user-attachments/assets/f5e1711a-23d6-48cb-a049-40aa5c5a7cab" />

---
