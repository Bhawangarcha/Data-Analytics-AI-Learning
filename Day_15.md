````markdown
# 🤖 Machine Learning Basics

# 📖 Introduction

Machine Learning (ML) is a branch of Artificial Intelligence (AI) that enables computers to learn patterns from data and make predictions or decisions without being explicitly programmed for every task.

### Simple Definition

**Machine Learning = Learning from data to improve performance automatically.**

### Real-Life Examples

- Spam Email Detection
- Netflix Recommendations
- Face Recognition
- Voice Assistants
- Self-driving Cars
- Fraud Detection



---

# 📚 Types of Machine Learning

Machine Learning is mainly divided into three categories.

## 1️⃣ Supervised Learning

Supervised Learning uses **labeled data** to train a model. The model learns the relationship between input and output data and predicts results for new inputs.

### Common Algorithms

- Linear Regression
- Logistic Regression
- Decision Trees
- Support Vector Machine (SVM)
- Random Forest

### Applications

- House Price Prediction
- Disease Diagnosis
- Email Spam Detection
- Student Result Prediction



---

## 2️⃣ Unsupervised Learning

Unsupervised Learning works with **unlabeled data** and finds hidden patterns or groups within the dataset.

### Common Algorithms

- K-Means Clustering
- Hierarchical Clustering
- Principal Component Analysis (PCA)

### Applications

- Customer Segmentation
- Pattern Discovery
- Data Compression



---

## 3️⃣ Reinforcement Learning

Reinforcement Learning trains an **agent** to interact with an environment using rewards and penalties to improve its decisions over time.

### Applications

- Robot Navigation
- Game Playing AI
- Autonomous Vehicles

### Key Terms

- Agent
- Environment
- Reward
- Action


---

# 🔄 Machine Learning Workflow

The basic workflow of a Machine Learning project is:

```text
Collect Data
      ↓
Clean Data
      ↓
Split Dataset
      ↓
Train Model
      ↓
Test Model
      ↓
Evaluate Performance
      ↓
Deploy Model
```

:contentReference[oaicite:5]{index=5}

---

# 📘 Important Terminology

## Dataset

A collection of data used for training and testing a machine learning model.

## Features

Input variables used to make predictions.

**Examples**

- House Size
- Number of Rooms

## Label (Target)

The output variable that the model predicts.

**Example**

- House Price

## Training Data

Used to train the machine learning model.

## Testing Data

Used to evaluate the model's performance.



---

# Common Machine Learning Algorithms

## Linear Regression

- Predicts continuous numerical values.
- Example: Salary Prediction, House Price Prediction.

### Formula

```
y = mx + b
```

---

## Logistic Regression

- Used for classification problems.
- Output is generally **0 or 1**.

### Examples

- Spam Detection
- Pass or Fail Prediction

---

## Decision Tree

A tree-like model used for decision-making.

### Advantages

- Easy to understand
- Handles categorical data

### Disadvantages

- Can overfit the training data

---

## Random Forest

A collection of multiple decision trees that improves prediction accuracy and reduces overfitting.

:contentReference[oaicite:7]{index=7}

---

# Overfitting vs Underfitting

## Overfitting

A model that memorizes the training data and performs poorly on new data.

### Signs

- High Training Accuracy
- Low Testing Accuracy

---

## Underfitting

A model that is too simple and performs poorly on both training and testing data.

:contentReference[oaicite:8]{index=8}

---

# 📊 Evaluation Metrics

## Regression Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Classification Metrics

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Confusion Matrix Terms

- True Positive (TP)
- True Negative (TN)
- False Positive (FP)
- False Negative (FN)

:contentReference[oaicite:9]{index=9}

---

# Bias-Variance Tradeoff

## Bias

Error caused by overly simple assumptions.

## Variance

Error caused by excessive sensitivity to training data.

### Goal

Maintain a balance between Bias and Variance for better model performance.

:contentReference[oaicite:10]{index=10}

---

# 🛠️ Feature Engineering

Feature Engineering improves the quality of input features for better model performance.

### Techniques

- Encoding Categorical Data
- Feature Scaling
- Feature Selection

---

# 📏 Feature Scaling

Feature Scaling normalizes data values so that features with larger ranges do not dominate smaller ones.

### Methods

- Standardization
- Normalization

:contentReference[oaicite:11]{index=11}

---

# 🐍 Common Python Libraries

| Library | Purpose |
|----------|---------|
| NumPy | Numerical Operations |
| Pandas | Data Analysis |
| Matplotlib | Data Visualization |
| Scikit-learn | Machine Learning |
| TensorFlow | Deep Learning |
| PyTorch | Deep Learning |



---

# 💻 Steps to Build a Simple ML Model

```python
from sklearn.linear_model import LinearRegression

model = LinearRegression()

model.fit(X_train, y_train)

predictions = model.predict(X_test)
```


---

# 🌍 Applications of Machine Learning

Machine Learning is widely used in:

- Healthcare
- Banking
- E-commerce
- Cybersecurity
- Agriculture
- Education
- Transportation



---

# ✅ Advantages

- Automates repetitive tasks
- Improves prediction accuracy
- Handles large amounts of data
- Learns continuously from data

:contentReference[oaicite:15]{index=15}

---

# ⚠️ Limitations

- Requires large datasets
- Can be biased
- Computationally expensive
- Difficult to interpret complex models

:contentReference[oaicite:16]{index=16}

---

# 🔍 AI vs ML vs Deep Learning

| Artificial Intelligence | Machine Learning | Deep Learning |
|-------------------------|------------------|---------------|
| Broad concept | Subset of AI | Subset of ML |
| Mimics human intelligence | Learns from data | Uses neural networks |


---

