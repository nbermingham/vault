# Neural Networks

## Overview
Neural Networks are a subset of [[Machine Learning]] inspired by the structure and functioning of biological neurons in the human brain. They consist of layers of interconnected nodes (neurons) that process and learn from data to make predictions, classify data, or generate outputs.

---

## Key Concepts

### **1. Structure**
- **Input Layer**: Receives the raw data (features).
- **[[Hidden Layers]]**: Perform computations to extract patterns. The number of layers determines the "depth" (e.g., deep learning).
- **Output Layer**: Produces predictions or classifications.
- **Weights and Biases**: Parameters adjusted during training to minimize errors.
- **[[Activation Function]]s**: Introduce non-linearity:
  - Common functions: [[ReLU]], [[Sigmoid]], [[Tanh]].

---

### **2. Types of Neural Networks**
- **Feedforward Neural Networks (FNN)**:
  - Information flows only in one direction (input → output).
  - Example: Basic classifiers.
- **Convolutional Neural Networks (CNN)**:
  - Specialize in image and video recognition.
  - Feature extraction using convolutional layers.
- **Recurrent Neural Networks (RNN)**:
  - Handle sequential data (e.g., time series, text).
  - Include feedback connections for memory (e.g., [[LSTMs]]).
- **Transformer Networks**:
  - State-of-the-art models for NLP (e.g., [[BERT]], [[GPT]]).
- **Generative Adversarial Networks (GANs)**:
  - Generate realistic data (e.g., images, text).

---

### **3. Learning Process**
1. **Forward Propagation**:
   - Data flows through the network to produce predictions.
2. **Loss Function**:
   - Measures the error between predictions and true values (e.g., Mean Squared Error, [[Cross-Entropy Loss]]).
3. **Backward Propagation**:
   - Uses the [[Gradient Descent]] algorithm to update weights by minimizing the loss function.
4. **Optimization**:
   - Algorithms like [[Adam Optimizer]], SGD, or RMSProp adjust parameters for better performance.

---

## Applications
- **Computer Vision**:
  - Object detection, image classification, facial recognition.
- **[[Natural Language Processing]] (NLP)**:
  - Sentiment analysis, translation, text generation.
- **Healthcare**:
  - Disease diagnosis, medical image analysis.
- **Generative Models**:
  - AI art, text-to-image generation (e.g., DALL·E).
- **Autonomous Systems**:
  - Self-driving cars, robotics.

---

## Tools and Frameworks
- **Python Libraries**:
  - [[TensorFlow]]: Comprehensive deep learning framework.
  - [[PyTorch]]: Flexible library for dynamic computation graphs.
  - [[Keras]]: High-level API for TensorFlow.
- **Visualization Tools**:
  - TensorBoard: Monitor training metrics.
  - Matplotlib/Seaborn: Visualize loss and accuracy trends.

---

## Advanced Topics
- [[Backpropagation]]: Algorithm for updating weights during training.
- [[Transfer Learning]]: Reusing pre-trained networks for new tasks.
- [[Regularization]]: Techniques to prevent overfitting (e.g., dropout, L2 regularization).
- [[Hyperparameter Tuning]]: Optimizing learning rate, batch size, etc.
- [[Attention Mechanisms]]: Key innovation in Transformer models.
- [[Explainability in AI]]: Tools like SHAP and LIME for interpreting predictions.

---

## Key Challenges
- **Overfitting**: Model performs well on training data but poorly on unseen data.
  - Solution: Regularization, more training data.
- **Vanishing/Exploding Gradients**: Gradients become too small or too large during backpropagation.
  - Solution: Use better initialization methods or activation functions like ReLU.
- **Computational Cost**: Deep networks require significant resources.
  - Solution: Optimize model architecture and use specialized hardware (e.g., GPUs).

---

## Metrics for Evaluation
- **Regression Tasks**: Mean Squared Error, Mean Absolute Error.
- **Classification Tasks**: Accuracy, Precision, Recall, F1-Score, ROC-AUC.
- **Custom Metrics**: Specific to the application (e.g., BLEU for NLP).

---

## Resources
- **Books**:
  - *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
  - *Neural Networks and Deep Learning* by Michael Nielsen.
- **Online Courses**:
  - Andrew Ng’s *Deep Learning Specialization* on Coursera.
  - *Fast.ai’s Practical Deep Learning for Coders*.
- **Research Papers**:
  - *[[Attention Is All You Need]]* (Transformer introduction).
  - *AlexNet* (CNN breakthrough).

---

## Related Topics
- [[Machine Learning]]: Parent topic of neural networks.
- [[Deep Learning]]: Advanced neural network architectures.
- [[Transformers]]: State-of-the-art NLP architectures.
- [[Gradient Descent]]: Optimization algorithm used in training.

---

## Aliases
- Neural Networks
- Neural Nets
- NN
- Artificial Neural Networks
- ANN
- Feedforward Neural Networks
- Deep Neural Networks
- DNN

---

## Tags
#neuralnetworks #deep-learning #AI #datascience #machinelearning

## Links to Explore
- [[Backpropagation]]: Core training mechanism.
- [[ReLU]]: Common activation function.
- [[TensorFlow]]: Popular framework for building neural networks.
- [[Attention Mechanisms]]: Foundation of transformer models.