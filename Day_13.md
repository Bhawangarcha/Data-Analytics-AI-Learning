# 📊 Matplotlib and Seaborn

A beginner-friendly guide to **Matplotlib** and **Seaborn**, two of the most widely used Python libraries for data visualization. This repository introduces the basic concepts, syntax, chart types, customization techniques, and best practices for creating meaningful visualizations in Python.

---

# 📖 Introduction

Data visualization is an important step in data analysis. It helps transform raw data into charts and graphs, making it easier to identify trends, patterns, relationships, and outliers.

This repository focuses on two popular visualization libraries:

- **Matplotlib**
- **Seaborn**

---

# 📚 Matplotlib

Matplotlib is a powerful Python library used for creating static, animated, and interactive visualizations. It provides complete control over chart customization and is suitable for creating publication-quality graphs.

### Import

```python
import matplotlib.pyplot as plt
```

### Features

- Static, animated, and interactive plots
- Highly customizable
- Supports a wide variety of charts
- Works seamlessly with NumPy and Pandas
- Save figures in multiple formats

---

# 📚 Seaborn

Seaborn is a high-level visualization library built on top of Matplotlib. It provides attractive default styles and simplifies the creation of statistical graphics with less code.

### Import

```python
import seaborn as sns
```

### Features

- Attractive default themes
- Easy statistical visualizations
- Built-in color palettes
- Works directly with Pandas DataFrames
- Less code compared to Matplotlib

---

# ⚙️ Basic Setup

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

sns.set_style("whitegrid")
```

---

# 📈 Visualization Techniques

## 📉 Line Chart

### Purpose

Used to display trends or changes over time.

### Common Uses

- Stock prices
- Temperature trends
- Monthly sales

---

## 📊 Bar Chart

### Purpose

Used to compare different categories.

### Common Uses

- Product sales
- Student marks
- Population comparison

---

## 📋 Horizontal Bar Chart

### Purpose

Used when category names are long and easier to read horizontally.

---

## 📶 Histogram

### Purpose

Displays the distribution of numerical data.

### Common Uses

- Exam scores
- Age distribution
- Data spread analysis

---

## 🔴 Scatter Plot

### Purpose

Shows the relationship between two numerical variables.

### Common Uses

- Height vs Weight
- Advertising vs Sales
- Correlation Analysis

---

## 📦 Box Plot

### Purpose

Displays data distribution and detects outliers.

### Important Terms

- Minimum
- First Quartile (Q1)
- Median
- Third Quartile (Q3)
- Maximum
- Outliers

### Common Uses

- Outlier detection
- Comparing distributions
- Statistical summaries

---

## Heatmap

### Purpose

Visualizes matrix-style data using colors.

### Common Uses

- Correlation matrices
- Feature relationships
- Confusion matrices

---

# Common Customization Options

Matplotlib and Seaborn allow various customization options to improve chart readability.

- Chart Title
- X-axis Label
- Y-axis Label
- Figure Size
- Legends
- Grid
- Save Figure

Example:

```python
plt.title("Chart Title")
plt.xlabel("X Label")
plt.ylabel("Y Label")
plt.legend()
plt.grid(True)
plt.savefig("chart.png")
```

---

# Matplotlib vs Seaborn

| Feature | Matplotlib | Seaborn |
|----------|------------|----------|
| Level | Low-level | High-level |
| Customization | Extensive | Easier Styling |
| Statistical Plots | Basic | Advanced |
| Default Design | Simple | Attractive |
| Ease of Use | More Code | Less Code |

---

# 🚀 Applications

Matplotlib and Seaborn are widely used in:

- Data Analysis
- Exploratory Data Analysis (EDA)
- Machine Learning
- Business Intelligence
- Scientific Research
- Financial Analysis
- Dashboard Development

---

# 🎯 Learning Outcomes

After studying this repository, you will be able to:

- Understand the basics of data visualization.
- Create professional charts using Matplotlib.
- Build attractive statistical plots using Seaborn.
- Customize charts with titles, labels, legends, and grids.
- Detect outliers using box plots.
- Analyze relationships using scatter plots.
- Visualize correlations using heatmaps.
- Apply visualization techniques in real-world projects.

---

