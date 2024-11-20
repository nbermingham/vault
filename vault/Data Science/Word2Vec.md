## Overview
**Word2Vec** is a word embedding model that learns dense vector representations of words based on their context in a corpus. It was introduced by [[Tomas Mikolov]] in 2013 and is widely used in [[Natural Language Processing]] (NLP) tasks. The key idea is that semantically similar words are mapped to nearby points in a continuous vector space.

---

## Key Concepts

### Distributional Hypothesis
- Word2Vec is based on the **distributional hypothesis**, which states: *"Words that occur in similar contexts tend to have similar meanings."*
- This is implemented by training the model to predict the context of a word or the word itself based on its context.

### Dense Word Embeddings
- Unlike one-hot encodings, which are sparse and high-dimensional, Word2Vec produces **dense, low-dimensional vectors** (e.g., 100–300 dimensions).
- These embeddings capture semantic relationships between words.

---

## Architectures

### [[Continuous Bag of Words (CBOW)]]
- Predicts the target word based on its surrounding context words.
- Example:
  - Input: ["The", "cat", "on", "the", "mat"]
  - Target: "sat"

### [[Skip-Gram]]
- Predicts the surrounding context words given a target word.
- Example:
  - Input: "sat"
  - Target: ["The", "cat", "on", "the", "mat"]

### Differences
- **CBOW**:
  - Faster to train.
  - Works well with smaller datasets.
- **Skip-Gram**:
  - Slower to train but better for rare words.

---

## Training Objective
Word2Vec maximizes the probability of a word given its context. The objective function is:
$$
P(w_t | context) = \frac{\exp(\mathbf{v}_{w_t} \cdot \mathbf{v}_{context})}{\sum_{i \in Vocab} \exp(\mathbf{v}_i \cdot \mathbf{v}_{context})}
$$
Where:
- $\mathbf{v}_{w_t}$: Vector for the target word.
- $\mathbf{v}_{context}$: Context vector.

To reduce computational cost, Word2Vec employs:
1. **[[Negative Sampling]]**: Simplifies the objective by approximating the full softmax.
2. **[[Hierarchical Softmax]]**: Uses a binary tree structure to compute probabilities efficiently.

---

## Properties of Word Embeddings

### Semantic Similarity
- Words with similar meanings have vectors close in space.
- Example: Vectors for "king" and "queen" are close.

### Linear Relationships
- Word2Vec captures relationships through vector arithmetic:
  - Example: **"king" - "man" + "woman" ≈ "queen"**

---

## Applications

### [[Text Similarity]]
- Compare word or document embeddings to measure semantic similarity.

### [[Text Clustering]]
- Cluster documents or words based on embeddings.

### [[Sentiment Analysis]]
- Use embeddings as features for sentiment [[Classification]].

### [[Recommendation Systems]]
- Model relationships between items or users by treating them like words.

---

## Limitations

1. **Context Independence**:
   - Word2Vec generates static embeddings, meaning a word's meaning does not change with context (e.g., "bank" in "river bank" vs. "money bank").
   - Addressed by models like [[BERT]] or [[ELMo]].

2. **Requires Large Corpora**:
   - Needs a substantial amount of text to produce high-quality embeddings.

3. **Does Not Handle OOV (Out-of-Vocabulary) Words**:
   - Cannot generate embeddings for words not in the training data.

---

## Tools and Libraries

### Gensim
- Python library for Word2Vec.
- Easy to train your own embeddings or use pre-trained ones.

### Pre-Trained Embeddings
- Google News Word2Vec (trained on Google News corpus).
- Word2Vec embeddings from large text datasets like Wikipedia.

---

## Related Topics
- [[Embeddings]]: General concept of dense vector representations.
- [[Cosine Similarity]]: Measure similarity between Word2Vec embeddings.
- [[Skip-Gram]]: One of the architectures used in Word2Vec.
- [[Natural Language Processing]]: Broader field where Word2Vec is applied.

---

## Resources
- **Research Papers**:
  - "Efficient Estimation of Word Representations in Vector Space" (Word2Vec original paper by Tomas Mikolov).
- **Books**:
  - *Speech and Language Processing* by Jurafsky and Martin.
- **Online Courses**:
  - Coursera: *[[Natural Language Processing]] Specialization* by DeepLearning.AI.
  - Udemy: *Word Embeddings and Beyond*.
- **Libraries**:
  - Gensim Documentation for Word2Vec.
  - TensorFlow or PyTorch for custom implementations.

---

## Tags
#word2vec #embeddings #machinelearning #NLP #representationlearning