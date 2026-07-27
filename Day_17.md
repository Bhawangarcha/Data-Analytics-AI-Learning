```markdown
# 📈 Types of Regression in Machine Learning

Regression is a supervised machine learning technique used to predict continuous numerical values based on input features.

---

## 1. Linear Regression

Linear Regression models the relationship between one or more independent variables and a dependent variable using a straight line.

### Formula

\[
y = mx + b
\]

Where:

- **y** = Predicted value
- **m** = Slope
- **x** = Independent variable
- **b** = Intercept

### Applications

- House Price Prediction
- Salary Prediction
- Sales Forecasting

### Advantages

- Simple and easy to implement.
- Fast to train.
- Easy to interpret.

### Disadvantages

- Works only for linear relationships.
- Sensitive to outliers.

---

## 2. Multiple Linear Regression

Multiple Linear Regression predicts the output using two or more independent variables.

### Formula

\[
y = b_0 + b_1x_1 + b_2x_2 + \cdots + b_nx_n
\]

### Applications

- Predicting house prices based on area, number of rooms, and location.
- Student performance prediction.

### Advantages

- Uses multiple features.
- More accurate than simple linear regression.

### Disadvantages

- Can suffer from multicollinearity.
- More complex than simple regression.

---

## 3. Polynomial Regression

Polynomial Regression models nonlinear relationships by fitting a polynomial curve to the data.

### Formula

\[
y = b_0 + b_1x + b_2x^2 + \cdots + b_nx^n
\]

### Applications

- Stock Market Analysis
- Population Growth Prediction
- Weather Forecasting

### Advantages

- Handles nonlinear data.
- More flexible than linear regression.

### Disadvantages

- Can overfit the training data.
- Higher computational complexity.

---

## 4. Ridge Regression

Ridge Regression is a regularized version of linear regression that reduces overfitting by adding an L2 penalty.

### Applications

- High-dimensional datasets
- Predictive analytics
- Financial modeling

### Advantages

- Reduces overfitting.
- Handles multicollinearity.

### Disadvantages

- Does not eliminate unnecessary features completely.

---

## 5. Lasso Regression

Lasso Regression adds an L1 penalty, which can shrink some coefficients to zero and perform feature selection.

### Applications

- Feature Selection
- Medical Data Analysis
- Marketing Analytics

### Advantages

- Reduces overfitting.
- Automatically selects important features.

### Disadvantages

- May remove useful features if the penalty is too high.

---

## 6. Elastic Net Regression

Elastic Net Regression combines both Ridge (L2) and Lasso (L1) regularization.

### Applications

- Large datasets
- Datasets with many correlated features

### Advantages

- Combines the strengths of Ridge and Lasso.
- Handles multicollinearity effectively.

### Disadvantages

- Requires tuning multiple parameters.

---

## 7. Logistic Regression

Although it contains the word **Regression**, Logistic Regression is used for **classification**, not regression.

### Applications

- Email Spam Detection
- Disease Prediction
- Customer Churn Prediction
- Fraud Detection

### Output

- 0 (No)
- 1 (Yes)

### Advantages

- Simple and efficient.
- Works well for binary classification.

### Disadvantages

- Cannot predict continuous values.
- Assumes a linear relationship between features and log odds.

---

# Comparison of Regression Types

| Regression Type | Used For | Output |
|-----------------|----------|--------|
| Linear Regression | Continuous prediction | Numerical Value |
| Multiple Linear Regression | Multiple input features | Numerical Value |
| Polynomial Regression | Nonlinear prediction | Numerical Value |
| Ridge Regression | Reduce overfitting | Numerical Value |
| Lasso Regression | Feature selection | Numerical Value |
| Elastic Net Regression | Combined regularization | Numerical Value |
| Logistic Regression | Classification | Class Label (0/1) |

---

# Conclusion

Regression algorithms are widely used to predict numerical values and analyze relationships between variables. Choosing the right regression technique depends on the nature of the dataset, the relationship between variables, and the problem being solved.
```
