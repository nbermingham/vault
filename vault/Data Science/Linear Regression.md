## Overview
**Linear Regression** is a fundamental [[Machine Learning]] algorithm used for predictive modeling. It assumes a linear relationship between the input features (independent variables) and the target variable (dependent variable). The goal is to find the best-fitting line that minimizes the error between predicted and actual values.

Linear Regression is commonly used in regression tasks where the target variable is continuous.

---

## Key Concepts

### Model Equation
For a single feature $x$, the relationship is modeled as:
$$
y = \beta_0 + \beta_1 x + \epsilon
$$
Where:
- $y$: Target variable (dependent variable).
- $x$: Feature (independent variable).
- $\beta_0$: Intercept (the value of $y$ when $x = 0$).
- $\beta_1$: Slope of the line (represents the change in $y$ for a unit change in $x$).
- $\epsilon$: Error term (captures the variance not explained by the model).

For multiple features, the equation extends to:
$$
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_n x_n + \epsilon
$$
This is called **Multiple Linear Regression**.

### [[Loss Function]]
Linear Regression minimizes the **[[Mean Squared Error]] (MSE)**:
$$
MSE = \frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2
$$
Where:
- $y_i$: Actual value.
- $\hat{y}_i$: Predicted value.
- $n$: Number of observations.

The optimization process finds the coefficients $\beta_0, \beta_1, \dots, \beta_n$ that minimize this loss.

### Assumptions
Linear Regression makes several key assumptions:
1. **[[Linearity]]**:
   - The relationship between features and the target is linear.
2. **[[Independence]]**:
   - Residuals (errors) are independent of each other.
3. **[[Homoscedasticity]]**:
   - Residuals have constant variance.
4. **[[Normality]]**:
   - Residuals are normally distributed.

---

## Applications

1. **Predictive Modeling**:
   - Forecasting continuous variables like sales, temperature, or stock prices.
2. **[[Feature Importance]]**:
   - Identifies the impact of independent variables on the target variable.
3. **Exploratory Data Analysis (EDA)**:
   - Determines relationships between variables in a dataset.

---

## Advantages

1. **Simplicity**:
   - Easy to understand and implement.
2. **Efficiency**:
   - Computationally inexpensive for small to medium-sized datasets.
3. **Interpretability**:
   - Coefficients directly represent the relationship between features and the target.

---

## Disadvantages

1. **Linearity Assumption**:
   - Poor performance when the relationship between variables is non-linear.
2. **Sensitivity to Outliers**:
   - Outliers can significantly skew the model.
3. **Multicollinearity**:
   - Highly correlated features can distort the model's coefficients.
4. **Underfitting**:
   - May fail to capture complex relationships in the data.

---

## Variants

1. **[[Ridge Regression]]**:
   - Adds $L2$ regularization to reduce overfitting.
2. **[[Lasso Regression]]**:
   - Adds $L1$ regularization to perform feature selection.
3. **[[Polynomial Regression]]**:
   - Extends Linear Regression to capture non-linear relationships by introducing polynomial terms.
4. **[[Logistic Regression]]**:
   - A classification algorithm that builds on the concepts of Linear Regression.

---

## Example

### [[Simple Linear Regression]]
Given a dataset:
| $x$ (Study Hours) | $y$ (Exam Score) |
|--------------------|------------------|
| 1                  | 50               |
| 2                  | 55               |
| 3                  | 60               |
| 4                  | 65               |
| 5                  | 70               |

The Linear Regression model predicts:
$$
y = 45 + 5x
$$
- For $x = 3$, the predicted score is:
  $$
  \hat{y} = 45 + 5(3) = 60
  $$

---

## Related Topics

- [[Mean Squared Error]]: The primary loss function for Linear Regression.
- [[Ridge Regression]]: Regularized Linear Regression for reducing overfitting.
- [[Polynomial Regression]]: Captures non-linear relationships using polynomial terms.
- [[Gradient Descent]]: Optimization technique for finding regression coefficients.
- [[Overfitting]]: A common issue in high-variance models.

---

## Aliases
- Linear Regression
- Simple Linear Regression
- Multiple Linear Regression
- Ordinary Least Squares (OLS)

---

## Tags
#linear-regression #machinelearning #regression #modeling #datascience

---

## Links to Explore
- [[Mean Squared Error]]: Understand the loss function used in Linear Regression.
- [[Ridge Regression]]: Learn about regularization to prevent overfitting.
- [[Gradient Descent]]: Explore optimization techniques for model training.
- [[Polynomial Regression]]: Handle non-linear relationships in data.
- [[Overfitting]]: Understand its impact on model generalization.