## Overview
**Information Retrieval (IR)** is the process of finding relevant information from a large corpus of unstructured or semi-structured data in response to a query. It is widely used in search engines, recommendation systems, and [[Question Answering]] systems. IR techniques include traditional methods like [[Sparse Retrieval]] (e.g., [[TF-IDF]] and [[BM25]]) and modern methods like [[Dense Retrieval]] using [[Embeddings]] from models like [[BERT]] or [[SBERT]].

---

## Key Concepts

### **1. Retrieval Models**
- **Sparse Retrieval**:
  - Relies on sparse vector representations with explicit term matching.
  - Examples: [[TF-IDF]], [[BM25]], and Boolean retrieval.
- **Dense Retrieval**:
  - Uses dense vector embeddings to capture semantic similarity between queries and documents.
  - Examples: [[Dense Passage Retrieval (DPR)]], [[Retrieval Augmented Generation (RAG)]].

### **2. Query and Document Representation**
- Queries and documents are represented as vectors for matching.
- Representations can be:
  - Term-based: Explicit term features in sparse retrieval.
  - Embedding-based: Dense vectors from neural networks in dense retrieval.

### **3. Scoring Functions**
- **Similarity Metrics**:
  - Compute relevance between queries and documents.
  - Examples: [[Cosine Similarity]], [[Dot Product]].
- **Ranking Functions**:
  - Rank documents based on relevance scores.
  - Examples: [[BM25]], learned-to-rank models.

---

## Applications

1. **Search Engines**:
   - Powering web search platforms like Google and Bing.
2. **Question Answering**:
   - Retrieving passages or documents to answer user queries.
3. **Recommendation Systems**:
   - Suggesting relevant items based on user queries or preferences.
4. **E-commerce**:
   - Product search and filtering.
5. **Legal and Medical Domains**:
   - Precise information retrieval for high-stakes decision-making.

---

## Techniques

1. **Indexing**:
   - Preprocesses documents to create searchable indices for faster retrieval.
   - Tools: Inverted indices, Elasticsearch, Lucene.
2. **Retrieval**:
   - Fetches candidate documents using sparse or dense methods.
3. **Ranking**:
   - Sorts candidates by relevance using scoring functions or models.
4. **Evaluation**:
   - Measures performance with metrics like [[Precision]], [[Recall]], [[F1-Score]], and [[Mean Average Precision (MAP)]].

---

## Popular Models

1. **Sparse Models**:
   - [[TF-IDF]]: Ranks documents based on term frequency and inverse document frequency.
   - [[BM25]]: Enhances TF-IDF with term saturation and document length normalization.
2. **Dense Models**:
   - [[BERT]]: Generates contextual embeddings for queries and documents.
   - [[SBERT]]: Sentence-level embeddings optimized for semantic similarity.
   - [[DPR]]: Combines dense embedding retrieval with passage readers.

---

## Tools and Libraries

1. **Elasticsearch**:
   - Industry-standard search engine for sparse retrieval.
2. **Hugging Face Transformers**:
   - Provides dense retrieval models like BERT and SBERT.
3. **FAISS**:
   - Efficient library for nearest neighbor search in dense retrieval.
4. **Anserini**:
   - Toolkit for sparse IR research based on Lucene.

---

## Challenges

1. **Scalability**:
   - Handling large-scale corpora with billions of documents.
2. **Ambiguous Queries**:
   - Determining user intent when queries are vague or underspecified.
3. **Semantic Understanding**:
   - Sparse models struggle with semantic relationships, while dense models require significant resources.
4. **Domain-Specific Retrieval**:
   - Adapting general-purpose models to specialized domains like healthcare or law.

---

## Related Topics

- [[Sparse Retrieval]]: Traditional IR methods relying on explicit term matching.
- [[Dense Retrieval]]: Modern methods using dense embeddings for semantic matching.
- [[BM25]]: A popular ranking function in sparse retrieval.
- [[Dense Passage Retrieval (DPR)]]: Combines dense embeddings with passage readers.
- [[Retrieval Augmented Generation (RAG)]]: Merges retrieval and generative models.

---

## Aliases
- Information Retrieval
- IR
- Search Retrieval

---

## Tags
#informationretrieval #IR #machinelearning #NLP #retrieval #searchengines

---

## Links to Explore
- [[Sparse Retrieval]]: Learn about traditional term-based retrieval methods.
- [[Dense Retrieval]]: Explore how dense embeddings revolutionize IR.
- [[BM25]]: Understand the ranking function behind many IR systems.
- [[FAISS]]: Discover efficient dense vector search.
- [[Elasticsearch]]: Implement IR systems with this powerful tool.