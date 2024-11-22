## Overview
**Semantic Similarity** is a task in [[Natural Language Processing]] that measures how similar two pieces of text are in terms of meaning, regardless of their actual wording. It is widely used in tasks like [[Text Classification]], [[Question Answering]], [[Information Retrieval]], and text clustering.

Semantic similarity is typically computed using [[Embeddings]] (e.g., [[Word2Vec]], [[GloVe]], or [[BERT Embeddings]]) and distance metrics like [[Cosine Similarity]] or [[Euclidean Distance]].

---

## Key Concepts

### **1. Definition**
Semantic similarity quantifies the degree to which two texts share the same meaning. Unlike string matching, which focuses on surface-level similarity, semantic similarity captures deeper relationships in the context of language.

### **2. Common Approaches**
1. **Embedding-Based Similarity**:
   - Represent sentences or words as numerical vectors using models like [[SBERT]] or [[GloVe]].
   - Compute similarity using metrics like [[Cosine Similarity]].
   - Example: "The cat is on the mat" vs. "A cat sits on a mat."
2. **Traditional Methods**:
   - Use lexical databases like WordNet to compute similarity based on word relationships.
3. **Neural Models**:
   - Fine-tune [[Transformer]]-based models like [[BERT]] to learn task-specific similarities.

---

## Applications

1. **Information Retrieval**:
   - Match user queries with relevant documents or web pages.
2. **Plagiarism Detection**:
   - Identify rewritten or paraphrased text in documents.
3. **Paraphrase Detection**:
   - Determine whether two sentences express the same idea.
4. **Question Answering**:
   - Match user questions with the most relevant answers from a database.
5. **Recommendation Systems**:
   - Find semantically similar items, such as movies, books, or products.

---

## Tools and Libraries

1. **Hugging Face Transformers**:
   - Pretrained models like [[SBERT]] and [[DistilBERT]] for semantic similarity.
2. **Sentence Transformers**:
   - Python library specifically designed for tasks like semantic similarity.
3. **SpaCy**:
   - Built-in similarity methods using word vectors or embeddings.
4. **Scikit-learn**:
   - Compute similarity using vectorized text and distance metrics.

---

## Common Metrics

1. **Cosine Similarity**:
   - Measures the cosine of the angle between two vectors.
   - Commonly used due to its interpretability and efficiency.
2. **Euclidean Distance**:
   - Measures the straight-line distance between two vectors.
3. **Manhattan Distance**:
   - Measures the sum of absolute differences between vector components.

---

## Example Workflow

1. **Preprocess Text**:
   - Tokenize, clean, and convert text into embeddings using models like [[SBERT]] or [[BERT]].
2. **Compute Similarity**:
   - Use metrics like [[Cosine Similarity]] or Euclidean distance to quantify similarity.
3. **Evaluate**:
   - Compare similarity scores with ground truth to validate the approach.

---

## Related Topics

- [[Cosine Similarity]]: A widely used metric for measuring semantic similarity.
- [[Embeddings]]: Numerical vector representations of text used to compute similarity.
- [[SBERT]]: Sentence-BERT, a specialized model for sentence-level semantic similarity.
- [[Word2Vec]]: A classic embedding model for word-level similarity.
- [[Information Retrieval]]: A common use case for semantic similarity in search engines.

---

## Aliases
- Semantic Similarity
- Sentence Similarity
- Text Similarity

---

## Tags
#semanticsimilarity #NLP #machinelearning #textprocessing #embeddings #similaritymetrics

---

## Links to Explore
- [[SBERT]]: Learn about this model specialized for sentence-level similarity.
- [[Cosine Similarity]]: Explore the most common metric for semantic similarity.
- [[Embeddings]]: Understand how text is transformed into numerical vectors.
- [[BERT]]: Dive into one of the most popular models for semantic similarity tasks.
- [[Information Retrieval]]: Discover how semantic similarity powers search engines.