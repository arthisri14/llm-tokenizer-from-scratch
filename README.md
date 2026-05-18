#  LLM Tokenizer Built From Scratch

A custom tokenizer implementation built entirely from scratch to deeply understand how modern Large Language Models (LLMs) process and tokenize text internally.

This project explores the core ideas behind tokenization systems used in GPT-style models, including Unicode handling, UTF-8 byte encoding, vocabulary construction, pair statistics, and Byte Pair Encoding (BPE).

---

#  Overview

Tokenization is one of the most fundamental components of any LLM pipeline.

Before text is fed into a transformer model, it must first be converted into smaller numerical units called **tokens**.

This project demonstrates:

* How raw text becomes bytes
* How tokens are formed
* How BPE merges frequent token pairs
* How vocabularies are built efficiently
* Why compression matters in NLP systems

The implementation focuses on learning the internal mechanics of tokenizers instead of relying on existing libraries.

---

#  Concepts Implemented

## 1. Unicode & UTF-8 Encoding

Understanding how text is converted into byte representations before tokenization.

Example:

```python
text.encode("utf-8")
```

---

## 2. Vocabulary Initialization

Creating an initial vocabulary from raw byte values.

---

## 3. Pair Frequency Statistics

Finding the most frequently occurring adjacent token pairs.

Example:

```python
def get_stats(ids):
```

This step is essential for identifying optimal merge candidates.

---

## 4. Byte Pair Encoding (BPE)

Implementing iterative token merges to compress text efficiently.

BPE helps:

* Reduce vocabulary size
* Improve compression
* Learn reusable subword units

---

## 5. Token Compression

Analyzing token count reduction and compression efficiency after merges.

---

#  Features

* Custom tokenizer implementation
* Manual BPE merge algorithm
* UTF-8 byte-level tokenization
* Vocabulary construction
* Pair frequency analysis
* Compression ratio calculation
* Educational walkthrough of tokenizer internals

---

#  Tech Stack

* Python
* Jupyter Notebook
* NLP Fundamentals
* UTF-8 Encoding
* Byte Pair Encoding (BPE)

---

#  Project Structure

```text
llm-tokenizer-from-scratch/
│
├── demo.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

#  Getting Started

## Clone the Repository

```bash
git clone https://github.com/arthisri14/llm-tokenizer-from-scratch.git
```

---

## Navigate to the Project

```bash
cd llm-tokenizer-from-scratch
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Notebook

```bash
jupyter notebook
```

Open:

```text
demo.ipynb
```

---

# 📊 Sample Workflow

1. Input raw text
2. Convert text → UTF-8 bytes
3. Generate token IDs
4. Compute pair statistics
5. Merge frequent pairs
6. Build optimized vocabulary
7. Analyze compression

---

#  Learning Outcomes

This project helped me understand:

* Internal working of GPT tokenizers
* Byte-level tokenization
* Compression-based NLP techniques
* Vocabulary optimization
* Subword tokenization
* Foundations of modern LLM preprocessing

---

#  Future Improvements

* Add tokenizer decoding support
* Save/load vocabulary files
* Regex-based pre-tokenization
* Compare results with GPT-2 tokenizer
* Train tokenizer on larger datasets
* Build a mini GPT-compatible tokenizer pipeline

---

#  References

* OpenAI GPT Tokenization Concepts
* Byte Pair Encoding (BPE)
* UTF-8 Encoding Standards
* NLP Tokenization Techniques

---

#  Motivation

Most developers use tokenizers through libraries without understanding how they work internally.

This project was built to gain a deeper understanding of the preprocessing pipeline behind modern LLMs and transformers.

---

#  License

This project is open-source and available under the MIT License.
