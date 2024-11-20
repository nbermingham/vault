## Overview
**Classification Metrics** are used to evaluate the performance of a classification model by comparing its predictions to the true labels. These metrics help quantify how well the model distinguishes between different classes, making them essential for assessing [[Machine Learning]] models in tasks like spam detection, sentiment analysis, and image classification.

---

## Key Metrics

### 1. Accuracy
- Measures the proportion of correctly classified samples:
$$
\text{Accuracy} = \frac{\text{TP} + \text{TN}}{\text{TP} + \text{TN} + \text{FP} + \text{FN}}
$$
Where:
- **TP**: True Positives.
- **TN**: True Negatives.
- **FP**: False Positives.
- **FN**: False Negatives.

**Limitations**:
- Misleading for imbalanced datasets, as it doesn’t account for class distribution.

---

### 2. [[Precision]]
- Measures the proportion of true positive predictions out of all positive predictions:
$$
\text{Precision} = \frac{\text{TP}}{\text{TP} + \text{FP}}
$$

**Use Case**:
- Important when false positives are costly (e.g., spam detection).

---

### 3. [[Recall]] ([[Sensitivity]], [[True Positive Rate]])
- Measures the proportion of true positives out of all actual positives:
$$
\text{Recall} = \frac{\text{TP}}{\text{TP} + \text{FN}}
$$

**Use Case**:
- Crucial when false negatives are costly (e.g., medical diagnosis).

---

### 4. [[F1-Score]]
- Harmonic mean of precision and recall:
$$
\text{F1 Score} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$
- Balances precision and recall, especially for imbalanced datasets.

---

### 5. [[ROC AUC]] (Receiver Operating Characteristic - Area Under the Curve)
- Measures the ability of the model to distinguish between classes.
- ROC Curve:
  - Plots **True Positive Rate (TPR)** vs. **False Positive Rate (FPR)**.
- **AUC**: Represents the area under the ROC curve (ranges from 0 to 1).

**Use Case**:
- Evaluates the ranking quality of predicted probabilities.

---

### 6. [[Log Loss]] (Logarithmic Loss)
- Measures the difference between predicted probabilities and actual labels:
$$
\text{Log Loss} = -\frac{1}{N} \sum_{i=1}^N \left[ y_i \log(p_i) + (1 - y_i) \log(1 - p_i) \right]
$$
Where:
- $y_i$: True label.
- $p_i$: Predicted probability.

**Use Case**:
- Penalizes incorrect predictions with high confidence.

---

### 7. [[Confusion Matrix]]
- Summarizes predictions into a table with counts of:
  - **True Positives (TP)**: Correct positive predictions.
  - **False Positives (FP)**: Incorrect positive predictions.
  - **True Negatives (TN)**: Correct negative predictions.
  - **False Negatives (FN)**: Incorrect negative predictions.

**Use Case**:
- Provides detailed insight into prediction errors.

---

### 8. [[Matthews Correlation Coefficient]] (MCC)
- A balanced metric even for imbalanced datasets:
$$
\text{MCC} = \frac{\text{TP} \cdot \text{TN} - \text{FP} \cdot \text{FN}}{\sqrt{(\text{TP} + \text{FP})(\text{TP} + \text{FN})(\text{TN} + \text{FP})(\text{TN} + \text{FN})}}
$$

**Use Case**:
- Useful for binary classification with imbalanced datasets.

---

### 9. [[Cohen's Kappa]]
- Measures agreement between predictions and true labels, adjusted for random chance:
$$
\text{Cohen's Kappa} = \frac{\text{Observed Agreement} - \text{Expected Agreement}}{1 - \text{Expected Agreement}}
$$

**Use Case**:
- Evaluates classifier performance with respect to a baseline.

---

## Considerations for Imbalanced Datasets

1. **Avoid Accuracy**:
   - Accuracy can be misleading when one class dominates.
2. **Use Precision, Recall, and F1 Score**:
   - These metrics better capture performance for minority classes.
3. **ROC-AUC and PR-AUC**:
   - Precision-Recall AUC is more informative for imbalanced datasets.

---

## Tools and Libraries

1. **Scikit-learn**:
   - Provides functions for all major classification metrics (`accuracy_score`, `f1_score`, `roc_auc_score`, etc.).
2. **TensorFlow/PyTorch**:
   - Built-in modules for computing loss and evaluation metrics.
3. **Visualization**:
   - Matplotlib and Seaborn for confusion matrices and ROC curves.

---

## Example Workflow

1. **Train Model**:
   - Train the classifier on the dataset.
2. **Make Predictions**:
   - Generate predictions on a test dataset.
3. **Evaluate Metrics**:
   - Compute metrics like precision, recall, F1 score, and ROC-AUC.
4. **Visualize**:
   - Plot confusion matrix, ROC curve, or precision-recall curve for interpretation.

---

## Related Topics

- [[Logistic Regression]]: A common algorithm for binary classification.
- [[Cross-Entropy Loss]]: Used for optimizing classification models.
- [[Imbalanced Datasets]]: Strategies to handle class imbalance.
- [[Precision-Recall Tradeoff]]: Balancing precision and recall based on use case.

---

## Resources

### Tutorials
- Scikit-learn's guide to classification metrics.
- Python tutorials for visualizing confusion matrices and ROC curves.

### Books
- *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* by Aurélien Géron.
- *Pattern Recognition and Machine Learning* by Christopher Bishop.

### Research Papers
- Articles on evaluation metrics for imbalanced datasets.

---

## Tags
#classification-metrics #machinelearning #model-evaluation #precision-recall #confusion-matrix