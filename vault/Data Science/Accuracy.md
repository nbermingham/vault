## Overview
**Accuracy** is a commonly used metric in [[Classification]] tasks that measures the proportion of correctly classified instances out of the total number of instances. It is often the first metric evaluated when determining a model's performance, especially for balanced datasets.

While simple to calculate, Accuracy may not always be reliable for imbalanced datasets, where the distribution of classes is skewed.

---

## Key Concepts

### **1. Formula**
For a binary classification task:
$$
\text{Accuracy} = \frac{\text{Number of Correct Predictions}}{\text{Total Number of Predictions}}
$$
Alternatively, in terms of the confusion matrix:
$$
\text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
$$
Where:
- $TP$: True Positives.
- $TN$: True Negatives.
- $FP$: False Positives.
- $FN$: False Negatives.

### **2. Interpretation**
- A high Accuracy means that the model predicts the majority of instances correctly.
- However, it does not provide insights into individual class performance or the cost of misclassifications.

---

## Applications

1. **Binary Classification**:
   - Example: Email classification (spam vs. non-spam).
2. **Multi-Class Classification**:
   - Example: Image classification with multiple categories.
3. **Quick Model Evaluation**:
   - Used as a baseline metric during initial model assessment.

---

## Advantages

1. **Simple to Compute**:
   - Easy to calculate and interpret.
2. **Quick Feedback**:
   - Provides a quick assessment of overall model performance.
3. **Baseline Metric**:
   - A good starting point for evaluating classification models.

---

## Disadvantages

1. **Insensitive to Class Imbalance**:
   - Accuracy can be misleading when classes are imbalanced.
     - Example: If 95% of data belongs to one class, a naive classifier that always predicts the majority class achieves 95% Accuracy without learning anything meaningful.
2. **Lack of Granularity**:
   - Does not differentiate between types of errors (e.g., $FP$ vs. $FN$).
3. **Not Suitable for Imbalanced Datasets**:
   - Metrics like [[Precision]], [[Recall]], and [[F1-Score]] are better suited in such cases.

---

## Comparison with Other Metrics

| **Metric**     | **Focus**               | **Use Case**                             |
|-----------------|-------------------------|------------------------------------------|
| Accuracy        | Overall correctness     | Balanced datasets                        |
| Precision       | Positive class accuracy | Minimizing false positives               |
| Recall          | Sensitivity             | Minimizing false negatives               |
| F1-Score        | Balance of precision/recall | Imbalanced datasets                     |

---

## Example

### Binary Classification Example
Confusion matrix for a dataset:
|                | Predicted Positive | Predicted Negative |
|----------------|--------------------|--------------------|
| **Actual Positive** | 50                 | 10                 |
| **Actual Negative** | 5                  | 35                 |

$$
\text{Accuracy} = \frac{50 + 35}{50 + 35 + 10 + 5} = \frac{85}{100} = 85\%
$$

---

## Tools and Libraries

1. **Python Libraries**:
   - [[Scikit-learn]]: `sklearn.metrics.accuracy_score`.
   - TensorFlow/Keras: Built-in accuracy metrics.
2. **Visualization Tools**:
   - Confusion matrix visualizations using Matplotlib or Seaborn.

---

## Related Topics

- [[Confusion Matrix]]: Provides a detailed breakdown of prediction outcomes.
- [[Precision]]: Focuses on the quality of positive predictions.
- [[Recall]]: Measures the completeness of positive predictions.
- [[F1-Score]]: Balances precision and recall.
- [[ROC AUC]]: Evaluates classification performance across thresholds.

---

## Aliases
- Accuracy
- Classification Accuracy
- Prediction Accuracy

---

## Tags
#accuracy #classification #metrics #machinelearning #modelperformance

---

## Links to Explore
- [[Confusion Matrix]]: Understand how Accuracy relates to other metrics.
- [[Precision]]: Learn when to prioritize precise predictions.
- [[Recall]]: Explore scenarios where recall is more critical.
- [[F1-Score]]: Discover how Accuracy compares to this balanced metric.
- [[Scikit-learn]]: Implement accuracy calculations in Python.