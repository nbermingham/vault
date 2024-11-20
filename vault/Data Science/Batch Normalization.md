## Overview
**Batch Normalization (BatchNorm)** is a technique used in [[Deep Learning]] to improve the training stability and speed of [[Neural Networks]]. It normalizes the input to each layer by adjusting and scaling the activations, ensuring that their distribution remains consistent throughout training. This helps mitigate issues like the [[Vanishing Gradient Problem]] and allows the use of higher learning rates.

Batch Normalization is applied to mini-batches of data and is now a standard component in many modern architectures, such as [[Convolutional Neural Networks (CNNs)]] and [[Recurrent Neural Networks (RNNs)]].

---

## Key Concepts

1. **Normalization**:
   - For each mini-batch, the activations are normalized to have zero mean and unit variance:
     $$
     \hat{x}_i = \frac{x_i - \mu}{\sqrt{\sigma^2 + \epsilon}}
     $$
     Where:
     - $\mu$: Mean of the mini-batch.
     - $\sigma^2$: Variance of the mini-batch.
     - $\epsilon$: Small constant to avoid division by zero.

2. **Learnable Parameters**:
   - To retain the network's capacity to learn, BatchNorm introduces two learnable parameters:
     - $\gamma$: Scale parameter.
     - $\beta$: Shift parameter.
   - The final normalized output becomes:
     $$
     y_i = \gamma \hat{x}_i + \beta
     $$

3. **Layer Independence**:
   - Normalization reduces the dependence of layer outputs on the distribution of previous layers' activations, a phenomenon known as [[Internal Covariate Shift]].

---

## Advantages

1. **Faster Training**:
   - By normalizing activations, BatchNorm allows the use of higher learning rates, reducing training time.

2. **Improved Gradient Flow**:
   - Helps address the [[Vanishing Gradient Problem]] by maintaining stable activation distributions.

3. **Regularization Effect**:
   - Acts as a form of regularization, reducing the need for techniques like [[Dropout]] in some cases.

4. **Stabilized Training**:
   - Reduces sensitivity to [[Weight Initialization]] and learning rate selection.

---

## Disadvantages

1. **Dependence on Mini-Batches**:
   - BatchNorm relies on statistics computed from mini-batches, which may lead to instability when batch sizes are very small.

2. **Computational Overhead**:
   - Adds extra computation during training, especially for large networks like [[Convolutional Neural Networks (CNNs)]].

3. **Issues During Inference**:
   - BatchNorm uses moving averages of mean and variance during inference, which may not always represent the training data accurately.

---

## Applications

1. **Convolutional Neural Networks (CNNs)**:
   - BatchNorm is widely used in [[Image Classification]] and [[Object Detection]] tasks to accelerate training.

2. **Recurrent Neural Networks (RNNs)**:
   - Variants of BatchNorm are used to stabilize training in recurrent architectures.

3. **Deep Architectures**:
   - Found in modern architectures like [[ResNets]] and [[Transformers]] to improve training efficiency.

---

## Steps in Batch Normalization

1. **Compute Batch Statistics**:
   - Calculate the mean ($\mu$) and variance ($\sigma^2$) of the activations for the current mini-batch.

2. **Normalize Activations**:
   - Subtract the mean and divide by the standard deviation to standardize the activations.

3. **Scale and Shift**:
   - Apply the learnable parameters ($\gamma$ and $\beta$) to adjust the normalized values.

4. **Use During Inference**:
   - Use moving averages of $\mu$ and $\sigma^2$ instead of batch statistics to ensure consistency.

---

## Related Topics

- [[Vanishing Gradient Problem]]: BatchNorm helps alleviate this issue by stabilizing [[Gradients]].
- [[Weight Initialization]]: Works in tandem with BatchNorm to ensure better training convergence.
- [[Dropout]]: Another regularization technique, often used alongside BatchNorm.
- [[ResNets]]: Incorporate BatchNorm to stabilize training in very deep networks.
- [[Transformers]]: Use LayerNorm, a related technique, in place of BatchNorm.

---

## Aliases
- Batch Normalization
- BatchNorm
- Mini-Batch Normalization
- BN
- Normalization Layer

---

## Tags
#batch-normalization #normalization #deep-learning #neural-networks #vanishing-gradients #optimization