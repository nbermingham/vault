## Overview
**Regression** is a type of supervised learning in [[Machine Learning]] used to predict continuous outcomes based on input features. Unlike [[Classification]], which deals with discrete labels, regression models output numerical values, making it a cornerstone in tasks such as forecasting, trend analysis, and risk assessment.

Regression is widely applied in fields like finance, healthcare, marketing, and engineering for predictive modeling.

---

## Key Concepts

### **1. Linear Regression**
- Models the relationship between the target variable ($y$) and input features ($x$) as a linear equation:
  $$
  y = \beta_0 + \beta_1 x + \epsilon
  $$
  Where:
  - $\beta_0$: Intercept.
  - $\beta_1$: Slope of the line.
  - $\epsilon$: Error term.
- Examples:
  - Predicting house prices based on size.
  - Estimating sales based on advertising spend.

### **2. Polynomial Regression**
- Extends [[Linear Regression]] by adding polynomial terms to model non-linear relationships:
  $$
  y = \beta_0 + \beta_1 x + \beta_2 x^2 + \dots + \beta_n x^n + \epsilon
  $$

### **3. Logistic Regression**
- Despite the name, it’s a classification algorithm. Outputs probabilities for binary or multi-class classification.

### **4. Ridge and Lasso Regression**
- Regularized regression techniques to reduce overfitting:
  - [[Ridge Regression]]: Adds $L2$ penalty.
  - [[Lasso Regression]]: Adds $L1$ penalty, performing feature selection.

### **5. Non-Linear Regression**
- Models complex relationships where linear assumptions fail.

### **6. Generalized Linear Models (GLMs)**
- Extends [[Linear Regression]] to handle different types of dependent variables, such as Poisson or binomial distributions.

---

## Applications

1. **Forecasting**:
   - Predicting future trends, such as stock prices or weather conditions.
2. **Risk Assessment**:
   - Estimating risks in credit scoring or insurance claims.
3. **Optimization**:
   - Modeling relationships to optimize resource allocation.
4. **Healthcare**:
   - Predicting patient outcomes based on clinical data.
5. **Marketing**:
   - Estimating customer lifetime value or sales impact.

---

## Metrics for Evaluation

1. **[[Mean Squared Error]] (MSE)**:
   - Measures average squared error between predicted and actual values.
2. **[[Mean Absolute Error (MAE)]]**:
   - Averages the absolute differences between predicted and actual values.
3. **[[R-Squared]]**:
   - Explains the proportion of variance in the target variable captured by the model.

---

## Techniques

1. **Feature Scaling**:
   - Standardize features to improve model performance.
2. **Feature Selection**:
   - Use techniques like [[Lasso Regression]] or [[Recursive Feature Elimination (RFE)]] to select relevant features.
3. **Cross-Validation**:
   - Evaluate model performance on unseen data.
4. **Regularization**:
   - Prevent overfitting by adding penalties to model coefficients.

---

## Advantages

1. **Interpretability**:
   - Models like [[Linear Regression]] provide coefficients that are easy to interpret.
2. **Flexibility**:
   - Handles both simple linear relationships and complex non-linear dependencies.
3. **Widely Applicable**:
   - Used across industries for numerous predictive tasks.

---

## Disadvantages

1. **Assumptions**:
   - Many regression models assume linear relationships or normality, which may not hold.
2. **Overfitting**:
   - Complex models can overfit small datasets without proper regularization.
3. **Sensitive to Outliers**:
   - Outliers can disproportionately influence regression models.

---

## Related Topics

- [[Linear Regression]]: The simplest form of regression analysis.
- [[Polynomial Regression]]: Extends linear regression for non-linear relationships.
- [[Logistic Regression]]: A classification technique based on regression concepts.
- [[Ridge Regression]]: Regularized regression to reduce overfitting.
- [[Lasso Regression]]: Performs feature selection by shrinking coefficients to zero.
- [[Gradient Descent]]: Optimization algorithm for training regression models.

---

## Aliases
- Regression Analysis
- Predictive Regression
- Regression Modeling

---

## Tags
#regression #machinelearning #datascience #predictivemodeling #supervisedlearning

---

## Links to Explore
- [[Linear Regression]]: The foundation of most regression techniques.
- [[Ridge Regression]]: Learn about regularization for continuous prediction.
- [[Gradient Descent]]: Explore how regression coefficients are optimized.
- [[Mean Squared Error]]: Key metric for evaluating regression performance.
- [[Lasso Regression]]: Understand feature selection in regression.