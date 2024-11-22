---
aliases:
  - SVMs
  - SVM
  - Support Vector Machine
---
## Overview
**Support Vector Machines (SVMs)** are supervised machine learning models used for [[Classification]] and [[Regression]] tasks. They are particularly effective for binary classification problems. SVMs work by finding the hyperplane that best separates data points of different classes in a high-dimensional space, maximizing the **margin** between the classes.

SVMs can handle linear and non-linear relationships using the **kernel trick**, making them versatile for many applications.

---

## Key Concepts

### **1. [[Hyperplane]]**
- A hyperplane is a decision boundary that separates data points into different classes. 
- In $n$-dimensional space, a hyperplane has the equation:
  $$
  \mathbf{w} \cdot \mathbf{x} + b = 0
  $$
  Where:
  - $\mathbf{w}$: Weight vector (direction of the hyperplane).
  - $b$: Bias term (distance of the hyperplane from the origin).
  - $\mathbf{x}$: Input feature vector.

### **2. [[Margin]]**
- The **margin** is the distance between the hyperplane and the closest data points (support vectors).
- SVMs maximize this margin to improve generalization.

### **3. [[Support Vectors]]**
- The data points that lie closest to the hyperplane.
- These points define the position of the hyperplane and are critical to the model.

### **4. [[Kernel Trick]]**
- SVMs use kernel functions to transform data into higher-dimensional spaces, enabling them to classify non-linear relationships. Common kernels include:
  - **Linear Kernel**: For linearly separable data.
  - **Polynomial Kernel**: For polynomial decision boundaries.
  - **Radial Basis Function (RBF) Kernel**: For non-linear decision boundaries.
  - **Sigmoid Kernel**: Similar to neural network activation functions.

---

## Mathematical Formulation
The optimization objective of SVMs is:
$$
\min_{\mathbf{w}, b} \frac{1}{2} ||\mathbf{w}||^2
$$
Subject to:
$$
y_i (\mathbf{w} \cdot \mathbf{x}_i + b) \geq 1, \; \forall i
$$
Where:
- $y_i$: Class label for the $i^{th}$ data point ($+1$ or $-1$).
- $\mathbf{x}_i$: Feature vector for the $i^{th}$ data point.
- $||\mathbf{w}||$: Norm of the weight vector (to minimize the margin width).

For non-linear problems, the optimization includes a **slack variable** $\xi_i$ for soft-margin SVMs, which allows some misclassified points:
$$
\min_{\mathbf{w}, b, \xi} \frac{1}{2} ||\mathbf{w}||^2 + C \sum_{i=1}^n \xi_i
$$

---

## Applications

1. **Text Classification**:
   - Spam detection, sentiment analysis, and topic categorization.
2. **Image Recognition**:
   - Handwriting and object classification.
3. **Bioinformatics**:
   - Protein classification and gene expression analysis.
4. **Financial Analysis**:
   - Fraud detection and stock price prediction.

---

## Advantages

1. **Effective with High-Dimensional Data**:
   - Performs well when the number of dimensions is greater than the number of samples.
2. **Robust to Overfitting**:
   - Effective in cases where data points are far from the hyperplane.
3. **Kernel Trick**:
   - Flexibility to model non-linear relationships.

---

## Disadvantages

1. **Computational Complexity**:
   - Training time increases with large datasets.
2. **Choice of Kernel**:
   - Requires careful tuning and domain expertise.
3. **Not Probabilistic**:
   - Does not directly provide probability estimates; requires additional calibration.

---

## Example
Consider a dataset with two classes: $+$ and $-$.

| Feature 1 | Feature 2 | Class |
|-----------|-----------|-------|
| 1         | 2         | $+$   |
| 2         | 3         | $-$   |
| 3         | 4         | $+$   |
| 4         | 5         | $-$   |

Using an SVM, the algorithm finds the hyperplane that separates the two classes while maximizing the margin. For a linear kernel, the hyperplane might look like:
$$
x_2 = 0.5 x_1 + 1
$$

---

## Tools and Libraries

1. **Scikit-learn**:
   - `sklearn.svm.SVC` for classification.
   - `sklearn.svm.SVR` for regression.
2. **LibSVM**:
   - A popular library for SVM implementation.
3. **TensorFlow** and **PyTorch**:
   - Can implement SVMs using custom optimization functions.

---

## Related Topics

- [[Classification]]: SVMs are primarily used for classification tasks.
- [[Kernel Trick]]: Enables SVMs to handle non-linear relationships.
- [[Hyperplane]]: The decision boundary in SVMs.
- [[Overfitting]]: SVMs are less prone to overfitting compared to other models.
- [[Gradient Descent]]: Alternative optimization techniques for training SVMs.

---

## Aliases
- Support Vector Machines
- SVM
- Support Vectors
- Kernel Machines

---

## Tags
#svm #machinelearning #classification #regression #datascience #kernelmethods

---

## Links to Explore
- [[Classification]]: Understand how SVMs fit into classification tasks.
- [[Kernel Trick]]: Explore how kernels enable non-linear SVMs.
- [[Overfitting]]: Learn why SVMs are robust to overfitting.
- [[Gradient Descent]]: Compare SVM optimization to gradient descent methods.