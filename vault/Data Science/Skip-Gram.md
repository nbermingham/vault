## Overview
**Skip-Gram** is a method used in [[Word2Vec]] for learning word embeddings by predicting the context words given a target word. It focuses on capturing the semantic relationships between words by maximizing the probability of context words occurring around a given target word. Skip-Gram is especially effective at learning embeddings for rare words.

Skip-Gram, along with [[Continuous Bag of Words (CBOW)]], was introduced by [[Tomas Mikolov]] as part of the Word2Vec model. It is widely used in [[Natural Language Processing]] to generate dense, context-aware vector representations of words.

---

## Key Concepts

### **1. Objective**
The primary goal of Skip-Gram is to maximize the probability of context words $w_{t-k}, \dots, w_{t-1}, w_{t+1}, \dots, w_{t+k}$ given a target word $w_t$ within a window of size $k$. The model optimizes the following:
$$
L = \sum_{t=1}^T \sum_{-k \leq j \leq k, j \neq 0} \log P(w_{t+j} \mid w_t)
$$
Where:
- $w_t$: Target word.
- $w_{t+j}$: Context word.
- $k$: Window size around the target word.

---

### **2. Architecture**
1. **Input Layer**:
   - The target word is represented as a one-hot vector.
2. **Hidden Layer**:
   - Projects the one-hot vector into a dense vector representation using an embedding matrix.
3. **Output Layer**:
   - Predicts the context words using the embedding of the target word.
4. **Loss Function**:
   - Negative log likelihood is used to maximize the probability of context words.

---

### **3. Comparison with CBOW**
- **Skip-Gram**:
  - Predicts context words given a target word.
  - Works well for rare words and large datasets.
- **CBOW**:
  - Predicts the target word given its context.
  - Focuses more on frequent words and is computationally efficient.

---

## Applications

1. **Word Embedding Generation**:
   - Learns dense vector representations that capture semantic and syntactic relationships.
2. **Semantic Similarity**:
   - Useful in tasks like [[Semantic Similarity]], [[Text Classification]], and [[Named Entity Recognition (NER)]].
3. **Preprocessing for NLP Models**:
   - Skip-Gram embeddings can be used as input features for downstream tasks.

---

## Advantages

1. **Effective for Rare Words**:
   - Handles infrequent words better than [[Continuous Bag of Words (CBOW)]].
2. **Rich Context Representation**:
   - Captures subtle semantic relationships between words.
3. **Task Adaptability**:
   - Embeddings learned via Skip-Gram are highly transferable across NLP tasks.

---

## Disadvantages

1. **Computational Cost**:
   - Skip-Gram requires more computation compared to CBOW, especially for large vocabularies.
2. **Fixed Context Window**:
   - Limited ability to capture long-range dependencies.
3. **Data Dependency**:
   - Performance depends on the quality and size of the training corpus.

---

## Example Workflow

1. **Prepare Data**:
   - Tokenize text and create pairs of target and context words using a sliding window.
2. **Train Skip-Gram Model**:
   - Use frameworks like Gensim or TensorFlow to train the model.
3. **Generate Embeddings**:
   - Extract learned embeddings for use in downstream NLP tasks.

---

## Tools and Libraries

1. **Gensim**:
   - Provides prebuilt implementations for Skip-Gram and [[CBOW]].
2. **TensorFlow**:
   - Allows for custom implementation of Skip-Gram.
3. **PyTorch**:
   - Useful for building Skip-Gram models with flexibility.

---

## Related Topics

- [[Word2Vec]]: The overarching framework that introduced Skip-Gram and CBOW.
- [[Continuous Bag of Words (CBOW)]]: The complementary architecture to Skip-Gram in Word2Vec.
- [[Embeddings]]: Dense vector representations learned using Skip-Gram.
- [[Semantic Similarity]]: Skip-Gram embeddings are often used for similarity computations.
- [[Text Classification]]: A common downstream task for embeddings generated by Skip-Gram.

---

## Aliases
- Skip-Gram
- SkipGram
- Word2Vec Skip-Gram

---

## Tags
#skipgram #Word2Vec #embeddings #NLP #machinelearning #textprocessing

---

## Links to Explore
- [[Word2Vec]]: Learn about the framework encompassing Skip-Gram.
- [[Continuous Bag of Words (CBOW)]]: Compare Skip-Gram with its counterpart in Word2Vec.
- [[Embeddings]]: Understand how Skip-Gram generates dense vector representations.
- [[Semantic Similarity]]: Explore applications of Skip-Gram in measuring text similarity.
- [[Gensim]]: Discover tools for implementing Skip-Gram models.