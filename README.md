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

All three models were trained and evaluated on the same held-out test set (2,000 samples, 6 emotion classes):
   Model | Accuracy | Macro F1 | Notes |
 |---|---|---|---|
 | FCNN | 0.82 | 0.76 | Baseline with embedding layer |
 | **Bi-LSTM** | **0.89** | **0.82** | Best overall — best trade-off under limited training budget |
 | BERT | 0.79 | 0.67 | Fine-tuned `bert-base-uncased`, constrained by training time/epochs |

**Key finding:** the Bi-LSTM outperformed fine-tuned BERT under a limited training budget — word-order modeling generalized better than a partially fine-tuned transformer on this dataset size.

Class-level highlights (Bi-LSTM): strong performance on *joy* (0.92) and *sadness* (0.95 F1); *surprise* remains the hardest class across all models (lowest support).

## 🔧 Tech Stack

TensorFlow/Keras · HuggingFace Transformers (`bert-base-uncased`) · scikit-learn · Pandas · Google Colab

## 📁 Repository

- `NLP_PROJECT.ipynb` — full analysis: EDA → preprocessing → model training → evaluation

---
📅 **Last Updated:** October 2025
