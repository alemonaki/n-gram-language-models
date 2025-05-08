# N-gram Language Models & Context-Aware Spelling Correction

This project implements bigram and trigram language models with Laplace smoothing, trained on a tokenized subset of an NLTK corpus. It supports:

- **Vocabulary building** (min frequency threshold, OOV handling with `*UNK*`)
- **Sentence scoring** with log-probabilities, cross-entropy, and perplexity
- **Autocompletion** of partial sentences using n-gram probabilities
- **Context-aware spelling correction** via beam search and Levenshtein distance
- **Evaluation** of correction performance using Word Error Rate (WER) and Character Error Rate (CER)

---

## Features

### 🔤 Language Models
- Bigram and trigram models with Laplace smoothing
- Cross-entropy & perplexity estimation on held-out test data

### ✍️ Sentence Autocompletion
- Predicts most likely sentence continuations
- Uses greedy decoding with optional beam search

### 🧠 Spelling Corrector
- Beam search decoding combining edit distance & language model
- Corrects both real-word and non-word errors

### 🧪 Evaluation
- WER and CER metrics on artificially corrupted test data

---

## Example

**Input:** `I would like to commend the`  
**Bigram Completion:** `president for his efforts *end*`  
**Trigram Completion:** `rapporteur on his work *end*`  
