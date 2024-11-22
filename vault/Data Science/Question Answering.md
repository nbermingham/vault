## Overview
**Question Answering (QA)** is a task in [[Natural Language Processing (NLP)]] that involves building systems capable of automatically answering questions posed in natural language. QA models can either extract answers from a given context (extractive QA) or generate answers without needing explicit context (generative QA).

Modern QA systems leverage pre-trained [[Transformer]] models like [[BERT]], [[RoBERTa]], and [[GPT]] to achieve state-of-the-art performance in a variety of tasks, including reading comprehension, open-domain QA, and knowledge-based QA.

---

## Key Types

### **1. Extractive QA**
- Extracts the answer directly from a given passage or document.
- Example:
  - **Question**: "What is the capital of France?"
  - **Context**: "Paris is the capital of France."
  - **Answer**: "Paris"
- Models: [[BERT]], [[RoBERTa]], and [[DistilBERT]].

### **2. Generative QA**
- Generates an answer using a language model, even if the answer is not explicitly present in the context.
- Example:
  - **Question**: "What are the benefits of exercise?"
  - **Answer**: "Exercise improves physical health, mental well-being, and overall quality of life."
- Models: [[GPT-3]], [[T5]], and [[BART]].

### **3. Open-Domain QA**
- Answers questions by searching across large corpora or knowledge bases, often combining [[Information Retrieval]] and QA techniques.
- Tools: [[Retriever-Reader Models]], [[Retrieval Augmented Generation (RAG)]].

---

## Applications

1. **Search Engines**:
   - Powering direct answers to user queries (e.g., Google snippets).
2. **Virtual Assistants**:
   - QA enables systems like Siri, Alexa, and Google Assistant to answer user questions.
3. **Customer Support**:
   - Automated response systems in e-commerce and customer service platforms.
4. **Healthcare**:
   - Assisting with medical question answering based on clinical guidelines or patient records.
5. **Education**:
   - Helping students find answers to academic questions or summarizing information.

---

## Techniques

1. **Pre-Trained Models**:
   - Use models like [[BERT]] and [[RoBERTa]] fine-tuned on QA datasets like [[SQuAD]].
2. **Retriever-Reader Pipelines**:
   - Combine a retriever to fetch relevant documents with a reader to extract or generate answers.
   - Example: [[Dense Passage Retrieval (DPR)]] + [[BERT]] reader.
3. **End-to-End Generative Models**:
   - Use models like [[T5]] or [[GPT-3]] to directly generate answers.

---

## Popular Datasets

1. **[[SQuAD]] (Stanford Question Answering Dataset)**:
   - Benchmark dataset for extractive QA.
2. **Natural Questions (NQ)**:
   - Questions with answers from Google search results.
3. **TriviaQA**:
   - Open-domain QA with trivia-style questions.
4. **HotpotQA**:
   - Multihop QA requiring reasoning across multiple documents.

---

## Tools and Libraries

1. **Hugging Face Transformers**:
   - Provides pre-trained QA models like `bert-base-uncased` fine-tuned on [[SQuAD]].
2. **Haystack**:
   - Open-source framework for building QA systems with retriever-reader pipelines.
3. **AllenNLP**:
   - Tools for building and evaluating QA models.

---

## Challenges

1. **Context Dependency**:
   - Answering questions often requires understanding long-range dependencies or combining information across multiple contexts.
2. **Ambiguity**:
   - Some questions may have multiple valid answers or require clarification.
3. **Generalization**:
   - Models may struggle with unseen questions or domains.
4. **Computational Costs**:
   - QA systems, especially open-domain ones, can be resource-intensive.

---

## Related Topics

- [[SQuAD]]: Benchmark dataset for extractive QA.
- [[Transformer]]: Core architecture powering modern QA models.
- [[Information Retrieval]]: Used in open-domain QA to fetch relevant documents.
- [[Dense Passage Retrieval (DPR)]]: A retriever component for open-domain QA.
- [[Retrieval Augmented Generation (RAG)]]: Combines retrieval and generative approaches for QA.

---

## Aliases
- Question Answering
- QA
- Machine Question Answering

---

## Tags
#questionanswering #QA #NLP #transformers #machinelearning #textprocessing

---

## Links to Explore
- [[BERT]]: Learn about extractive QA using this model.
- [[SQuAD]]: Explore the benchmark dataset for QA tasks.
- [[Retrieval Augmented Generation (RAG)]]: Discover how retrieval and generation are combined in QA.
- [[Information Retrieval]]: Understand the retriever-reader paradigm in QA systems.
- [[Hugging Face]]: Use pre-trained models for QA tasks.