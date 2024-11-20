## Overview
**Masked Language Modeling (MLM)** is a training objective used in [[Encoder-Only Architecture]] models like [[BERT]]. In MLM, some tokens in the input sequence are randomly masked, and the model is trained to predict the original tokens at the masked positions. This approach enables the model to learn bidirectional context, making it ideal for [[Natural Language Understanding (NLU)]] tasks.

MLM is a foundational technique for pre-training [[Large Language Models (LLMs)]] that require a deep understanding of input text, such as [[Text Classification]] or [[Named Entity Recognition (NER)]].

---

## Key Concepts

### **1. Objective**
The goal of MLM is to predict masked tokens in the input sequence:
$$
L = - \sum_{i \in \text{masked}} \log P(x_i \mid x_{\backslash i})
$$
Where:
- $x_i$: Masked token to predict.
- $x_{\backslash i}$: All other tokens in the input sequence.

---

### **2. Bidirectional Context**
- Unlike [[Causal Language Modeling (CLM)]], MLM uses bidirectional context, allowing the model to consider both preceding and succeeding tokens when predicting the masked token.
- This makes MLM particularly effective for understanding relationships between words and phrases.

---

### **3. Masking Strategy**
- A certain percentage (e.g., 15%) of tokens are masked during training.
- Of the masked tokens:
  - 80% are replaced with a special `[MASK]` token.
  - 10% are replaced with a random token.
  - 10% remain unchanged.
- This variability ensures the model generalizes better and avoids over-relying on the `[MASK]` token.

---

## Applications

1. **Natural Language Understanding (NLU)**:
   - Tasks like [[Text Classification]], [[Sentiment Analysis]], and [[Named Entity Recognition (NER)]].
2. **Question Answering**:
   - Enables the model to understand and extract relevant information from text.
3. **Sentence Pair Tasks**:
   - Tasks like [[Semantic Similarity]] and [[Natural Language Inference (NLI)]].
4. **Feature Extraction**:
   - Pre-trained MLMs like [[BERT]] can generate embeddings for downstream tasks.

---

## Advantages

1. **Bidirectional Context**:
   - Leverages both past and future context for better language understanding.
2. **Strong Pre-Training Signal**:
   - Effective for learning deep relationships in text.
3. **Transferability**:
   - Pre-trained MLMs can be fine-tuned for a wide range of tasks.

---

## Disadvantages

1. **Inapplicability to Generation Tasks**:
   - Cannot be used directly for [[Text Generation]] due to the lack of autoregressive structure.
2. **Dependency on [MASK] Token**:
   - The `[MASK]` token does not appear during fine-tuning or inference, potentially causing a mismatch.
3. **Computationally Intensive**:
   - Requires large-scale data and resources for effective pre-training.

---

## Prominent Models

1. **[[BERT]]**:
   - Introduced MLM as a pre-training objective.
2. **[[RoBERTa]]**:
   - Optimized BERT by modifying masking strategies and removing next-sentence prediction.
3. **[[ELECTRA]]**:
   - Replaces masked token prediction with a discriminator model to classify replaced tokens.

---

## Tools and Libraries

1. **Hugging Face Transformers**:
   - Provides pre-trained MLM-based models like BERT and RoBERTa.
2. **PyTorch**:
   - Supports custom MLM implementations with encoder-based architectures.
3. **TensorFlow**:
   - Offers APIs for training and fine-tuning MLM models.

---

## Related Topics

- [[BERT]]: The first major model trained using MLM.
- [[Encoder-Only Architecture]]: The design suited for MLM-based tasks.
- [[Fine-Tuning]]: Adapting pre-trained MLM models for specific tasks.
- [[Causal Language Modeling (CLM)]]: A contrasting autoregressive training objective.
- [[Tokenization]]: Preprocessing step critical for MLM training.

---

## Aliases
- Masked Language Modeling
- MLM
- Masked Token Prediction

---

## Tags
#maskedlanguagemodeling #transformer #NLP #machinelearning #LLMs #textunderstanding

---

## Links to Explore
- [[BERT]]: Dive into the model that introduced MLM.
- [[Encoder-Only Architecture]]: Learn about the structure optimized for MLM.
- [[Causal Language Modeling (CLM)]]: Compare MLM with this autoregressive approach.
- [[Fine-Tuning]]: Discover how to adapt MLM-based models for specific tasks.
- [[Tokenization]]: Explore the preprocessing step critical for masking tokens.