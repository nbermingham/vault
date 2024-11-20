## Overview
**ROC AUC (Receiver Operating Characteristic - Area Under the Curve)** is a metric used to evaluate the performance of classification models, particularly binary classifiers. The **ROC (Receiver Operating Characteristic)** curve plots the trade-off between the [[True Positive Rate]] (TPR) and the [[False Positive Rate]] (FPR) at various threshold settings. The **AUC (Area Under the Curve)** quantifies the overall ability of the model to distinguish between classes, with values ranging from 0 to 1.

---

## Key Concepts

### ROC Curve
The ROC curve is a plot of:
- **True Positive Rate (TPR)**: Proportion of correctly classified positive samples.
  $$
  TPR = \frac{\text{TP}}{\text{TP} + \text{FN}}
  $$
- **False Positive Rate (FPR)**: Proportion of negative samples incorrectly classified as positive.
  $$
  FPR = \frac{\text{FP}}{\text{FP} + \text{TN}}
  $$
Each point on the curve represents a different threshold for classifying predictions as positive or negative.

### AUC (Area Under the Curve)
- Measures the total area under the ROC curve.
- **Interpretation**:
  - $AUC = 1.0$: Perfect classifier.
  - $AUC = 0.5$: Random guess.
  - $AUC < 0.5$: Worse than random guessing (indicates a model may be inverted).

---

## Advantages

1. **Threshold Independence**:
   - ROC AUC evaluates model performance across all classification thresholds, making it a robust metric.
2. **Handles Imbalanced Datasets**:
   - Unlike accuracy, ROC AUC provides meaningful insights even for datasets with imbalanced class distributions.
3. **Visual Interpretation**:
   - The ROC curve provides a clear visualization of the trade-offs between TPR and FPR.

---

## Disadvantages

1. **Focus on Rankings**:
   - Evaluates the ranking quality of predictions, not absolute probability calibration.
2. **Less Informative for Highly Imbalanced Data**:
   - Precision-Recall AUC may be more appropriate when the focus is on the minority class.
3. **Not Always Interpretable**:
   - AUC scores are not intuitive for non-technical stakeholders.

---

## Applications

1. **Binary Classification**:
   - Evaluating models like [[Logistic Regression]], [[Random Forest]], or [[Neural Networks]].
   - Examples: Spam detection, disease prediction.
2. **Threshold Selection**:
   - Analyzing the ROC curve helps choose an optimal threshold balancing TPR and FPR.
3. **Model Comparison**:
   - Comparing ROC AUC scores across multiple models to select the best-performing one.

---

## Workflow for ROC AUC Evaluation

1. **Train a Classification Model**:
   - Fit the model to your training data.
2. **Predict Probabilities**:
   - Use the model to generate predicted probabilities for the positive class.
3. **Plot ROC Curve**:
   - Plot the TPR vs. FPR at different thresholds.
4. **Calculate AUC**:
   - Compute the AUC score using libraries like Scikit-learn.

---

## ROC AUC vs. Precision-Recall AUC

| Feature                | ROC AUC                           | Precision-Recall AUC                                 |
| ---------------------- | --------------------------------- | ---------------------------------------------------- |
| **Focus**              | Balances TPR and FPR              | Emphasizes performance on the [[Minority Class]]     |
| **Imbalanced Data**    | Less sensitive to class imbalance | Better for highly imbalanced datasets                |
| **Threshold Insights** | Evaluates across all thresholds   | Focuses on thresholds relevant to the positive class |

---

## Tools and Libraries

1. **Scikit-learn**:
   - `roc_auc_score`: Computes the AUC score.
   - `roc_curve`: Generates TPR and FPR values for plotting the ROC curve.
2. **Matplotlib/Seaborn**:
   - Used for visualizing the ROC curve.
3. **TensorFlow/Keras**:
   - Includes metrics for ROC AUC during training and evaluation.

---

## Example ROC AUC Interpretation

- **Model A**: AUC = 0.85
  - Performs well at distinguishing between positive and negative classes.
- **Model B**: AUC = 0.65
  - Better than random guessing but requires improvement.

---

## Related Topics

- [[Precision-Recall Curve]]: A complementary evaluation metric for imbalanced datasets.
- [[Binary Classification]]: ROC AUC is a standard metric for evaluating binary classifiers.
- [[Threshold Selection]]: Choosing decision thresholds based on ROC or other metrics.

---

## Resources

### Tutorials
- Scikit-learn's guide to ROC AUC and ROC curve visualization.
- Online tutorials on evaluating binary classifiers using ROC AUC.

### Books
- *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* by Aurélien Géron.
- *Introduction to Statistical Learning* by James et al.

### Research Papers
- *Receiver Operating Characteristic (ROC) Analysis in Machine Learning* by Fawcett, 2006.

---

## Tags
#ROC-AUC #model-evaluation #classification-metrics #binary-classification #machinelearning