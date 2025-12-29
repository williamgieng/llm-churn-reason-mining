# LLM Churn Reason Mining (Synthetic Case Study)

This repository demonstrates an end-to-end approach to extracting, categorizing, and summarizing customer churn reasons from free-text notes using modern NLP techniques.

All data in this project is **synthetic** and intentionally designed for demonstration and portfolio use.

---

## Problem Framing

Customer churn feedback often exists as unstructured text:
- cancellation notes
- call center summaries
- support tickets
- survey responses

While rich in signal, this data is difficult to analyze at scale without:
- consistent labeling
- explainable categorization
- executive-ready summaries

This project shows how a modern NLP pipeline can address those challenges.

---

## What This Project Demonstrates

- Synthetic generation of churn-style text data
- Weak supervision to bootstrap labels without manual annotation
- Transformer-based text classification (DistilBERT)
- Prompt-engineered LLM summaries for human-readable insights
- Executive-style visualization of churn drivers and evidence

The focus is on **system design, tradeoffs, and interpretability**, not leaderboard metrics.

---

## High-Level Architecture

1. **Synthetic Data Generation**
   - Realistic churn language patterns
   - Multiple churn drivers with overlapping themes

2. **Weak Supervision**
   - Rule-based labeling to create an initial training signal
   - No human-labeled data required

3. **Transformer Fine-Tuning**
   - DistilBERT sequence classifier
   - Lightweight training for rapid iteration

4. **Prompt-Engineered Summarization**
   - LLM prompts extract:
     - dominant themes
     - representative phrases
     - example customer language

5. **Executive-Ready Visualization**
   - Driver mix distribution
   - Supporting evidence per category
   - Designed for readability and discussion

---

## Interpreting the Metrics

Evaluation metrics may appear near-perfect in this notebook.

This is **expected** because:
- the dataset is synthetic
- class boundaries are intentionally separable
- labels are derived from high-precision weak supervision rules
- training and validation data come from the same generation process

The purpose of evaluation here is to validate:
- pipeline correctness
- modeling viability
- end-to-end system wiring

It is **not** intended to represent real-world churn prediction performance.

---

## Why Synthetic Data

Real churn data is often:
- proprietary
- sensitive
- legally restricted

Synthetic data allows:
- safe sharing
- reproducibility
- architectural demonstration
- portfolio-ready examples

The techniques shown here transfer directly to real datasets.

---

## Repository Contents

- `churn-reasons-llm-synthetic-case-study.ipynb`  
  End-to-end notebook with data generation, modeling, prompting, and visualization.

- `.gitignore`  
  Standard exclusions for clean version control.

---

## How This Would Extend to Production

In a real deployment, this approach could be extended with:
- human-in-the-loop review
- multi-label classification
- continual retraining
- experiment tracking
- drift monitoring
- integration with BI tools

---

## Disclaimer

This project uses **synthetic data only**.  
No proprietary, customer, or internal company data is included.
