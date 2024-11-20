## Overview
**GloVe** (Global Vectors for Word Representation) is a word embedding model that represents words as dense vectors in a continuous vector space. Unlike [[Word2Vec]], which predicts words based on their local context, GloVe learns embeddings by factorizing a global word co-occurrence matrix, combining the strengths of statistical and predictive models.

---

## Key Concepts

### [[Co-occurrence Matrix]]
- GloVe uses a **word co-occurrence matrix**, where each entry \( X_{ij} \) represents how often word \( i \) appears in the context of word \( j \) across the entire corpus.
- Co-occurrence statistics capture global relationships between words in the corpus.

### [[Objective Function]]
- GloVe optimizes an objective function that models the logarithm of co-occurrence probabilities:
$$
J = \sum_{i,j=1}^{V} f(X_{ij}) \left( \mathbf{w}_i^\top \mathbf{w}_j + b_i + b_j - \log(X_{ij}) \right)^2
$$
Where:
- $\mathbf{w}_i$ and  $\mathbf{w}_j$: Word vectors for words \( i \) and \( j \).
- $b_i$ and $b_j$: Bias terms for words \( i \) and \( j \).
- $X_{ij}$: Co-occurrence count between words \( i \) and \( j \).
- $f(X_{ij})$: Weighting function that reduces the impact of very frequent word pairs.

### Weighting Function
- GloVe uses a weighting function to balance the importance of frequent and infrequent word pairs:
$$
f(X_{ij}) = \begin{cases} 
\left( \frac{X_{ij}}{X_{\text{max}}} \right)^\alpha & \text{if } X_{ij} < X_{\text{max}} \\
1 & \text{otherwise}
\end{cases}
$$
Where $\alpha$ is a tunable parameter (typically 0.75).

---

## Properties of GloVe Embeddings

### Semantic Relationships
- Words with similar meanings have vectors that are close in space.
- Example: "king" and "queen" will have similar vectors.

### Linear Relationships
- GloVe captures linear relationships between words, enabling vector arithmetic:
  - Example: **"king" - "man" + "woman" ≈ "queen"**

### Global Context
- Unlike [[Word2Vec]], which focuses on local context, GloVe incorporates global co-occurrence statistics, making it better at capturing long-range dependencies.

---

## Advantages
1. **Captures Global Information**: Learns embeddings based on the entire corpus.
2. **Efficient Training**: Factorization-based training is computationally efficient for large corpora.
3. **High Quality for Similarity Tasks**: Performs well in tasks like word analogy and similarity.

---

## Disadvantages
1. **Static Embeddings**: Produces the same vector for a word regardless of its context, unlike contextual models like [[BERT]] or [[ELMo]].
2. **Memory Intensive**: Requires storing and factorizing the co-occurrence matrix, which can be computationally expensive for very large corpora.
3. **Out-of-Vocabulary (OOV) Words**: Cannot handle words not present in the training data.

---

## Applications
- **Word Similarity Tasks**: Compare word meanings based on embedding distances.
- **Sentiment Analysis**: Use embeddings as features for text classification.
- **Machine Translation**: Represent words in a shared vector space across languages.
- **Question Answering**: Extract meaningful relationships between words in a corpus.

---

## Comparison with Word2Vec
| **Feature**               | **Word2Vec**                            | **GloVe**                                |
|---------------------------|-----------------------------------------|------------------------------------------|
| **Training**              | Predicts context or target words       | Factorizes co-occurrence matrix          |
| **Context**               | Local (sliding window)                 | Global (entire corpus)                   |
| **Efficiency**            | Faster for streaming data              | More efficient for batch data            |
| **Embedding Properties**  | Good for rare words                    | Better at capturing global relationships |

---

## Tools and Libraries

### Pre-Trained GloVe Embeddings
- **GloVe Pre-Trained Embeddings**:
  - Available for download from the Stanford NLP website.
  - Common corpora: Wikipedia, Gigaword, Common Crawl.

### Python Libraries
- **Gensim**:
  - Supports loading pre-trained GloVe embeddings for NLP tasks.
- **TensorFlow and PyTorch**:
  - Use GloVe embeddings as input layers for deep learning models.

---

## Training Process
1. Build a word co-occurrence matrix from the corpus.
2. Factorize the co-occurrence matrix to find word vectors.
3. Optimize the objective function to reduce the reconstruction error.

---

## Related Topics
- [[Embeddings]]: Dense vector representations for words, sentences, and documents.
- [[Word2Vec]]: Predictive model for word embeddings.
- [[Cosine Similarity]]: Metric to measure similarity between GloVe embeddings.
- [[BERT]]: Contextual embeddings that extend static models like GloVe.

---

## Resources
- **Research Papers**:
  - "GloVe: Global Vectors for Word Representation" (original paper by Pennington, Socher, and Manning).
- **Books**:
  - *Speech and Language Processing* by Jurafsky and Martin.
- **Courses**:
  - Coursera: *Natural Language Processing Specialization* by DeepLearning.AI.
- **Tutorials**:
  - Stanford NLP group's official GloVe documentation.
  - Gensim's guide for using pre-trained embeddings.

---

## Tags
#glove #embeddings #machinelearning #NLP #representationlearning