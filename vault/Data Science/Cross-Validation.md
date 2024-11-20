## Overview
**Cross-Validation** is a statistical method used in [[Machine Learning]] to evaluate the generalization performance of a model. It splits the dataset into multiple subsets (folds), training the model on some subsets while testing it on the others. This ensures that the model's performance is not biased by a single train-test split.

Cross-Validation helps in selecting models, tuning hyperparameters, and preventing issues like [[Overfitting]] and [[Underfitting]].

---

## Key Concepts

### **1. Process**
1. **Split the Data**:
   - Divide the dataset into $k$ equal-sized subsets (folds).
2. **Iterate**:
   - Train the model on $k-1$ folds and evaluate it on the remaining fold.
3. **Repeat**:
   - Rotate the testing fold and repeat the process $k$ times.
4. **Aggregate**:
   - Calculate the mean performance metric (e.g., accuracy, [[Mean Squared Error]]) across all folds.

### **2. Types of Cross-Validation**
- **K-Fold Cross-Validation**:
  - Splits the dataset into $k$ folds and iterates through them as described above.
- **Stratified K-Fold Cross-Validation**:
  - Ensures that each fold maintains the same class distribution as the original dataset, commonly used in [[Classification]] tasks.
- **Leave-One-Out Cross-Validation (LOOCV)**:
  - Each fold contains exactly one data point, making it computationally expensive but highly thorough.
- **Time-Series Cross-Validation**:
  - Used for time-dependent data, where future data cannot "leak" into the training set. Splits are sequential.
- **Repeated K-Fold Cross-Validation**:
  - Repeats K-Fold multiple times with different random splits to get a more robust estimate.

---

## Applications

1. **Model Evaluation**:
   - Provides an unbiased estimate of model performance on unseen data.
2. **Hyperparameter Tuning**:
   - Works in conjunction with techniques like [[Grid Search]] or [[Random Search]] to optimize hyperparameters.
3. **Feature Selection**:
   - Assesses the impact of different feature subsets on model performance.
4. **Algorithm Comparison**:
   - Evaluates multiple algorithms to determine the best-performing one for a specific task.

---

## Advantages

1. **Reduced Overfitting**:
   - Ensures the model is not overly fitted to a single train-test split.
2. **Unbiased Performance Estimate**:
   - Aggregates results from multiple splits to provide a reliable estimate of generalization performance.
3. **Robustness**:
   - Suitable for datasets with limited size, ensuring all data points are used for training and testing.

---

## Disadvantages

1. **Computational Cost**:
   - Training and evaluating the model multiple times increases computation time.
2. **Complexity**:
   - More complex workflows compared to a simple train-test split.
3. **Bias in Small Datasets**:
   - In very small datasets, the testing fold may not be representative of the entire data distribution.

---

## Example
Suppose you have a dataset with 10 samples:
| Fold | Training Samples      | Testing Samples |
|------|-----------------------|-----------------|
| 1    | 2, 3, 4, 5, 6, 7, 8, 9, 10 | 1               |
| 2    | 1, 3, 4, 5, 6, 7, 8, 9, 10 | 2               |
| ...  | ...                   | ...             |
| 10   | 1, 2, 3, 4, 5, 6, 7, 8, 9 | 10              |

After training and evaluating the model on each fold, compute the average performance metric (e.g., accuracy, [[ROC AUC]], or [[Mean Squared Error]]).

---

## Tools and Libraries

1. **Scikit-learn**:
   - Provides implementations for `KFold`, `StratifiedKFold`, and `TimeSeriesSplit`.
2. **Python Libraries**:
   - Pandas and NumPy for preprocessing.
   - TensorFlow and PyTorch for deep learning tasks.
3. **Visualization Tools**:
   - Matplotlib or Seaborn to plot performance across folds.

---

## Related Topics

- [[Overfitting]]: Cross-Validation helps prevent this issue by testing on unseen data.
- [[Underfitting]]: Ensures the model is not too simplistic by evaluating it on diverse subsets.
- [[Bias-Variance Tradeoff]]: Cross-Validation balances bias and variance during evaluation.
- [[Hyperparameter Tuning]]: Guides parameter optimization using techniques like grid search.
- [[Feature Selection]]: Evaluates feature subsets with Cross-Validation.

---

## Aliases
- Cross Validation
- CV
- K-Fold Validation
- Validation Splits

---

## Tags
#cross-validation #model-evaluation #machinelearning #datascience #overfitting #hyperparameter-tuning

---

## Links to Explore
- [[Overfitting]]: Understand how Cross-Validation mitigates this issue.
- [[Bias-Variance Tradeoff]]: Explore the balance Cross-Validation helps achieve.
- [[Hyperparameter Tuning]]: Learn how Cross-Validation integrates into tuning pipelines.
- [[Feature Selection]]: Discover how features are evaluated using Cross-Validation.
- [[Grid Search]]: Use Cross-Validation with grid search for optimal hyperparameter selection.