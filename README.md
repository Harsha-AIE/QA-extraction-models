Question Answer Extraction

This repository documents a set of structured experiments focused on neural question answer extraction. The project explores how different architectural and representation choices influence the model’s ability to extract accurate answer spans from a given context.

The work is organized as a progressive study, starting from a transformer model built from scratch and gradually incorporating more advanced techniques such as pretrained contextual embeddings and attention mechanisms.

Purpose of the Repository

The primary goal of this repository is to understand and compare multiple approaches to question answer extraction by implementing them step by step and analyzing their behavior. Instead of presenting a single final model, the repository emphasizes learning through experimentation and architectural comparison.

Implemented Approaches

Baseline Transformer Model
A custom transformer-based architecture trained without pretrained embeddings. This model serves as a reference point to understand the limitations of learning representations solely from task-specific data.

Transformer with BERT Embeddings
A transformer architecture enhanced with BERT-based contextual embeddings. This approach improves semantic representation of both questions and contexts, leading to better alignment during answer extraction.

Transformer with Bahdanau Attention
An additive (Bahdanau) attention mechanism applied over encoder outputs to strengthen focus on answer-relevant tokens. This method aims to improve span localization and interpretability.

Repository Organization

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


Evaluation Strategy

Model performance is evaluated using standard question answering metrics such as Exact Match (EM) and F1 score. Training dynamics and qualitative observations are recorded to better understand convergence behavior and error patterns.

Each model directory contains an accompanying notes file that documents experimental insights, limitations, and comparative observations.

Future Extensions

Planned extensions include cross-attention mechanisms between question and context, span-based pointer networks, ablation studies on attention variants, and visualization of attention weights for interpretability.



Experiments on neural question answer extraction using transformer architectures, pretrained BERT embeddings, and attention mechanisms, with a focus on progressive model development and comparative analysis.
