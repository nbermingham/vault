## Overview
A **Confusion Matrix** is a performance evaluation tool for [[Classification]] tasks that summarizes the prediction results of a model. It provides a detailed breakdown of correctly and incorrectly classified instances for each class, offering insights beyond metrics like [[Accuracy]].

The confusion matrix is especially useful in understanding model performance on imbalanced datasets and analyzing errors in multi-class classification tasks.

---

## Key Concepts

### **1. Structure of a Confusion Matrix**
For a binary classification task, the confusion matrix is a 2x2 table:
|                  | Predicted Positive | Predicted Negative |
|------------------|--------------------|--------------------|
| **Actual Positive** | True Positive ($TP$) | False Negative ($FN$) |
| **Actual Negative** | False Positive ($FP$) | True Negative ($TN$) |

Where:
- $TP$: Correctly predicted positive instances.
- $FP$: Incorrectly predicted positive instances.
- $FN$: Incorrectly predicted negative instances.
- $TN$: Correctly predicted negative instances.

For multi-class classification, the confusion matrix extends to an $N \times N$ table, where $N$ is the number of classes.

---

## Key Metrics Derived from the Confusion Matrix

1. **[[Accuracy]]**:
   $$
   \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN}
   $$

2. **[[Precision]]**:
   $$
   \text{Precision} = \frac{TP}{TP + FP}
   $$

3. **[[Recall]] (Sensitivity)**:
   $$
   \text{Recall} = \frac{TP}{TP + FN}
   $$

4. **[[F1-Score]]**:
   $$
   \text{F1-Score} = 2 \cdot \frac{\text{Precision} \cdot \text{Recall}}{\text{Precision} + \text{Recall}}
   $$

5. **Specificity**:
   $$
   \text{Specificity} = \frac{TN}{TN + FP}
   $$

---

## Applications

1. **Binary Classification**:
   - Evaluate tasks like spam detection, fraud detection, or medical diagnosis.
2. **Multi-Class Classification**:
   - Analyze performance on tasks like image recognition or sentiment analysis.
3. **Imbalanced Datasets**:
   - Identify how well the model handles minority and majority classes.
4. **Error Analysis**:
   - Pinpoint specific types of errors (e.g., false positives vs. false negatives).

---

## Example

### Binary Classification Example
Consider the following confusion matrix:
|                  | Predicted Positive | Predicted Negative |
|------------------|--------------------|--------------------|
| **Actual Positive** | 50                 | 10                 |
| **Actual Negative** | 5                  | 35                 |

From this matrix:
- $TP = 50$, $FP = 5$, $FN = 10$, $TN = 35$
- **Accuracy**: 
  $$
  \text{Accuracy} = \frac{TP + TN}{TP + TN + FP + FN} = \frac{50 + 35}{50 + 10 + 5 + 35} = 0.85
  $$
- **Precision**:
  $$
  \text{Precision} = \frac{TP}{TP + FP} = \frac{50}{50 + 5} = 0.91
  $$
- **Recall**:
  $$
  \text{Recall} = \frac{TP}{TP + FN} = \frac{50}{50 + 10} = 0.83
  $$

---

## Advantages

1. **Detailed Breakdown**:
   - Provides a granular view of model performance, highlighting types of errors.
2. **Useful for Imbalanced Data**:
   - Highlights performance on minority and majority classes.
3. **Supports Multi-Class Tasks**:
   - Extends to evaluate multiple classes effectively.

---

## Disadvantages

1. **Scalability**:
   - Becomes harder to interpret for large multi-class problems.
2. **Focus on Raw Counts**:
   - Raw counts alone may not be meaningful without derived metrics.

---

## Tools and Libraries

1. **Python Libraries**:
   - [[Scikit-learn]]: `confusion_matrix` and `plot_confusion_matrix`.
   - Seaborn: `heatmap` for visualizing confusion matrices.
2. **Visualization Tools**:
   - Matplotlib and Plotly for custom visualizations.

---

## Related Topics

- [[Accuracy]]: A metric derived from the confusion matrix.
- [[Precision]]: Evaluates the quality of positive predictions.
- [[Recall]]: Measures how many actual positives were identified.
- [[F1-Score]]: Balances precision and recall for imbalanced data.
- [[ROC AUC]]: Evaluates performance across classification thresholds.

---

## Aliases
- Confusion Matrix
- Classification Matrix
- Error Matrix

---

## Tags
#confusionmatrix #classification #metrics #machinelearning #modelperformance #datascience

---

## Links to Explore
- [[Accuracy]]: Learn about this foundational metric derived from confusion matrices.
- [[Precision]]: Explore its role in assessing positive predictions.
- [[Recall]]: Understand its importance in measuring model sensitivity.
- [[F1-Score]]: Discover how it balances precision and recall.
- [[Scikit-learn]]: Implement confusion matrices using this popular library.