# 🧠 NLP Emotion Classification

**Comparing FCNN, Bi-LSTM, and fine-tuned BERT on 6-class emotion classification.**

---

## 📊 Overview

This project builds and compares three deep learning approaches for emotion classification from text:

- **FCNN** — baseline feedforward network with an embedding layer
- **Bi-LSTM** — bidirectional sequential model capturing word order
- **BERT** — fine-tuned `bert-base-uncased` transformer

The full workflow lives in `NLP_PROJECT.ipynb`: EDA → preprocessing → model training → evaluation.

## 📊 Results

All three models were trained and evaluated on the same held-out test set.
*Detailed per-model metrics (accuracy / macro F1) will be added from the evaluation cells in `NLP_PROJECT.ipynb`.*

| Model | Approach |
|---|---|
| FCNN | Baseline with embedding layer |
| Bi-LSTM | Sequential model (bidirectional) |
| BERT | Fine-tuned `bert-base-uncased` transformer |

## 🔧 Tech Stack

TensorFlow/Keras · HuggingFace Transformers (`bert-base-uncased`) · scikit-learn · Pandas · Google Colab

## 📁 Repository

- `NLP_PROJECT.ipynb` — full analysis: EDA → preprocessing → model training → evaluation

---
📅 **Last Updated:** October 2025
