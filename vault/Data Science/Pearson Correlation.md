## Overview
**Pearson Correlation** is a statistical measure that quantifies the strength and direction of the linear relationship between two continuous variables. It is widely used in [[Feature Selection]], [[Exploratory Data Analysis (EDA)]], and [[Regression]] tasks to assess how changes in one variable correspond to changes in another.

The Pearson Correlation coefficient, denoted by $r$, ranges from -1 to 1:
- $r = 1$: Perfect positive correlation.
- $r = -1$: Perfect negative correlation.
- $r = 0$: No linear correlation.

---

## Formula

The Pearson Correlation coefficient is defined as:
$$
r = \frac{\sum_{i=1}^N (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^N (x_i - \bar{x})^2} \sqrt{\sum_{i=1}^N (y_i - \bar{y})^2}}
$$
Where:
- $x_i, y_i$: Individual data points of variables $X$ and $Y$.
- $\bar{x}, \bar{y}$: Mean of $X$ and $Y$.
- $N$: Number of data points.

---

## Key Properties

1. **Symmetry**:
   - $r(X, Y) = r(Y, X)$.
2. **Unitless**:
   - The coefficient is a dimensionless value, making it comparable across datasets.
3. **Linear Relationship**:
   - Measures only linear relationships; it does not capture non-linear associations.

---

## Applications

1. **Feature Selection**:
   - Identify strongly correlated features for inclusion or exclusion in [[Machine Learning]] models.
   - Example: Remove features with high inter-correlation to prevent multicollinearity in [[Linear Regression]].
2. **Exploratory Data Analysis (EDA)**:
   - Detect relationships between variables to guide model design or hypothesis testing.
3. **Data Transformation**:
   - Identify variables that require scaling or transformation based on their relationships.

---

## Advantages

1. **Simplicity**:
   - Easy to compute and interpret.
2. **Identifies Linear Relationships**:
   - Useful for determining how strongly two variables are linearly related.
3. **Widely Applicable**:
   - Can be used across diverse fields, from [[Economics]] to [[Machine Learning]].

---

## Disadvantages

1. **Sensitive to Outliers**:
   - Outliers can significantly distort the correlation coefficient.
2. **Ignores Non-Linear Relationships**:
   - Fails to capture non-linear dependencies between variables.
3. **Assumes Normality**:
   - Assumes the variables are normally distributed, which may not hold in all datasets.

---

## Example

Given two variables:
- $X = [2, 4, 6, 8, 10]$
- $Y = [1, 3, 5, 7, 9]$

1. Compute means: $\bar{x} = 6$, $\bar{y} = 5$.
2. Compute deviations from the mean:
   - $X - \bar{x} = [-4, -2, 0, 2, 4]$
   - $Y - \bar{y} = [-4, -2, 0, 2, 4]$
3. Compute $r$:
   - Numerator: $\sum(X - \bar{x})(Y - \bar{y}) = 40$
   - Denominator: $\sqrt{\sum(X - \bar{x})^2} \cdot \sqrt{\sum(Y - \bar{y})^2} = 40$
   - $r = \frac{40}{40} = 1$, indicating a perfect positive correlation.

---

## Related Topics

- [[Correlation]]: Pearson is a specific type of correlation.
- [[Feature Selection]]: Use Pearson Correlation to identify redundant features.
- [[Multicollinearity]]: Address correlated predictors in regression models.
- [[Regression]]: Evaluate the relationship between independent and dependent variables.
- [[Spearman Correlation]]: An alternative for non-linear or rank-based relationships.

---

## Aliases
- Pearson Correlation
- Pearson Correlation Coefficient
- Linear Correlation Coefficient

---

## Tags
#correlation #statistics #machinelearning #featureselection #EDA

---

## Links to Explore
- [[Correlation]]: Understand the broader concept of relationships between variables.
- [[Feature Selection]]: Explore how correlation guides feature inclusion or exclusion.
- [[Regression]]: Use Pearson Correlation to assess predictor-target relationships.
- [[Spearman Correlation]]: Discover a rank-based alternative to Pearson.
- [[Multicollinearity]]: Learn about handling correlated features in regression models.