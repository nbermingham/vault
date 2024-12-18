## Overview
**BERT Embeddings** are contextualized word embeddings generated by the [[BERT]] (Bidirectional Encoder Representations from Transformers) model. Unlike traditional embeddings like [[Word2Vec]] or [[GloVe]], which generate static embeddings, BERT embeddings consider the context in which a word appears, producing different embeddings for the same word depending on its surrounding text.

BERT embeddings are widely used in [[Natural Language Processing]] tasks such as text classification, [[Named Entity Recognition (NER)]], and [[Machine Translation]].

---

## Key Concepts

### **1. Contextualized Word Embeddings**
- Traditional embeddings represent words as fixed vectors regardless of context.
- BERT embeddings dynamically adjust word representations based on the sentence in which the word appears.
  - Example:
    - "The bank is by the river" and "He went to the bank for a loan" generate different embeddings for "bank."

### **2. Tokenization**
- BERT uses [[WordPiece Tokenization]] to split words into subword units.
  - Example:
    - "unbelievable" → ["un", "##believable"]
- Each token is mapped to an embedding vector.

### **3. Embedding Layers in BERT**
BERT embeddings are generated from the sum of:
1. **Token Embeddings**:
   - Represent individual tokens (subwords).
2. **Position Embeddings**:
   - Encodes the position of tokens in a sequence.
   - Related to [[Positional Encoding]].
3. **Segment Embeddings**:
   - Distinguishes between different segments in input pairs (e.g., question vs. answer).

---

## Applications

1. **Text Classification**:
   - Use BERT embeddings as input features for tasks like sentiment analysis.
2. **[[Named Entity Recognition (NER)]]**:
   - Extract entities like names, dates, and locations using contextual embeddings.
3. **Question Answering**:
   - BERT embeddings power models to extract relevant answers from text.
4. **Semantic Search**:
   - Embed sentences for similarity comparison in [[Information Retrieval]] tasks.
5. **Machine Translation**:
   - Represent contextual meaning in multilingual settings.

---

## Advantages

1. **Context Awareness**:
   - Produces embeddings that adapt to word usage in different contexts.
2. **Rich Representations**:
   - Captures complex syntactic and semantic relationships.
3. **Transfer Learning**:
   - Pre-trained BERT models provide high-quality embeddings for various downstream tasks.

---

## Disadvantages

1. **Computational Cost**:
   - Generating BERT embeddings requires significant computational resources.
2. **Sentence Length Limit**:
   - BERT embeddings are limited to a fixed input length (typically 512 tokens).
3. **Complexity**:
   - Requires understanding of [[Transformers]] architectures and tokenization.

---

## Workflow

1. **Tokenize Text**:
   - Preprocess input text using BERT’s tokenizer (e.g., [[WordPiece Tokenization]]).
2. **Input to BERT**:
   - Feed tokenized text to a pre-trained BERT model.
3. **Extract Embeddings**:
   - Choose output layers for embeddings:
     - **CLS Token**: Represents the entire input sequence.
     - **Token-Level Outputs**: Contextual embeddings for individual tokens.
4. **Use for Downstream Tasks**:
   - Pass embeddings to task-specific models (e.g., [[Linear Regression]] for classification).

---

## Tools and Libraries

1. **Hugging Face Transformers**:
   - `transformers` library provides pre-trained BERT models for generating embeddings.
2. **TensorFlow and PyTorch**:
   - Frameworks for integrating BERT embeddings into custom models.

---

## Related Topics

- [[BERT]]: The architecture behind BERT embeddings.
- [[Transformers]]: Core architecture enabling contextual embeddings.
- [[Word2Vec]]: A static embedding method for comparison.
- [[Contextual Embeddings]]: Broader category of embeddings like [[ELMo]] and [[GPT]] embeddings.
- [[Transfer Learning]]: Use pre-trained BERT embeddings for new tasks.

---

## Aliases
- BERT Embeddings
- Contextual Word Embeddings (BERT)
- BERT Sentence Embeddings

---

## Tags
#bert #transformers #nlp #embeddings #machinelearning #deeplearning

---

## Links to Explore
- [[BERT]]: Learn about the model generating these embeddings.
- [[Transformers]]: Understand the mechanism enabling contextual embeddings.
- [[Word2Vec]]: Compare with static embeddings.
- [[Hugging Face]]: Use their tools to extract BERT embeddings easily.
- [[Named Entity Recognition (NER)]]: Discover applications of token-level embeddings.