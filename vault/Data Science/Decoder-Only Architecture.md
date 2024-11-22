## Overview
**Decoder-Only Architecture** is a [[Transformer]]-based design primarily used in [[Natural Language Processing]] tasks for [[Text Generation]]. Unlike the standard encoder-decoder structure, the decoder-only architecture eliminates the encoder and relies solely on an autoregressive decoder. This design predicts the next token in a sequence by considering only the tokens that precede it, making it ideal for tasks such as [[Language Modeling]], [[Machine Translation]], and conversational AI.

Prominent models like [[GPT]] and [[GPT-3]] use decoder-only architectures to generate coherent and contextually relevant text.

---

## Key Concepts

### **1. Autoregressive Decoding**
- Decoder-only models generate tokens sequentially:
  - The model predicts one token at a time, conditioning on all previous tokens in the sequence.
- Uses causal masking to prevent the model from attending to future tokens during training.

### **2. Self-Attention**
- Employs [[Self-Attention]] mechanisms to process input sequences.
- Causal masking ensures that predictions depend only on earlier tokens.

### **3. Pre-Training Objectives**
- Typically trained using [[Causal Language Modeling]]:
  $$
  L = - \sum_{i=1}^n \log P(x_i \mid x_{<i})
  $$
  Where:
  - $x_i$: Current token.
  - $x_{<i}$: All preceding tokens.

### **4. Fine-Tuning and Prompting**
- Models can be fine-tuned on task-specific datasets or adapted using [[Prompt Engineering]] for few-shot or zero-shot learning.

---

## Applications

1. **Language Modeling**:
   - Predicts the probability of the next token in a sequence.
2. **Text Generation**:
   - Generates coherent text for applications like chatbots, story writing, or code generation.
3. **Summarization**:
   - Generates summaries by conditioning on long input contexts.
4. **Conversational AI**:
   - Powers dialogue systems for virtual assistants.
5. **Machine Translation**:
   - Translates text by autoregressively generating tokens in the target language.

---

## Advantages

1. **Simplicity**:
   - Streamlined architecture compared to encoder-decoder models.
2. **Scalability**:
   - Easy to scale for larger datasets and longer sequences.
3. **Generalization**:
   - Adapts to a wide range of tasks using pre-trained weights and minimal fine-tuning.
4. **Efficiency**:
   - Reduces computational overhead by removing the encoder.

---

## Disadvantages

1. **Limited Bidirectional Context**:
   - Cannot fully leverage bidirectional context like [[Encoder-Only Architecture]] or [[Encoder-Decoder Architecture]].
2. **Training Complexity**:
   - Requires significant computational resources for pre-training.
3. **Long-Context Dependencies**:
   - Struggles with very long input sequences due to memory limitations.

---

## Prominent Models

1. **[[GPT]] (Generative Pre-trained Transformer)**:
   - The first widely adopted decoder-only architecture.
2. **[[GPT-3]]**:
   - Scaled-up version with 175 billion parameters.
3. **[[Codex]]**:
   - Specialized for code generation tasks.
4. **[[LLama]]**:
   - Optimized for efficiency and smaller-scale hardware deployment.

---

## Tools and Libraries

1. **Hugging Face Transformers**:
   - Provides pre-trained decoder-only models like GPT and GPT-2.
2. **PyTorch**:
   - Framework for implementing custom decoder-only architectures.
3. **TensorFlow**:
   - Supports training and deploying decoder-only models.

---

## Related Topics

- [[Transformer]]: The foundational architecture for decoder-only models.
- [[Causal Language Modeling]]: The training objective for decoder-only models.
- [[Self-Attention]]: Mechanism used for context-aware token generation.
- [[Encoder-Decoder Architecture]]: Compare with this two-part structure.
- [[Prompt Engineering]]: Adapt decoder-only models for specific tasks.

---

## Aliases
- Decoder-Only Architecture
- Autoregressive Transformer
- Single-Decoder Transformer

---

## Tags
#transformer #decoderonly #textgeneration #NLP #machinelearning #deeplearning

---

## Links to Explore
- [[Transformer]]: Learn about the core architecture underlying decoder-only models.
- [[GPT]]: Explore the most prominent decoder-only model.
- [[Causal Language Modeling]]: Understand the pre-training objective for these models.
- [[Self-Attention]]: Dive into the mechanism that powers context-aware generation.
- [[Prompt Engineering]]: Discover how to adapt decoder-only models for various tasks.