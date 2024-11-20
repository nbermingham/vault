## Overview
**Class Imbalance** refers to a scenario in [[Machine Learning]] where the number of instances in one class is significantly higher than in other classes. It is a common challenge in classification tasks, particularly in domains such as [[Fraud Detection]], [[Medical Diagnosis]], and [[Anomaly Detection]]. Models trained on imbalanced datasets tend to be biased toward the majority class, resulting in poor performance on the minority class.

---

## Key Concepts

1. **Majority Class**:
   - The class with a significantly larger number of instances in the dataset.

2. **Minority Class**:
   - The class with a smaller number of instances, often the class of interest (e.g., detecting fraud or diseases).

3. **Imbalanced Ratios**:
   - A dataset is considered imbalanced when the ratio between the majority and minority classes is high, such as 90:10 or 99:1.

4. **Impact on Metrics**:
   - Standard metrics like [[Accuracy]] can be misleading in imbalanced datasets, as models may achieve high accuracy by predicting only the majority class.

---

## Challenges

1. **Bias Toward Majority Class**:
   - Models tend to predict the majority class more often, ignoring the minority class.

2. **Poor Generalization**:
   - Class imbalance can lead to [[underfitting]] or [[Overfitting]], particularly for the minority class.

3. **Evaluation Metrics**:
   - Common metrics like [[Accuracy]] fail to reflect the model's performance on the minority class.

---

## Solutions

### 1. **Data-Level Techniques**
- **[[Resampling]]**:
  - **Oversampling**:
    - Increase the number of minority class instances using techniques like [[SMOTE]] (Synthetic Minority Oversampling Technique).
  - **[[Undersampling]]**:
    - Reduce the number of majority class instances to balance the dataset.
- **Data Augmentation**:
  - Create synthetic samples for the minority class using transformations or generative models like [[GANs]].

### 2. **Algorithm-Level Techniques**
- **Class Weights**:
  - Assign higher weights to minority class samples in the [[Loss Function]] to penalize misclassification more heavily.
- **Cost-Sensitive Learning**:
  - Modify the model to handle imbalanced data explicitly by considering misclassification costs.

### 3. **Evaluation Metrics**
- Use metrics better suited for imbalanced datasets, such as:
  - [[Precision]], [[Recall]], and [[F1-Score]]
  - [[ROC AUC]]
  - [[Confusion Matrix]]-based metrics like sensitivity and specificity.

---

## Applications

1. **Fraud Detection**:
   - Minority class represents fraudulent transactions, which are rare but critical to detect.
2. **Medical Diagnosis**:
   - Identifying diseases or conditions where positive cases are significantly fewer than negative cases.
3. **Anomaly Detection**:
   - Detecting rare events or abnormalities in systems or data.

---

## Related Topics

- [[Minority Class]]: The underrepresented class in an imbalanced dataset.
- [[Accuracy]]: Often misleading in the presence of class imbalance.
- [[SMOTE]]: A popular oversampling technique to balance datasets.
- [[Precision, Recall, and F1-Score]]: Key metrics for evaluating performance on imbalanced datasets.
- [[ROC AUC]]: Evaluates the ability of the model to separate classes.
- [[Synthetic Data]]: Techniques for generating additional samples for the minority class.

---

## Aliases
- Class Imbalance
- Imbalanced Datasets
- Dataset Imbalance
- Class Distribution Imbalance

---

## Tags
#class-imbalance #imbalanced-datasets #machinelearning #classification #metrics