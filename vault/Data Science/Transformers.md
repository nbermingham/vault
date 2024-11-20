---
aliases:
  - Transformer
  - Transformer Architecture
---

## Overview
The **Transformer** is a neural network architecture introduced in the paper *"[[Attention Is All You Need]]"* by [[Vaswani et al.]] in 2017. It revolutionized [[Natural Language Processing]] (NLP) by enabling parallelized training and leveraging the powerful **attention mechanism** to model long-range dependencies in sequences. Transformers are the backbone of models like [[BERT]], [[GPT]], and [[T5]].

---

## Key Concepts

### [[Attention Mechanism]]
- The Transformer relies on the **self-attention mechanism** to weigh the importance of different words in a sequence relative to each other.
- **Self-Attention**:
  - Computes relationships between all words in a sequence, allowing the model to focus on relevant parts of the input.
  - Example: In the sentence "The cat sat on the mat," the word "cat" has a higher relationship to "sat" than "mat."

### Parallelization
- Unlike [[Recurrent Neural Networks (RNNs)]], Transformers do not process input sequentially. Instead, they process all tokens simultaneously, enabling faster training.

### [[Encoder-Decoder Architecture]]
- The Transformer consists of two main components:
  1. **[[Encoder-Only Architecture]]**:
     - Maps the input sequence into a sequence of continuous representations.
     - Used in tasks like sentence [[Classification]] and feature extraction.
  2. **[[Decoder-Only Architecture]]**:
     - Generates the output sequence from the encoded representations.
     - Used in tasks like translation and text generation.

---

## Architecture

### Input Representation
- Input tokens are converted to embeddings (e.g., word embeddings or [[Positional Encoding]]).
- Positional encodings are added to embeddings to incorporate order information since Transformers do not process tokens sequentially.

### Multi-Head Self-Attention
- Splits attention into multiple "heads" to capture different types of relationships between tokens.
- Each head computes attention independently, and their results are concatenated and transformed.

### Feedforward Layers
- Fully connected layers that process the output of the attention mechanism for each token.

### Residual Connections
- Add input to the output of each layer to stabilize gradients during training.

### Layer Normalization
- Normalizes the output of each layer to improve convergence.

---

## Mathematical Components

### Scaled Dot-Product Attention
$$
\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^\top}{\sqrt{d_k}}\right)V
$$
Where:
- $Q$: Query matrix.
- $K$: Key matrix.
- $V$: Value matrix.
- $d_k$: Dimensionality of the key vectors (scaling factor).

### [[Multi-Head Attention]]
$$
\text{MultiHead}(Q, K, V) = \text{Concat}(\text{head}_1, \dots, \text{head}_h)W^O
$$
Where:
- Each head computes scaled dot-product attention.

### [[Positional Encoding]]
- Adds information about the order of tokens in a sequence.
- Example (sinusoidal encoding):
$$
PE(pos, 2i) = \sin(pos / 10000^{2i/d})
$$
$$
PE(pos, 2i+1) = \cos(pos / 10000^{2i/d})
$$

---

## Applications

### [[Natural Language Processing]]
- **Machine Translation**: Convert text from one language to another.
- **Text Generation**: Models like [[GPT]] generate coherent and context-aware text.
- **Text Summarization**: Create concise summaries of longer documents.

### [[Computer Vision]]
- **Vision Transformers (ViT)**: Adapt Transformers for image recognition by dividing images into patches.

### Speech Processing
- Models like Wav2Vec use Transformer-based architectures for speech-to-text and other audio tasks.

---

## Advantages
1. **Parallelization**:
   - Allows for faster training compared to sequential models like RNNs.
2. **Handles Long Dependencies**:
   - Models relationships between tokens across long sequences.
3. **Generalizable**:
   - Can be applied to multiple domains beyond NLP, such as vision and speech.

---

## Disadvantages
1. **Computational Cost**:
   - Transformers require significant computational resources, especially for long sequences.
2. **Memory Usage**:
   - Self-attention scales quadratically with sequence length, making it memory-intensive.
3. **Data Requirements**:
   - Requires large amounts of data for effective training.

---

## Variants of Transformers

### BERT (Bidirectional Encoder Representations from Transformers)
- Pre-trained Transformer encoder for contextual embeddings.

### GPT (Generative Pre-trained Transformer)
- Decoder-only Transformer for text generation.

### T5 (Text-to-Text Transfer Transformer)
- Treats every NLP task as a text-to-text problem.

### Vision Transformers (ViT)
- Adapts the Transformer architecture for image [[Classification]].

---

## Tools and Libraries
- **Hugging Face Transformers**:
  - Library for pre-trained Transformer models (e.g., BERT, GPT, T5).
- **TensorFlow and PyTorch**:
  - Frameworks for custom Transformer implementations.
- **OpenAI API**:
  - Provides access to GPT models for text generation.

---

## Related Topics
- [[Self-Attention]]: Core mechanism behind Transformers.
- [[BERT]]: Transformer-based encoder model.
- [[GPT]]: Transformer-based decoder model for text generation.
- [[Multi-Head Attention]]: Key component of the Transformer architecture.

---

## Resources
- **Research Papers**:
  - "[[Attention Is All You Need]]" (Vaswani et al., 2017).
- **Books**:
  - *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
- **Courses**:
  - Coursera: *[[Natural Language Processing]] Specialization* by DeepLearning.AI.
  - Hugging Face Course: *Transformers in NLP*.

---

## Tags
#transformers #machinelearning #NLP #attentionmechanism #deep-learning