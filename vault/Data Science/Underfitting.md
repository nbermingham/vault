## Overview
**Underfitting** occurs when a [[Machine Learning]] model is too simple to capture the underlying patterns in the training data, resulting in poor performance on both the training and test datasets. Underfitting often arises when the model has high [[Bias]] and low complexity, failing to learn from the data effectively.

Underfitting is the opposite of [[Overfitting]], where the model is overly complex and fits the noise in the data rather than the true patterns.

---

## Key Characteristics

1. **High Training Error**:
   - The model performs poorly even on the training dataset, indicating it has not learned the patterns in the data.
2. **High Test Error**:
   - The model fails to generalize to unseen data due to inadequate learning.
3. **Simplistic Model**:
   - The model lacks the complexity needed to represent the data (e.g., using a [[Linear Regression]] model for highly non-linear data).

---

## Causes of Underfitting

1. **Model Simplicity**:
   - Using a model that is too simple for the problem (e.g., [[Linear Models]] for non-linear problems).
2. **Insufficient Features**:
   - Not providing the model with enough relevant features to learn the target patterns.
3. **Inadequate Training**:
   - Training the model for too few epochs or iterations.
4. **Over-Regularization**:
   - Excessive use of [[Regularization]] techniques like [[Lasso Regression|L1 Regularization]] or [[Ridge Regression|L2 Regularization]].

---

## Symptoms of Underfitting

1. **Linear Decision Boundaries**:
   - A model that creates overly simplistic boundaries for classification tasks.
2. **Poor Training Metrics**:
   - High [[Loss Function]] values or low [[Accuracy]] on the training dataset.
3. **Flat Learning Curve**:
   - Minimal improvement in metrics as training progresses.

---

## Solutions to Underfitting

1. **Increase Model Complexity**:
   - Use more complex models like [[Neural Networks]] or [[Polynomial Regression]] for non-linear data.
2. **Feature Engineering**:
   - Add relevant features, perform [[Feature Selection]], or create polynomial features.
3. **Reduce Regularization**:
   - Decrease the strength of [[Regularization]] techniques to allow the model more flexibility.
4. **Train Longer**:
   - Train the model for more epochs or iterations to ensure it has learned sufficiently from the data.
5. **Use Better Initialization**:
   - Optimize weight initialization to help the model converge effectively.

---

## Examples

1. **Linear Regression**:
   - Using [[Linear Regression]] to fit a dataset with non-linear relationships will result in underfitting.
2. **Shallow Neural Networks**:
   - A neural network with insufficient layers or neurons may fail to capture complex patterns.

---

## Related Topics

- [[Overfitting]]: The counterpart of underfitting, where the model is overly complex.
- [[Bias-Variance Tradeoff]]: Underfitting is associated with high bias.
- [[Regularization]]: While preventing overfitting, excessive regularization can cause underfitting.
- [[Feature Engineering]]: Helps mitigate underfitting by enriching the dataset.
- [[Loss Function]]: High training loss indicates underfitting.

---

## Aliases
- Underfitting
- High Bias
- Model Underfitting

---

## Tags
#underfitting #machinelearning #biasvariance #regularization #modelperformance

---

## Links to Explore
- [[Overfitting]]: Understand the opposite phenomenon of underfitting.
- [[Bias-Variance Tradeoff]]: Learn how underfitting relates to high bias.
- [[Regularization]]: Explore its role in preventing and causing underfitting.
- [[Loss Function]]: Identify underfitting using training loss metrics.
- [[Feature Engineering]]: Improve model performance to mitigate underfitting.