## Overview
**Convolutional Neural Networks (CNNs)** are a class of [[Neural Networks]] specifically designed for processing structured data, such as images, videos, and spatially-ordered data. CNNs leverage convolutional layers to extract hierarchical features, enabling them to recognize patterns such as edges, textures, and objects. CNNs are widely used in [[Computer Vision]] tasks like [[Image Classification]], [[Object Detection]], and [[Semantic Segmentation]].

CNNs stand out due to their ability to learn spatial hierarchies of features, reducing the need for extensive manual feature engineering.

---

## Key Components

### 1. **Convolutional Layers**
- Perform the convolution operation by sliding filters (kernels) over the input to extract features.
- Key parameters:
  - **Filter Size**: Determines the size of the region each kernel scans.
  - **Stride**: Defines how much the filter moves after each operation.
  - **Padding**: Adds zeros around the input to control the output size.
- Output:
  - Feature maps, which highlight patterns detected by filters.

### 2. **[[Pooling Layers]]**
- Reduce the spatial dimensions of feature maps, preserving important features while minimizing computational cost.
- Types:
  - **Max Pooling**: Selects the maximum value in each region.
  - **Average Pooling**: Computes the average value in each region.

### 3. **[[Fully Connected Layers]]**
- Flatten feature maps and connect them to output layers for predictions.
- Often used for tasks like classification.

### 4. **[[Activation Functions]]**
- Common activations include [[ReLU]], [[Leaky ReLU]], and [[Softmax Function]] to introduce non-linearity and enable classification.

### 5. **[[Batch Normalization]]**
- Normalizes activations to stabilize and speed up training.

---

## Workflow

1. **Input Layer**:
   - Accepts structured data like images, typically in 2D or 3D formats (e.g., width × height × channels).

2. **[[Feature Extraction]]**:
   - Convolutional layers detect patterns, and pooling layers reduce spatial dimensions.

3. **[[Classification]]**:
   - Fully connected layers process the extracted features to produce predictions (e.g., class probabilities).

---

## Applications

1. **Image Classification**:
   - Assigns labels to input images (e.g., [[Cats vs Dogs]]).
   - Example: [[AlexNet]], [[VGG]], [[ResNets]].

2. **Object Detection**:
   - Identifies and localizes objects in an image (e.g., [[YOLO]], [[Faster R-CNN]]).

3. **Semantic Segmentation**:
   - Classifies each pixel in an image to understand the spatial structure.

4. **Video Analysis**:
   - Tasks like action recognition and video summarization.

5. **[[Medical Imaging]]**:
   - Analyzing X-rays, MRIs, or CT scans for diagnostic purposes.

---

## Advantages

1. **Automatic Feature Extraction**:
   - CNNs learn features directly from data, reducing the need for manual feature engineering.

2. **Translation Invariance**:
   - Convolutional layers capture patterns regardless of their location in the input.

3. **Parameter Efficiency**:
   - Shared weights in convolutional layers reduce the number of parameters compared to fully connected networks.

---

## Disadvantages

1. **Computational Cost**:
   - Training CNNs on large datasets requires significant computational resources (e.g., GPUs or TPUs).

2. **Data Requirements**:
   - CNNs perform best with large amounts of labeled data.

3. **Interpretability**:
   - Understanding how CNNs make decisions can be challenging compared to simpler models.

---

## Architectures

1. **AlexNet**:
   - Introduced deep learning to [[Image Classification]] in 2012.

2. **VGG**:
   - Explored deeper networks with small 3×3 filters.

3. **ResNets**:
   - Used [[Residual Connections]] to enable training of very deep networks.

4. **YOLO**:
   - Designed for real-time [[Object Detection]].

5. **Faster R-CNN**:
   - A two-stage detector for object detection tasks.

---

## Related Topics

- [[Neural Networks]]: CNNs are a specialized type of neural network.
- [[ReLU]]: The most commonly used activation function in CNNs.
- [[Pooling Layers]]: Essential for dimensionality reduction in CNNs.
- [[Residual Connections]]: Used in advanced architectures like [[ResNets]].
- [[Batch Normalization]]: Improves training stability in CNNs.
- [[Object Detection]]: A key application area of CNNs.
- [[Transformers in Computer Vision]]: Emerging alternatives to CNNs for vision tasks.

---

## Aliases
- Convolutional Neural Networks
- CNNs
- ConvNets
- Convolutional Networks
- Convolutional Models

---

## Tags
#cnn #convolutional-neural-networks #deep-learning #computer-vision #image-classification #object-detection