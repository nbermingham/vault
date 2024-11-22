## Overview
**Recall**, also known as **Sensitivity** or **True Positive Rate**, is a performance metric in [[Classification]] tasks that measures the proportion of actual positive instances correctly identified by the model. Recall is especially important in scenarios where identifying all positive instances is critical, even at the cost of false positives.

Recall is often evaluated alongside [[Precision]] and other metrics like [[F1-Score]] to provide a comprehensive view of model performance.

---

## Key Concepts

### **1. Formula**
Recall is calculated as:
$$
\text{Recall} = \frac{TP}{TP + FN}
$$
Where:
- $TP$: True Positives (correctly predicted positive instances).
- $FN$: False Negatives (positive instances incorrectly predicted as negative).

---

### **2. Interpretation**
- **High Recall**: The model successfully identifies most of the positive instances.
- **Low Recall**: The model misses many positive instances.

---

## Applications

1. **Medical Diagnosis**:
   - Recall is crucial to minimize false negatives (e.g., detecting cancer cases).
2. **Fraud Detection**:
   - Prioritizes identifying all fraudulent transactions, even at the cost of some false positives.
3. **Search Engines**:
   - Ensures relevant results are included in the output, even if some irrelevant results are also returned.

---

## Advantages

1. **Focus on Positive Class**:
   - Recall emphasizes the ability of the model to capture actual positives.
2. **Critical in High-Risk Applications**:
   - Essential in scenarios where missing positive instances can have severe consequences (e.g., healthcare, fraud).

---

## Disadvantages

1. **Ignores False Positives**:
   - Recall does not account for false positives, making it insufficient on its own for many tasks.
2. **Bias Toward Positive Predictions**:
   - Models predicting more positives may achieve high recall but at the cost of precision.

---

## Comparison with Other Metrics

| **Metric**     | **Focus**               | **Use Case**                             |
|-----------------|-------------------------|------------------------------------------|
| **Recall**      | Coverage of positives   | Minimize false negatives                 |
| **Precision**   | Quality of positive predictions | Minimize false positives               |
| **F1-Score**    | Balance of precision and recall | Imbalanced datasets                     |
| **Accuracy**    | Overall correctness     | Balanced datasets                        |

---

## Example

### Binary Classification Example
Confusion matrix:

|                  | Predicted Positive | Predicted Negative |
|------------------|--------------------|--------------------|
| **Actual Positive** | $TP = 50$          | $FN = 10$          |
| **Actual Negative** | $FP = 5$           | $TN = 35$          |

**Recall Calculation**:
$$
\text{Recall} = \frac{TP}{TP + FN} = \frac{50}{50 + 10} = 0.83
$$
This means the model correctly identifies 83% of the actual positives.

---

## Tools and Libraries

1. **Python Libraries**:
   - [[Scikit-learn]]: `recall_score`.
   - TensorFlow/Keras: Metrics modules for recall evaluation.
2. **Visualization Tools**:
   - Precision-Recall curves to analyze the relationship between Precision and Recall across thresholds.

---

## Related Topics

- [[Confusion Matrix]]: Provides the data needed to compute Recall.
- [[Precision]]: Complements Recall by focusing on false positives.
- [[F1-Score]]: Balances Precision and Recall for imbalanced datasets.
- [[Accuracy]]: Measures overall correctness but does not highlight class-specific performance.
- [[Precision-Recall Curve]]: Evaluates performance trade-offs between Precision and Recall.

---

## Aliases
- Recall
- Sensitivity
- True Positive Rate (TPR)

---

## Tags
#recall #classification #metrics #machinelearning #modelperformance #datascience

---

## Links to Explore
- [[Precision]]: Learn how it complements Recall in evaluating model performance.
- [[F1-Score]]: Discover how Precision and Recall are balanced.
- [[Confusion Matrix]]: Understand the context of Recall in classification tasks.
- [[Scikit-learn]]: Implement recall calculations with this library.
- [[Precision-Recall Curve]]: Visualize Recall and Precision trade-offs.