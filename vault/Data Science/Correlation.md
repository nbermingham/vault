---
aliases:
  - Correlation Coefficient
  - Variable Correlation
  - variable correlation
---
## Overview
**Correlation** is a statistical measure that quantifies the relationship between two variables. It indicates whether an increase (or decrease) in one variable is associated with an increase (or decrease) in another variable. Correlation plays a key role in [[Feature Engineering]], [[Feature Selection]], and understanding data relationships in [[Machine Learning]] and [[Data Analysis]].

The value of correlation lies between $-1$ and $1$, where:
- $1$: Perfect positive relationship.
- $0$: No relationship.
- $-1$: Perfect negative relationship.

---

## Types of Correlation

### 1. **[[Pearson Correlation]]**
- Measures the linear relationship between two variables.
- Formula:
  $$
  r = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^n (x_i - \bar{x})^2 \sum_{i=1}^n (y_i - \bar{y})^2}}
  $$
- Assumes:
  - Variables are continuous.
  - Linear relationship between variables.

### 2. **[[Spearman Correlation]]**
- Measures the monotonic relationship (rank-based) between two variables.
- Useful for non-linear relationships.

### 3. **[[Kendall’s Tau]]**
- Measures the ordinal association between two variables, based on the concordance of data rankings.

---

## Applications

1. **[[Feature Selection]]**:
   - Correlation is used to identify redundant features with high inter-feature correlation, which can be removed to improve model performance.

2. **[[Multicollinearity Detection]]**:
   - High correlation among independent variables in [[Regression]] tasks may indicate multicollinearity, which can affect model stability.

3. **Exploratory Data Analysis (EDA)**:
   - Correlation matrices are used to visualize relationships between multiple features.

4. **[[Time Series Analysis]]**:
   - Autocorrelation identifies patterns or [[Seasonality]] in time series data.

---

## Advantages

1. **Simple Interpretation**:
   - Easy to compute and understand.
   
2. **Widely Used**:
   - A foundational tool in [[Exploratory Data Analysis (EDA)]].

3. **Versatile**:
   - Can handle both linear (Pearson) and [[monotonic]]  (Spearman) relationships.

---

## Disadvantages

1. **Only Measures Association**:
   - Correlation does not imply causation.
   
2. **Sensitivity to Outliers**:
   - Pearson correlation can be heavily influenced by outliers.
   
3. **Assumes Linear Relationships**:
   - Pearson correlation assumes linearity, which may not always hold.

---

## Tools for Computing Correlation

1. **Python Libraries**:
   - `pandas.corr()`: Computes pairwise correlation of columns.
   - `scipy.stats.pearsonr()`, `spearmanr()`: For Pearson and Spearman correlations.

2. **Visualization**:
   - Heatmaps using `seaborn` or `matplotlib` for correlation matrices.

---

## Related Topics

- [[Feature Selection]]: Correlation is used to remove redundant features.
- [[Exploratory Data Analysis (EDA)]]: Correlation is critical in understanding relationships between features.
- [[Regression]]: Multicollinearity can degrade regression performance.
- [[Dimensionality Reduction]]: Techniques like [[Principal Component Analysis]] reduce dimensionality in highly correlated data.
- [[Time Series Analysis]]: Correlation is used to identify lag-based relationships.
- [[Causation]]: Correlation is often confused with causation, requiring advanced techniques for causal inference.

---

## Aliases
- Correlation
- Correlation Coefficient
- Variable Correlation

---

## Tags
#correlation #statistical-analysis #feature-selection #data-analysis #machinelearning