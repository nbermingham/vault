## Overview
**Linear Models** are a class of machine learning models that establish a linear relationship between input features ($X$) and the target variable ($y$). They are widely used in both [[Regression]] and [[Classification]] tasks due to their simplicity, interpretability, and efficiency. Linear models predict the target variable as a weighted sum of the input features, optionally adding a bias term.

---

## Key Concepts

### **1. General Form**
The general equation for a linear model is:
$$
y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \dots + \beta_p x_p + \epsilon
$$
Where:
- $y$: Target variable.
- $x_i$: Input features.
- $\beta_i$: Model coefficients (weights).
- $\beta_0$: Intercept (bias term).
- $\epsilon$: Error term.

### **2. Applications**
- **[[Regression]]**:
  - Predict continuous outcomes (e.g., housing prices, stock values).
- **[[Classification]]**:
  - Assign categorical labels (e.g., spam vs. not spam).
  - Example: [[Logistic Regression]] for binary or multi-class classification.

### **3. Assumptions**
Linear models often rely on the following assumptions:
1. **Linearity**:
   - The relationship between features and the target is linear.
2. **Independence**:
   - Observations are independent of each other.
3. **Homoscedasticity**:
   - Constant variance of errors.
4. **Normality**:
   - Errors are normally distributed (mostly for regression).

---

## Variants of Linear Models

### **1. Linear Regression**
- Predicts continuous values.
- Minimizes the [[Mean Squared Error (MSE)]] to fit a line to the data.

### **2. Logistic Regression**
- Used for binary and multi-class [[Classification]].
- Uses the [[Sigmoid Function]] to map predictions to probabilities.

### **3. Ridge Regression**
- Adds $L2$ regularization to reduce overfitting.
- Penalizes large coefficients: $$\lambda \sum_{i=1}^p \beta_i^2$$.

### **4. Lasso Regression**
- Adds $L1$ regularization for feature selection.
- Shrinks irrelevant coefficients to zero: $$\lambda \sum_{i=1}^p |\beta_i|$$.

### **5. Elastic Net**
- Combines $L1$ (Lasso) and $L2$ (Ridge) penalties for balanced regularization.

### **6. Generalized Linear Models (GLMs)**
- Extends linear models for non-normal distributions (e.g., Poisson regression for count data).

---

## Advantages

1. **Interpretability**:
   - Coefficients provide direct insights into the relationship between features and the target.
2. **Efficiency**:
   - Computationally fast to train and predict, even with large datasets.
3. **Scalability**:
   - Suitable for high-dimensional data.
4. **Regularization**:
   - Easily incorporates penalties like $L1$ and $L2$ to improve generalization.

---

## Disadvantages

1. **Linearity Assumption**:
   - Assumes a linear relationship, which may not hold for complex datasets.
2. **Sensitivity to Outliers**:
   - Outliers can disproportionately affect the model.
3. **Feature Engineering**:
   - Requires careful preprocessing (e.g., [[Feature Scaling]], handling multicollinearity).

---

## Applications

1. **Predictive Modeling**:
   - Forecasting trends, such as housing prices or stock values.
2. **Medical Research**:
   - Analyzing the relationship between risk factors and outcomes.
3. **Marketing**:
   - Predicting customer lifetime value or churn.
4. **Text Classification**:
   - Using [[Logistic Regression]] for spam detection or sentiment analysis.

---

## Related Topics

- [[Ridge Regression]]: Handles multicollinearity and reduces overfitting.
- [[Lasso Regression]]: Performs feature selection through regularization.
- [[Elastic Net]]: Combines Ridge and Lasso for balanced regularization.
- [[Gradient Descent]]: Optimization algorithm used in training linear models.
- [[Feature Scaling]]: Essential preprocessing step for linear models.

---

## Aliases
- Linear Models
- Linear Predictive Models
- Linear Regression Models

---

## Tags
#linear-models #machinelearning #regression #classification #regularization #datascience

---

## Links to Explore
- [[Logistic Regression]]: A linear model for classification tasks.
- [[Ridge Regression]]: Explore regularization techniques for linear models.
- [[Gradient Descent]]: Learn how coefficients are optimized.
- [[Feature Scaling]]: Understand its importance in linear models.
- [[Elastic Net]]: A hybrid approach to regularization.