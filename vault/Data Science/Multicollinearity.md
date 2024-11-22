## Overview
**Multicollinearity** occurs when two or more independent variables in a regression model are highly correlated, meaning they contain redundant information. This can distort the estimation of regression coefficients, making it difficult to assess the individual effect of each variable on the dependent variable.

Multicollinearity is a common issue in [[Regression]] models, particularly in datasets with many features, and can lead to unstable models with high variance in coefficient estimates.

---

## Key Characteristics

1. **High Correlation Between Features**:
   - Multicollinearity arises when independent variables are strongly correlated, leading to redundancy.
2. **Unstable Coefficient Estimates**:
   - Coefficients may change dramatically with slight modifications to the data.
3. **Non-Unique Solutions**:
   - Severe multicollinearity can make the regression equation ill-posed, leading to non-unique solutions.

---

## Types of Multicollinearity

1. **Perfect Multicollinearity**:
   - When one feature is an exact linear combination of others.
   - Example: If $X_3 = X_1 + X_2$.
2. **Imperfect Multicollinearity**:
   - When features are highly correlated but not perfectly linearly dependent.

---

## Causes

1. **Redundant Features**:
   - Including variables with similar meanings or relationships (e.g., height in inches and height in centimeters).
2. **High-Dimensional Data**:
   - A large number of features relative to the number of samples increases the likelihood of correlated features.
3. **Feature Engineering**:
   - Creating derived features (e.g., polynomial terms) can inadvertently introduce correlations.

---

## Problems Caused by Multicollinearity

1. **Unreliable Coefficients**:
   - Regression coefficients may have high variance, making them unreliable for interpretation.
2. **Reduced Model Interpretability**:
   - It becomes hard to determine which feature has the strongest relationship with the target.
3. **Inflated Standard Errors**:
   - Standard errors of coefficients increase, reducing statistical significance.
4. **Overfitting**:
   - High correlation among features can lead to overfitting, especially in models with weak regularization.

---

## Detection Methods

1. **Correlation Matrix**:
   - Compute the pairwise [[Correlation|Correlation Coefficient]] between features and look for values close to 1 or -1.
2. **Variance Inflation Factor (VIF)**:
   - Measures the degree of multicollinearity. A VIF value greater than 5 or 10 indicates high multicollinearity.
   $$
   VIF_j = \frac{1}{1 - R_j^2}
   $$
   Where $R_j^2$ is the $R^2$ value of the $j$-th feature regressed on all other features.
3. **Eigenvalues of Covariance Matrix**:
   - Very small eigenvalues indicate multicollinearity.

---

## Solutions to Multicollinearity

1. **Remove Redundant Features**:
   - Drop one of the correlated variables identified via the correlation matrix or VIF.
2. **Regularization**:
   - Apply [[Ridge Regression]] (L2 regularization) or [[Lasso Regression]] (L1 regularization) to reduce multicollinearity's impact.
3. **Principal Component Analysis (PCA)**:
   - Use [[Dimensionality Reduction]] to transform correlated features into uncorrelated components.
4. **Increase Sample Size**:
   - Adding more data can reduce the instability caused by multicollinearity.
5. **Domain Knowledge**:
   - Use subject matter expertise to select the most relevant features.

---

## Applications

1. **Regression Models**:
   - Multicollinearity is a significant concern in linear, logistic, and generalized linear models.
2. **Feature Engineering**:
   - Detect and handle multicollinearity when creating new features.
3. **Economic Modeling**:
   - In [[Econometrics]], multicollinearity often arises in models of related economic indicators.

---

## Related Topics

- [[Regression]]: Multicollinearity affects the reliability of regression models.
- [[Feature Selection]]: Techniques to eliminate redundant features and reduce multicollinearity.
- [[Dimensionality Reduction]]: Reduces feature redundancy by transforming correlated features.
- [[Regularization]]: Mitigates multicollinearity using penalty terms.

---

## Aliases
- Multicollinearity
- Collinearity

---

## Tags
#multicollinearity #regression #featureselection #machinelearning #dimensionalityreduction

---

## Links to Explore
- [[Regression]]: Learn how multicollinearity impacts regression models.
- [[Feature Selection]]: Explore techniques to identify and handle redundant features.
- [[Ridge Regression]]: Discover how L2 regularization mitigates multicollinearity.
- [[Principal Component Analysis (PCA)]]: Transform correlated features into uncorrelated components.
- [[Correlation]]: Understand the relationships that lead to multicollinearity.