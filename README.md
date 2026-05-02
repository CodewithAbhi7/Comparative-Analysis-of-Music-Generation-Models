# Symbolic Music Generation & Benchmarking Framework

> This project is part of an ongoing **research study**. The full research paper will be added soon.

---

## Overview

This project presents an **end-to-end symbolic music generation and benchmarking framework** built using the **MIT Irish Folk Music Dataset (ABC notation)**.

It goes beyond generation by introducing a **comprehensive and standardized evaluation pipeline** to fairly compare multiple deep learning architectures across **model-level, structural, and audio-based metrics**.

## Experimental Note

> This study focuses on exploring different model architectures for music generation rather than maximizing their performance.  
> All models were trained using the same hyperparameters to ensure a fair and unbiased comparison.  
>  
> The purpose of this setup is to identify which architectures are most promising for building more complex music-generation systems in the future.  
>  
> Due to limited GPU resources and the exploratory nature of the work, the reported results may not represent the models’ optimal performance.  
>  
> With further tuning and compute, these architectures can be extended to tasks like polyphonic generation and chord prediction.

---

## Key Highlights

- End-to-end pipeline: **Data → Training → Generation → Evaluation**
- Implementation of **7 deep learning architectures**
- Unified benchmarking framework across all models
- Multi-dimensional evaluation:
  - Model-level metrics  
  - Symbolic & structural metrics  
  - Musical coherence analysis  
  - Audio similarity (DTW)  
- Research-focused design for **fair model comparison**

---

## Models Implemented

| Model        | Type |
|-------------|------|
| RNN         | Sequence Model |
| LSTM        | Advanced RNN |
| GRU         | Gated RNN |
| CNN         | Convolutional |
| Transformer | Attention-based |
| VAE         | Generative |
| GAN         | Generative |

---

## Dataset

- **MIT Irish Folk Music Dataset**
- Format: **ABC Notation (Symbolic Music)**

### Preprocessing:
- Character-level tokenization  
- Vocabulary mapping  
- Sequence batching  
- Training sample generation  

---

## Pipeline Architecture


ABC Dataset 

↓  
Preprocessing & Tokenization

↓  
Model Training  
(RNN / LSTM / GRU / CNN / Transformer / VAE / GAN)  

↓  
Music Generation (ABC → Audio)  

↓  
Evaluation Framework (Multi-level Metrics)

## Evaluation Framework

This project introduces a **comprehensive benchmarking system**:

### Model-Level Metrics
- Loss  
- Note Accuracy  
- Perplexity  
- GAN-specific:
  - Transition Accuracy  
  - Distribution Loss & Similarity  

---

### Symbolic & Structural Metrics
- Jaccard Similarity (Note Overlap)  
- Bigram / Trigram Overlap  
- BLEU Score  
- Sequence Similarity  
- Melodic Contour Similarity  
- Pitch-Class Histogram Divergence  

---

### Musical Flow Analysis
- Musical Coherence (Original vs Generated)

---

### Audio-Level Evaluation
- MFCC-based similarity  
- Dynamic Time Warping (DTW)

---

## Results & Benchmarking

### Model Performance (Model-Level Metrics)
<img width="649" height="126" alt="Screenshot 2026-05-02 162525" src="https://github.com/user-attachments/assets/c7c8c34d-fa7e-41af-bd37-9ef5421b4151" />

---

### Symbolic & Structural Evaluation

<img width="547" height="172" alt="Screenshot 2026-05-02 162542" src="https://github.com/user-attachments/assets/2d0a076d-8bf9-4a96-ae83-eed7fce2543a" />


---

## Research Insights

### Key Findings

- **LSTM and CNN emerged as the most reliable models**
  - LSTM → Best balance of structure, coherence, and accuracy  
  - CNN → Extremely high accuracy but weak musical structure  

- **RNN performs strongly in sequence modeling**
  - High similarity and coherent melody generation  

- **GRU and Transformer show inconsistent results**
  - Require further tuning or larger datasets  

- **GAN and VAE struggle with structure**
  - Capture distribution but fail in sequence coherence  

---

### Core Insight

> High predictive accuracy **does not guarantee musical quality**

Models like CNN and GRU achieve high accuracy but fail to preserve:
- melodic flow  
- structure  
- long-term coherence  

---

###  Best Overall Model

**LSTM** achieves the best trade-off across:
- accuracy  
- structural similarity  
- musical coherence  

---

## Research Paper (Coming Soon)

This repository supports a research study titled:

**"Comparative Analysis of Deep Learning Models for Symbolic Music Generation"**

The paper will include:
- Methodology  
- Detailed experiments  
- Full evaluation results  
- Comparative analysis  
- Future research directions  

---

## Final Note

> **Music generation is not just about accuracy — it's about structure, coherence, and musicality.**
