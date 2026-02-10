# Question Answer Extraction

This repository documents a set of structured experiments focused on neural question answer extraction. The project explores how different architectural and representation choices influence a model’s ability to extract accurate answer spans from a given context.

The work is organized as a progressive study, starting from a transformer model built from scratch and gradually incorporating more advanced techniques such as pretrained contextual embeddings and attention mechanisms.

---

## Purpose of the Repository

The primary goal of this repository is to understand and compare multiple approaches to question answer extraction by implementing them step by step and analyzing their behavior. Instead of presenting a single final model, the repository emphasizes learning through experimentation and architectural comparison.

---

## Implemented Approaches

### Baseline Transformer Model
A custom transformer-based architecture trained without pretrained embeddings. This model serves as a reference point to understand the limitations of learning representations solely from task-specific data.

### Transformer with BERT Embeddings
A transformer architecture enhanced with BERT-based contextual embeddings. This approach improves semantic representation of both questions and contexts, leading to better alignment during answer extraction.

### Transformer with Bahdanau Attention
An additive (Bahdanau) attention mechanism applied over encoder outputs to strengthen focus on answer-relevant tokens. This method aims to improve span localization and interpretability.

---

## Repository Organization

```text
question-answer-extraction/
├── data/
│   ├── raw/
│   └── processed/
├── models/
│   ├── baseline_transformer/
│   ├── bert_embeddings/
│   └── bahdanau_attention/
├── evaluation/
│   └── metrics.py
├── experiments/
│   └── logs/
├── utils/
│   └── preprocessing.py
├── requirements.txt
└── README.md
