## Overview
The F1 Score is a performance metric used to evaluate [[Classification]] models. It is the harmonic mean of **precision** and **recall** and provides a balanced measure, especially useful when dealing with imbalanced datasets.

---

## Formula
The F1 Score is calculated as:
$$
F1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
$$

Where:
- **Precision**: The proportion of true positive predictions out of all positive predictions.
	$$
  \text{Precision} = \frac{\text{True Positives (TP)}}{\text{True Positives (TP)} + \text{False Positives (FP)}}
  $$
- **Recall**: The proportion of true positive predictions out of all actual positives.
  $$
  \text{Recall} = \frac{\text{True Positives (TP)}}{\text{True Positives (TP)} + \text{False Negatives (FN)}}
  $$

---

## Interpretation
- **Range**: The F1 Score ranges from 0 to 1.
  - **1**: Perfect precision and recall (ideal case).
  - **0**: Poor performance with either precision or recall being zero.
- **When to Use**:
  - When both precision and recall are important.
  - For imbalanced datasets where accuracy alone is misleading.

---

## Example Calculation
Suppose a binary classifier produces the following confusion matrix:

|                 | Predicted Positive | Predicted Negative |
|-----------------|--------------------|--------------------|
| **Actual Positive** | True Positive (TP) = 40 | False Negative (FN) = 10 |
| **Actual Negative** | False Positive (FP) = 5  | True Negative (TN) = 45 |

### Precision:
$$
\text{Precision} = \frac{TP}{TP + FP} = \frac{40}{40 + 5} = 0.89
$$

### Recall:
$$
\text{Recall} = \frac{TP}{TP + FN} = \frac{40}{40 + 10} = 0.80
$$

### F1 Score:
$$
F1 = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}} = 2 \cdot \frac{0.89 \cdot 0.80}{0.89 + 0.80} = 0.84
$$

---

## Advantages
- **Balances Precision and Recall**: Useful when one metric is not sufficient to evaluate model performance.
- **Handles Class Imbalance**: More informative than accuracy for datasets with imbalanced classes.

---

## Disadvantages
- Does not consider the **True Negatives (TN)**, which can be important in some applications.
- Can be misleading if either precision or recall is prioritized more heavily.

---

## Use Cases
- **Spam Detection**: Balances minimizing false positives (important emails marked as spam) and false negatives (spam emails marked as legitimate).
- **Medical Diagnosis**: Reduces false negatives (missed diagnoses) while minimizing false positives (unnecessary treatments).
- **Search and Recommendation Systems**: Ensures relevance while reducing noise.

---

## Related Metrics
- **[[Accuracy]]**: Overall correctness of predictions.
  $$
  \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
  $$
- **[[Precision]]**: Focuses on minimizing false positives.
- **[[Recall]](Sensitivity)**: Focuses on minimizing false negatives.
- **[[ROC AUC]]**: Evaluates the trade-off between true positive rate and false positive rate.

---

## Tools for Calculation
- **[[Scikit-learn]] (Python)**:
  ```python
  from sklearn.metrics import f1_score

  y_true = [1, 1, 0, 0, 1]
  y_pred = [1, 0, 1, 0, 1]

  f1 = f1_score(y_true, y_pred)
  print(f"F1 Score: {f1}")```


**Tags**

#f1score #machinelearning #[[Classification]] #evaluationmetrics #datascience