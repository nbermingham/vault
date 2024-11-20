## Overview
**BERT** (Bidirectional Encoder Representations from Transformers) is a state-of-the-art NLP model introduced by Google in 2018. It is based on the [[Transformers]] architecture and pre-trained on a massive text corpus. Unlike earlier models like [[Word2Vec]] or [[GloVe]], BERT generates **contextual embeddings**, meaning that the representation of a word changes depending on its context.

---

## Key Concepts

### Contextual Embeddings
- BERT captures the meaning of a word based on its surrounding words.
- For example:
  - "The bank of the river" vs. "The bank approved my loan."
  - The embedding of "bank" differs in each context.

### Bidirectionality
- Unlike unidirectional models like [[GPT]], which read text from left-to-right, BERT reads text **bidirectionally**.
- This allows it to capture context from both the left and right sides of a word.

### Pre-training Tasks
BERT is pre-trained on two unsupervised tasks:
1. **Masked Language Modeling (MLM)**:
   - Randomly masks 15% of tokens in the input and trains the model to predict them.
   - Example:
     - Input: "The cat sat on the [MASK]."
     - Prediction: "mat."
2. **Next Sentence Prediction (NSP)**:
   - Trains the model to predict whether one sentence logically follows another.
   - Example:
     - Sentence A: "I love playing soccer."
     - Sentence B: "The weather is nice today."
     - Prediction: **Not Next**.

---

## Training and Fine-tuning

### Pre-training
- BERT is pre-trained on large corpora like Wikipedia and BookCorpus.
- Pre-training creates general-purpose embeddings for a wide range of NLP tasks.

### Fine-tuning
- After pre-training, BERT is fine-tuned on specific tasks by adding task-specific layers.
- Examples of tasks:
  - [[Text Classification]]: Sentiment analysis, spam detection.
  - [[Named Entity Recognition (NER)]]: Extracting entities like names, dates, and locations.
  - [[Question Answering]]: Answering questions based on given text.

---

## Variants of BERT
1. **Base BERT**:
   - 12 Transformer layers (encoders).
   - Hidden size: 768.
   - Parameters: 110 million.

2. **BERT Large**:
   - 24 Transformer layers (encoders).
   - Hidden size: 1024.
   - Parameters: 340 million.

3. **DistilBERT**:
   - A lighter, faster version of BERT with fewer parameters.
   - Trades off some accuracy for efficiency.

4. **RoBERTa**:
   - A variant of BERT optimized by removing NSP and using a larger training dataset.

5. **ALBERT**:
   - A lightweight version of BERT with reduced memory usage and faster training.

---

## Applications
- **Text [[Classification]]**:
  - Sentiment analysis, spam filtering, and topic categorization.
- **Question Answering**:
  - Models like BERT can answer questions by extracting relevant spans from text.
- **Named Entity Recognition (NER)**:
  - Identify entities like names, locations, and dates.
- **Text Summarization**:
  - Generate concise summaries of longer documents.
- **Language Translation**:
  - Used in combination with other Transformer-based models.

---

## Advantages
1. **Contextual Embeddings**:
   - Captures the true meaning of words in different contexts.
2. **Bidirectional Context**:
   - Utilizes both left and right contexts for better understanding.
3. **Fine-Tuning Flexibility**:
   - Adaptable to a wide range of downstream tasks.

---

## Disadvantages
1. **Computationally Expensive**:
   - Requires significant hardware resources (e.g., GPUs/TPUs) for training and inference.
2. **Large Memory Footprint**:
   - The large number of parameters can be a challenge for deployment.
3. **Interpretability**:
   - Like other deep learning models, BERT’s predictions are often hard to interpret.

---

## How BERT Differs from Word2Vec and GloVe
| **Feature**               | **Word2Vec/GloVe**                 | **BERT**                                 |
|---------------------------|------------------------------------|------------------------------------------|
| **Embeddings**            | Static (one vector per word)      | Contextual (varies by context)           |
| **Architecture**          | Predictive                        | Transformer-based                        |
| **Directionality**        | Unidirectional or no direction    | Bidirectional                            |
| **Applications**          | General-purpose word embeddings   | Task-specific NLP fine-tuning            |

---

## Tools and Libraries

### Hugging Face Transformers
- Provides pre-trained BERT models and tools for fine-tuning.
- Example Models:
  - `bert-base-uncased`: Lowercased English BERT.
  - `bert-large-cased`: Cased English BERT.

### TensorFlow and PyTorch
- Support custom implementations and fine-tuning for BERT.

---

## Related Topics
- [[Transformers]]: The architecture behind BERT.
- [[Embeddings]]: Word and sentence representations learned by BERT.
- [[Fine-Tuning]]: Adapting pre-trained BERT to specific NLP tasks.
- [[RoBERTa]]: A robustly optimized variant of BERT.
- [[GPT]]: A unidirectional language model with similar Transformer architecture.

---

## Resources
- **Research Papers**:
  - "BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding" (Devlin et al., 2018).
- **Books**:
  - *Deep Learning for [[Natural Language Processing]]* by Palash Goyal et al.
- **Courses**:
  - Coursera: *[[Natural Language Processing]] Specialization* by DeepLearning.AI.
  - Hugging Face Course: *Introduction to Transformers*.
- **Tutorials**:
  - Hugging Face documentation on BERT.
  - Google Colab: Fine-tuning BERT on text [[Classification]].

---

## Tags
#BERT #transformers #NLP #machinelearning #contextualembeddings