---
aliases:
  - LSTM
  - LSTMs
---
![[Screenshot 2024-11-18 at 12.01.23 PM.png]]

# LSTMs (Long Short-Term Memory)

## Overview
**Long Short-Term Memory (LSTMs)** are a type of [[Recurrent Neural Network (RNN)]] architecture designed to capture long-term dependencies in sequential data. They were introduced by Hochreiter and Schmidhuber in 1997 to address the [[Vanishing Gradient Problem]] inherent in traditional RNNs. LSTMs are widely used in tasks such as [[Natural Language Processing]] (NLP), [[Time Series Analysis]], and [[Speech Processing]].

---

## Key Concepts

### Memory Cell
- The core of an LSTM is its **memory cell**, which stores information over time.
- Memory cells are updated and controlled by **gates**.

### Gates
LSTMs use three types of gates to regulate the flow of information:
1. **Forget Gate**:
   - Decides which information to discard from the memory cell.
   - Formula:
     $$
     f_t = \sigma(W_f \cdot [h_{t-1}, x_t] + b_f)
     $$
   - $f_t$: Forget gate activation.
   - $x_t$: Input at time \( t \).
   - $h_{t-1}$: Hidden state from the previous time step.

2. **Input Gate**:
   - Decides what new information to add to the memory cell.
   - Formula:
     $$
     i_t = \sigma(W_i \cdot [h_{t-1}, x_t] + b_i)
     $$
     $$
     \tilde{C}_t = \tanh(W_C \cdot [h_{t-1}, x_t] + b_C)
     $$
   - $i_t$: Input gate activation.
   - $\tilde{C}_t$: Candidate values for the memory cell.

3. **Output Gate**:
   - Decides what part of the memory cell should be output as the hidden state.
   - Formula:
	    $$
     o_t = \sigma(W_o \cdot [h_{t-1}, x_t] + b_o)
     $$
     $$
     h_t = o_t \cdot \tanh(C_t)
     $$
   - $o_t$: Output gate activation.
   - $h_t$: Hidden state at time \( t \).

### Memory Cell Update
The memory cell \( C_t \) is updated as:
$$
C_t = f_t \cdot C_{t-1} + i_t \cdot \tilde{C}_t
$$
Where:
- $f_t$: Forget gate activation.
- $C_{t-1}$: Previous memory cell state.
- $i_t$: Input gate activation.
- $\tilde{C}_t$: Candidate memory update.

---

## Applications

### Natural Language Processing
- **Text Generation**: Generate text sequences by predicting the next word or character.
- **Language Modeling**: Model the probability distribution of word sequences.
- **Named Entity Recognition (NER)**: Identify entities in text such as names and dates.

### Time Series Analysis
- **Forecasting**: Predict future values based on past data (e.g., stock prices, weather).
- **Anomaly Detection**: Detect irregular patterns in time-dependent data.

### Speech Processing
- **Speech-to-Text**: Convert spoken language into written text.
- **Audio Synthesis**: Generate or process audio signals.

### Video Processing
- **Action Recognition**: Classify activities in videos.
- **Video Captioning**: Generate textual descriptions for video content.

---

## Advantages

1. **Captures Long-Term Dependencies**:
   - The use of memory cells allows LSTMs to retain information over long sequences.
2. **Mitigates Vanishing Gradients**:
   - Gates help regulate the flow of gradients, improving training stability.
3. **Flexible Architecture**:
   - Can handle variable-length input sequences, making them suitable for diverse tasks.

---

## Disadvantages

1. **Computational Complexity**:
   - LSTMs are computationally expensive due to their gating mechanisms.
2. **Long Training Time**:
   - Slower to train compared to simpler architectures like [[GRUs]] or [[Transformers]].
3. **Difficulty in Parallelization**:
   - Sequential nature of LSTMs limits their parallelization during training.

---

## Variants of LSTMs

### 1. [[Bidirectional LSTMs]]
- Processes input sequences in both forward and backward directions.
- Improves performance on tasks like sentiment analysis and speech recognition.

### 2. [[Stacked LSTMs]]
- Multiple LSTM layers are stacked to capture higher-level sequence features.
- Common in deep learning models for text and speech.

### 3. [[Peephole LSTMs]]
- Includes connections from the memory cell to gates, enabling the gates to access the memory state directly.

---

## Tools and Libraries

### Python Libraries
1. **TensorFlow**:
   - `tf.keras.layers.LSTM`: Built-in support for LSTMs with various configurations.
2. **PyTorch**:
   - `torch.nn.LSTM`: Implementation for building LSTM models.
3. **Keras**:
   - High-level APIs for defining and training LSTM networks.

---

## Related Topics
- [[Recurrent Neural Networks]]: LSTMs are an advanced version of RNNs.
- [[GRUs]]: Simplified alternative to LSTMs with fewer parameters.
- [[Vanishing Gradient Problem]]: A problem mitigated by LSTMs.
- [[Transformers]]: Modern alternative to LSTMs for sequence modeling.

---

## Resources

### Research Papers
- *Long Short-Term Memory* (Hochreiter & Schmidhuber, 1997).

### Tutorials
- TensorFlow and PyTorch official tutorials on LSTMs.
- Hugging Face guides for sequence modeling.

### Books
- *Deep Learning* by Ian Goodfellow, Yoshua Bengio, and Aaron Courville.
- *Speech and Language Processing* by Jurafsky and Martin.

---

## Tags
#LSTMs #RNNs #deep-learning #sequence-modeling #NLP #time-series