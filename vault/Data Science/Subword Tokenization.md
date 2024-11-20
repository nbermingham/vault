## Overview
**Subword Tokenization** is a modern tokenization technique used in [[Natural Language Processing (NLP)]] that splits words into smaller meaningful units, or subwords, to handle rare and unknown words effectively. This method bridges the gap between [[Word Tokenization]] and [[Character Tokenization]], providing a balance between vocabulary size and sequence length.

Subword tokenization is commonly used in state-of-the-art models like [[BERT]], [[GPT]], and [[T5]], where it plays a critical role in efficiently representing textual data.

---

## Key Concepts

### **1. Purpose**
- **Rare Words**:
  - Instead of treating rare or unknown words as out-of-vocabulary (OOV), subword tokenization breaks them into smaller known units.
  - Example: "unbelievably" → ["un", "##believable", "##ly"]
- **Vocabulary Efficiency**:
  - Reduces the overall vocabulary size by reusing common subword units across words.

---

### **2. Techniques**

#### **Byte-Pair Encoding (BPE)**
- Iteratively merges the most frequent pairs of characters or subwords into new subword units.
- Widely used in [[GPT-2]] and [[RoBERTa]].
- Example:
  - Input: ["un", "believable", "ly"]
  - Merge: ["un", "##believable", "##ly"]

#### **WordPiece**
- A probabilistic variation of BPE that chooses subwords to maximize the likelihood of sequences.
- Used in [[BERT]].
- Example:
  - "unbelievably" → ["un", "##believable", "##ly"]

#### **SentencePiece**
- Treats text as a stream of bytes, enabling language-agnostic subword tokenization.
- Used in [[T5]] and [[ALBERT]].
- Example:
  - "Tokyo2020" → ["▁Tokyo", "2020"]

---

### **3. Advantages**
1. **Handles OOV Words**:
   - Rare or unknown words are decomposed into recognizable subwords.
2. **Reduces Vocabulary Size**:
   - Smaller vocabularies improve computational efficiency and memory usage.
3. **Language-Agnostic**:
   - Techniques like SentencePiece are adaptable to non-space-separated languages (e.g., Chinese, Japanese).

---

### **4. Disadvantages**
1. **Sequence Length**:
   - Increases the number of tokens for long or complex words, leading to longer input sequences.
2. **Loss of Interpretability**:
   - Subword units may lack semantic meaning (e.g., "##ly").

---

## Applications

1. **Transformer Models**:
   - [[BERT]], [[GPT]], and [[T5]] rely on subword tokenization for efficient representation.
2. **Machine Translation**:
   - Handles morphologically rich languages with a large number of word forms.
3. **Text Summarization**:
   - Ensures consistent tokenization across training and inference.

---

## Example

### Byte-Pair Encoding (BPE)
Input: "unbelievably"
- Initial Tokens: ["u", "n", "b", "e", "l", "i", "e", "v", "a", "b", "l", "y"]
- Merge 1: ["un", "b", "e", "l", "i", "e", "v", "a", "b", "l", "y"]
- Merge 2: ["un", "bel", "i", "e", "v", "a", "b", "l", "y"]
- Final Tokens: ["un", "believable", "ly"]

### WordPiece
Input: "unbelievably"
- Output: ["un", "##believable", "##ly"]

---

## Tools and Libraries

1. **Python Libraries**:
   - [[Hugging Face]]: Tokenizers for BERT, GPT, and other transformer models.
   - [[SentencePiece]]: Library for language-agnostic subword tokenization.
2. **Visualization Tools**:
   - Plot token distributions and analyze subword splits.

---

## Related Topics

- [[Tokenization]]: Subword tokenization is a specific approach to tokenization.
- [[BERT]]: Uses WordPiece for tokenizing input text.
- [[GPT]]: Employs Byte-Pair Encoding (BPE).
- [[T5]]: Relies on SentencePiece for language-independent tokenization.
- [[Byte-Pair Encoding (BPE)]]: A foundational subword tokenization technique.

---

## Aliases
- Subword Tokenization
- Subword Segmentation
- BPE Tokenization

---

## Tags
#subwordtokenization #NLP #textprocessing #transformer #machinelearning #preprocessing

---

## Links to Explore
- [[Tokenization]]: Learn about the broader process of breaking text into tokens.
- [[Byte-Pair Encoding (BPE)]]: Explore the most widely used subword tokenization technique.
- [[BERT]]: Understand how WordPiece tokenization works in this model.
- [[SentencePiece]]: Discover a tool for language-agnostic subword tokenization.
- [[GPT]]: Dive into models using subword techniques like BPE.