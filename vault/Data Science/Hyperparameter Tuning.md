## Overview
Hyperparameter tuning is the process of optimizing a machine learning model's hyperparameters to improve performance. Unlike model parameters (learned during training), hyperparameters are set before training and control how the model learns.

---

## Key Concepts

### **1. Hyperparameters**
- **Definition**: Hyperparameters are configuration settings that influence model behavior.
- **Examples**:
  - Learning rate (\(\alpha\)): Controls the step size for weight updates during [[Gradient Descent]].
  - Number of hidden layers and neurons: Architecture of neural networks.
  - Regularization strength: Controls overfitting (e.g., L1/L2 penalties).
  - Batch size: Number of samples processed at a time.
  - Number of epochs: Number of times the model sees the entire dataset.

### **2. Model Parameters vs. Hyperparameters**
| **Model Parameters**            | **Hyperparameters**         |
|----------------------------------|-----------------------------|
| Learned during training.         | Set manually or via tuning. |
| E.g., weights and biases.        | E.g., learning rate, batch size. |

---

## Tuning Strategies

### **1. Manual Tuning**
- Adjust hyperparameters by trial and error.
- Suitable for simple models but time-consuming and error-prone.

### **2. Grid Search**
- Explores a pre-defined grid of hyperparameter combinations.
- Example:
  ```python
  from sklearn.model_selection import GridSearchCV
  grid = {'learning_rate': [0.01, 0.1, 0.5], 'batch_size': [32, 64, 128]}