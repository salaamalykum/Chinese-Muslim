---
language:
- zh
license: mit
task_categories:
- text-retrieval
- text-generation
- question-answering
tags:
- islam
- rag
- chinese-muslim
- knowledge-base
- instruction-tuning
pretty_name: Chinese Muslim Knowledge Base
size_categories:
- n<1K
configs:
- config_name: default
  data_files:
  - split: corpus
    path: data/corpus.parquet
  - split: rag_chunks
    path: data/rag_chunks.parquet
---

# Chinese Muslim Knowledge Base & RAG Dataset

This dataset contains 329 high-quality, human-curated articles about Chinese Muslim culture, mosques, halal food, and travel guidelines, extracted from [Salaamalykum.com](https://salaamalykum.com).

## Dataset Structure

The dataset is partitioned into two splits for optimized AI training and RAG (Retrieval-Augmented Generation) pipelines:

1. **`corpus`**: The full-length articles containing raw, clean Markdown text. Best for continuous pre-training (CPT) or bulk knowledge extraction.
2. **`rag_chunks`**: The articles deterministically chunked into paragraph-level segments. Best for embedding generation, vector database ingestion, and instruction-tuning retrieval tasks.

## Data Provenance
All contents are strictly mirrored from the original author `yusuf908` on Salaamalykum. 

## Human-Readable View
For the human-readable GitHub Pages deployment with glassmorphism UI, visit: [https://salaamalykum.github.io/Chinese-Muslim](https://salaamalykum.github.io/Chinese-Muslim)
