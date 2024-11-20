# Minority Class

## Overview
The **minority class** refers to the class in a dataset that has significantly fewer instances compared to the other class(es). It is a key concept in imbalanced datasets, where one class (the majority class) dominates the data distribution.

---

## Challenges
1. **Bias Toward Majority Class**:
   - Models tend to prioritize the majority class, leading to poor performance on the minority class.
2. **Metrics Misrepresentation**:
   - Accuracy may be misleading in imbalanced datasets.

---

## Solutions
1. **[[Oversampling]]**:
   - Techniques like [[SMOTE]] generate synthetic samples for the minority class.
2. **[[Undersampling]]**:
   - Reduces the size of the majority class to balance the dataset.
3. **[[Weighted Loss]]**:
   - Penalizes misclassifications of the minority class more heavily during training.

---

## Applications
- Fraud detection, medical diagnosis, anomaly detection, and other tasks where the minority class is critical.

---

## Tags
#minority-class #imbalanced-data #classification