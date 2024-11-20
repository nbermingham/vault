## Overview
**TF-IDF (Term Frequency-Inverse Document Frequency)** is a statistical method used in [[Natural Language Processing]] (NLP) to evaluate the importance of a word in a document relative to a collection of documents (corpus). It improves upon the [[Count Vectorizer]] by not just counting word occurrences but also weighting words based on how unique or significant they are in the entire corpus.

---

## Key Concepts

### Term Frequency (TF)
- Measures how often a word appears in a document.
$$
TF(t, d) = \frac{\text{Number of times term } t \text{ appears in document } d}{\text{Total number of terms in document } d}
$$

### Inverse Document Frequency (IDF)
- Measures how rare or unique a word is across the corpus.
$$
IDF(t, D) = \log\left(\frac{N}{1 + \text{Number of documents containing term } t}\right)
$$
Where:
- $N$: Total number of documents in the corpus.
- The $+1$ prevents division by zero.

### TF-IDF Score
- Combines TF and IDF to assign a weight to each word in a document:
$$
TF\text{-}IDF(t, d, D) = TF(t, d) \cdot IDF(t, D)
$$
- High TF-IDF indicates that the term is frequent in a specific document but rare across the corpus.

---

## Advantages

1. **Captures Importance**:
   - Highlights words that are important for a specific document but not common across the corpus.
2. **Efficient**:
   - Produces sparse representations, making it computationally efficient.
3. **Customizable**:
   - Can be adjusted by modifying TF or IDF formulas for specific applications.

---

## Disadvantages

1. **Ignores Context**:
   - Like the [[Count Vectorizer]], it does not capture word order or semantic relationships.
2. **Sensitive to Large Corpora**:
   - In very large corpora, common but still relevant terms may be overly down-weighted.
3. **Sparse Representation**:
   - High-dimensional sparse vectors may still be inefficient for certain downstream tasks.

---

## Applications

1. **Text Classification**:
   - Frequently used for tasks like spam detection, sentiment analysis, and topic classification.
2. **Information Retrieval**:
   - Ranks documents based on relevance to a query by comparing their TF-IDF vectors.
3. **Text Similarity**:
   - Measures similarity between documents by comparing their TF-IDF representations.

---

## Example

### Corpus
1. Document 1: "The cat sat on the mat."
2. Document 2: "The dog lay on the mat."

### Vocabulary
[cat, dog, lay, mat, on, sat, the]

### TF-IDF Scores
- Term: "cat"
  - $TF(cat, \text{Doc1}) = \frac{1}{6}$
  - $IDF(cat, \text{Corpus}) = \log\left(\frac{2}{1}\right) = 0.693$
  - $TF\text{-}IDF(cat, \text{Doc1}) = \frac{1}{6} \cdot 0.693 = 0.1155$
- Repeat for all terms across documents.

---

## Tools and Libraries

1. **[[Scikit-learn]]**:
   - `TfidfVectorizer`: Built-in tool for TF-IDF vectorization.
2. **[[NLTK]]**:
   - Provides utilities for tokenization and preprocessing before applying TF-IDF.
3. **[[SpaCy]]**:
   - Integrates well with TF-IDF for text processing pipelines.

---

## Comparison with Count Vectorizer

| Feature             | Count Vectorizer              | TF-IDF                                |
| ------------------- | ----------------------------- | ------------------------------------- |
| **Frequency Focus** | Pure frequency count          | Weighs terms by rarity and importance |
| **Word Weighting**  | Equal weighting for all terms | Weighted by importance across corpus  |
| **Use Cases**       | Suitable for small datasets   | Better for diverse, larger datasets   |

---

## Related Topics
- [[Count Vectorizer]]: A simpler method of text vectorization.
- [[Word Embeddings]]: Dense vector representations that capture semantic relationships.
- [[Text Similarity]]: TF-IDF is often used to compute document similarity.

---

## Resources

### Tutorials
- [[Scikit-learn]] documentation on `TfidfVectorizer`.
- NLP tutorials on text preprocessing and vectorization.

### Books
- *Speech and Language Processing* by Jurafsky and Martin.
- *Deep Learning for NLP* by Palash Goyal et al.

---

## Tags
#TF-IDF #NLP #machinelearning #textprocessing #informationretrieval