---
aliases:
  - PCA
---


## Overview
**Principal Component Analysis (PCA)** is a linear [[Dimensionality Reduction]] technique used to reduce the number of features in a dataset while preserving as much variance as possible. PCA achieves this by transforming the original features into a new set of uncorrelated variables called **principal components**, ranked by the amount of variance they capture.

PCA is widely used in [[Machine Learning]], [[Data Visualization]], and preprocessing high-dimensional data for other tasks.

---

## Key Concepts

### [[Dimensionality Reduction]]
- PCA reduces the dimensionality of data by projecting it onto a lower-dimensional subspace, maximizing the variance retained.
- This helps mitigate the **curse of dimensionality** and improves computational efficiency.

### Principal Components
- **[[Principal Component]]**: A linear combination of the original features that captures the maximum variance in the data.
- Components are orthogonal (uncorrelated), ensuring that each successive component explains the next highest variance.

### [[Covariance Matrix]]
- PCA uses the **covariance matrix** to measure relationships between features and find directions of maximum variance.

### Eigenvalues and Eigenvectors
- **[[Eigenvalues]]**: Represent the amount of variance captured by each principal component.
- **[[Eigenvectors]]**: Represent the direction of each principal component.

---

## Steps in PCA

1. **[[Standardize]] the Data**:
   - Center the data by subtracting the mean and scale to unit variance if required.
2. **Compute the Covariance Matrix**:
   - Calculate the covariance matrix to understand relationships between features.
3. **Calculate Eigenvalues and Eigenvectors**:
   - Solve for eigenvalues and eigenvectors of the covariance matrix.
4. **Select Principal Components**:
   - Rank eigenvalues in descending order and select the top $k$ components to retain $k$-dimensional data.
5. **Transform the Data**:
   - Project the original data onto the $k$-dimensional subspace spanned by the selected principal components.

---

## Parameters

1. **Number of Components ($k$)**:
   - Specifies the number of principal components to retain.
   - Can be chosen based on the explained variance ratio.

2. **[[Explained Variance Ratio]]**:
   - Measures the proportion of variance captured by each principal component.
   - A cumulative threshold (e.g., 95%) is often used to determine the number of components.

---

## Advantages

1. **Dimensionality Reduction**:
   - Reduces computational cost by lowering the number of features while preserving variance.
2. **Removes [[Multicollinearity]]**:
   - Transforms correlated features into uncorrelated components.
3. **Improves Visualization**:
   - Projects high-dimensional data into 2D or 3D for visualization.

---

## Disadvantages

1. **[[Linear Assumption]]**:
   - PCA assumes linear relationships between features and may not capture complex patterns in the data.
2. **Loss of Interpretability**:
   - Principal components are combinations of original features, making them harder to interpret.
3. **Scaling Sensitivity**:
   - PCA is sensitive to the scaling of features and requires preprocessing (e.g., standardization).

---

## Applications

1. **[[Feature Reduction]]**:
   - Removes redundant or irrelevant features to improve model performance.
2. **[[Noise Reduction]]**:
   - Filters out noise by retaining only the most significant components.
3. **[[Data Visualization]]**:
   - Projects data onto 2D or 3D for easy exploration and visualization.
4. **[[Anomaly Detection]]**:
   - Identifies outliers in the reduced-dimensional space.

---

## Example Workflow

1. **Preprocess the Data**:
   - Standardize the features to ensure all have equal importance.
2. **Apply PCA**:
   - Use PCA to compute principal components.
3. **Select Components**:
   - Retain components that explain a significant amount of variance.
4. **Transform Data**:
   - Project the original dataset onto the reduced-dimensional space.

---

## Comparison with Other Techniques

| Feature               | PCA                                | t-SNE                              | UMAP                               |
|-----------------------|-------------------------------------|-------------------------------------|-------------------------------------|
| **Linear**            | Yes                                | No                                 | No                                 |
| **Scalability**       | High                               | Moderate                           | Moderate                           |
| **Interpretability**  | Moderate (based on variance)       | Low                                | Low                                |
| **Preserves Structure** | Global (variance-based)           | Local                              | Local                              |

---

## Tools and Libraries

1. **Python Libraries**:
   - **[[Scikit-learn]]**: `sklearn.decomposition.PCA` for implementing PCA.
   - **NumPy**: Custom implementation using covariance matrix and linear algebra.
2. **Visualization Tools**:
   - **Matplotlib/Seaborn**: Plot cumulative explained variance or principal components.
   - **Plotly**: Interactive 2D/3D visualizations.

---

## Related Topics

- [[Dimensionality Reduction]]: PCA is one of many techniques for reducing feature dimensions.
- [[t-SNE]]: A nonlinear dimensionality reduction method for visualization.
- [[UMAP]]: Another nonlinear method, often used for clustering.
- [[Feature Scaling]]: Essential preprocessing step before applying PCA.

---

## Resources

### Tutorials
- [[Scikit-learn]]’s PCA documentation.
- Online tutorials on dimensionality reduction with PCA.

### Books
- *Hands-On Machine Learning with [[Scikit-learn]], Keras, and TensorFlow* by Aurélien Géron.
- *Pattern Recognition and Machine Learning* by Christopher Bishop.

### Research Papers
- *PCA* by Karl Pearson (1901), the original paper introducing PCA.

---

Aliases

- Principal Component Analysis
- PCA
- PCA Analysis
- Principal Components
- Dimensionality Reduction (PCA)

---

## Tags
#PCA #dimensionality-reduction #machinelearning #unsupervised-learning #datavisualization