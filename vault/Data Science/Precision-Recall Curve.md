## Overview

A **Precision-Recall Curve** is a graphical representation of the trade-off between [[Precision]] and [[Recall]] across different decision thresholds in a [[Classification]] model. It is particularly useful for evaluating models on imbalanced datasets, where the positive class is rare, and metrics like [[Accuracy]] can be misleading.

The curve plots **Precision** on the y-axis and **Recall** on the x-axis, showing how the two metrics change as the classification threshold is varied.

---

## Key Concepts

### **1. Thresholds and Trade-Offs**
- **Threshold**: The decision boundary used to classify instances as positive or negative.
  - Lowering the threshold increases Recall but may decrease Precision.
  - Raising the threshold increases Precision but may decrease Recall.
- **Trade-Off**: Models must balance Precision and Recall based on the problem's requirements.

### **2. Area Under the Curve (AUC)**
- **Precision-Recall AUC (PR AUC)**:
  - Measures the overall performance of the model.
  - Higher AUC indicates better model performance across thresholds.

### **3. Key Points**
- **Perfect Model**:
  - Precision = 1 and Recall = 1 at all thresholds.
- **Baseline Model**:
  - Precision equals the prevalence of the positive class in the dataset (e.g., 10% for a dataset with 10% positives).
- **Skewed Datasets**:
  - For imbalanced datasets, PR AUC is more informative than [[ROC AUC]] as it focuses on the positive class.

---

## Applications

1. **Imbalanced Classification**:
   - Evaluating fraud detection, rare disease diagnosis, or other problems with rare positive instances.
2. **Threshold Optimization**:
   - Choosing the best threshold for Precision-Recall trade-offs based on application needs.
3. **Comparing Models**:
   - Comparing PR curves helps assess which model better balances Precision and Recall.

---

## Advantages

1. **Focus on Positive Class**:
   - Highlights performance on the positive class, making it ideal for imbalanced datasets.
2. **Visual Representation**:
   - Provides insights into how Precision and Recall vary with threshold changes.
3. **Application-Specific Insights**:
   - Helps select thresholds based on specific trade-off requirements (e.g., prioritizing high Recall in medical applications).

---

## Disadvantages

1. **Limited Scope**:
   - Does not consider the performance on the negative class.
2. **Difficult Interpretation for Multiple Classes**:
   - Extending PR curves to multi-class classification requires additional complexity.
3. **Not Always Comparable**:
   - PR curves are dataset-specific and depend on the class imbalance ratio.

---

## Example

### Binary Classification Example
Suppose a model predicts probabilities for a binary classification task. By varying the threshold, Precision and Recall change as follows:

| **Threshold** | **Precision** | **Recall** |
|---------------|---------------|------------|
| 0.9           | 0.95          | 0.50       |
| 0.7           | 0.85          | 0.70       |
| 0.5           | 0.80          | 0.85       |
| 0.3           | 0.75          | 0.95       |

Plotting Precision vs. Recall at these thresholds results in the Precision-Recall Curve.

---

## Tools and Libraries

1. **Python Libraries**:
   - [[Scikit-learn]]: `precision_recall_curve` and `plot_precision_recall_curve`.
   - TensorFlow/Keras: Metrics modules for PR curve generation.
2. **Visualization**:
   - Matplotlib or Seaborn for plotting PR curves.

---

## Related Topics

- [[Precision]]: Metric representing the quality of positive predictions.
- [[Recall]]: Metric representing the completeness of positive predictions.
- [[F1-Score]]: Balances Precision and Recall for imbalanced datasets.
- [[ROC AUC]]: Evaluates performance across classification thresholds but focuses on overall performance.

---

## Aliases
- Precision-Recall Curve
- PR Curve
- Precision vs. Recall Curve

---

## Tags
#precisionrecallcurve #classification #metrics #machinelearning #modelperformance #datascience

---

## Links to Explore
- [[Precision]]: Understand the metric plotted on the y-axis of the PR curve.
- [[Recall]]: Learn about the metric plotted on the x-axis of the PR curve.
- [[F1-Score]]: Explore the balance between Precision and Recall.
- [[Scikit-learn]]: Implement Precision-Recall Curves with this library.
- [[ROC AUC]]: Compare PR curves with ROC curves.