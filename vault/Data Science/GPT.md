## Overview
**GPT (Generative Pre-trained Transformer)** is a language model developed by OpenAI that uses the [[Transformers]] architecture to generate human-like text. GPT is pre-trained on large text corpora and fine-tuned for specific tasks, excelling in [[Natural Language Processing]] (NLP) tasks such as text generation, summarization, and translation.

---

## Key Concepts

### [[Generative Model]]
- GPT is **generative**, meaning it predicts the next token in a sequence based on the previous tokens.
- The model generates coherent and contextually relevant text by maximizing the likelihood of the sequence:
$$
P(w_1, w_2, \dots, w_n) = \prod_{i=1}^n P(w_i | w_1, w_2, \dots, w_{i-1})
$$

### [[Pre-Training]]
- Pre-trained on a large, diverse corpus of text (e.g., books, articles, and web pages).
- Task: Predict the next word (language modeling) in a sequence.

### [[Fine-Tuning]]
- Fine-tuned on task-specific datasets (e.g., sentiment analysis, summarization) to improve performance on specific applications.

### [[Unidirectional Transformer]]
- GPT is **unidirectional**, meaning it processes text from left to right.
- Only attends to past tokens during generation, making it distinct from bidirectional models like [[BERT]].

---

## Variants

### [[GPT]] (Original, 2018)
- Introduced in the paper *"Improving Language Understanding by Generative Pre-training."*
- Built on the [[Transformers]] decoder architecture.
- Demonstrated strong performance on tasks like text classification and question answering.

### [[GPT-2]] (2019)
- Improved model with larger parameters (up to 1.5 billion).
- Key advancements:
  - Better text coherence and contextual understanding.
  - Zero-shot learning capabilities for new tasks without fine-tuning.

### [[GPT-3]] (2020)
- Massive model with 175 billion parameters.
- Key features:
  - Few-shot and zero-shot learning capabilities.
  - Handles a wide range of NLP tasks with minimal task-specific data.
- Applications include chatbot development, content creation, and code generation.

### [[GPT-4]] (2024)
- Multi-modal model that can process both text and images.
- Further improvements in contextual understanding, reasoning, and task versatility.

---

## Architecture

### [[Decoder-Only Architecture]]
- GPT uses only the decoder block of the [[Transformers]] architecture.
- Components:
  - **Self-Attention Mechanism**:
    - Focuses on previous tokens to predict the next token.
  - **Masked Self-Attention**:
    - Ensures the model cannot "see" future tokens during training.
  - **Feedforward Layers**:
    - Processes intermediate outputs from the attention mechanism.

### [[Positional Encoding]]
- Adds positional information to input tokens since Transformers do not inherently capture token order.

---

## Training and Inference

### Training Objective
- GPT is trained to minimize the negative log-likelihood of the next token:
$$
\mathcal{L} = -\sum_{i=1}^N \log P(w_i | w_1, w_2, \dots, w_{i-1})
$$

### Inference
- Text generation involves sampling tokens iteratively from the output distribution.
- Techniques:
  - **[[Greedy Search]]**: Selects the token with the highest probability at each step.
  - **[[Beam Search]]**: Considers multiple sequences simultaneously to improve fluency.
  - **[[Top-k Sampling]]**: Samples tokens from the top-k most probable options.
  - **[[Temperature]]**: Adjusts the randomness of token selection.

---

## Applications

### [[Text Generation]]
- Generates coherent and contextually relevant text for creative writing, storytelling, and chatbot conversations.

### [[Text Summarization]]
- Condenses long articles, documents, or books into shorter summaries.

### [[Machine Translation]]
- Translates text between different languages.

### [[Question Answering]]
- Answers factual and conversational queries based on provided context.

### [[Programming Assistance]]
- Generates code, explains snippets, and fixes bugs.

---

## Advantages
1. **[[Few-Shot Learning]]**:
   - Requires minimal task-specific data to perform new tasks.
2. **[[Scalability]]**:
   - Performance improves with larger models and more data.
3. **Versatility**:
   - Applicable to a wide range of NLP tasks without retraining.

---

## Disadvantages
1. **Computational Cost**:
   - Requires significant computational resources for training and deployment.
2. **[[Data Bias]]**:
   - Can generate biased or inappropriate content if biases exist in the training data.
3. **[[Context Limitation]]**:
   - Limited context window; struggles with very long documents.
4. **[[Lack of Explainability]]**:
   - Predictions are not easily interpretable.

---

## Tools and Libraries

### APIs
- **OpenAI API**:
  - Provides access to GPT models (e.g., GPT-3 and GPT-4) for text generation and other tasks.
- **Hugging Face Transformers**:
  - Open-source implementations of GPT and related models.

### Libraries
- **PyTorch**:
  - Framework for building and fine-tuning GPT models.
- **TensorFlow**:
  - Alternative deep learning framework for GPT implementations.

---

## Advanced Topics

### [[Few-Shot Learning]]
- GPT excels at performing tasks with only a few examples provided in the input prompt.

### [[Zero-Shot Learning]]
- Can perform tasks it wasn’t explicitly trained on by leveraging general knowledge learned during pre-training.

### [[Multi-Modal]] GPT
- GPT-4 introduced multi-modal capabilities, enabling text and image understanding.

---

## Related Topics
- [[Transformers]]: The foundational architecture for GPT.
- [[Attention Mechanism]]: Core mechanism enabling GPT’s contextual understanding.
- [[BERT]]: Bidirectional counterpart of GPT for tasks requiring contextual embeddings.
- [[Text Generation]]: Primary application of GPT models.

---

## Resources

### Research Papers
- *Improving Language Understanding by Generative Pre-training* (GPT, 2018).
- *Language Models Are Few-Shot Learners* (GPT-3, 2020).

### Books
- *Deep Learning for Natural Language Processing* by Palash Goyal et al.
- *Speech and Language Processing* by Jurafsky and Martin.

### Courses
- Hugging Face: *Introduction to Transformers*.
- Coursera: *Natural Language Processing Specialization* by DeepLearning.AI.

---

## Tags
#GPT #NLP #transformers #textgeneration #machinelearning