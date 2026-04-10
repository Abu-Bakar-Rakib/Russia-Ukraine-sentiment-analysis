# Sentiment Analysis of YouTube Comments on the Russia–Ukraine Conflict

[![IEEE](https://img.shields.io/badge/Published-IEEE%20ICECTE%202026-blue?logo=ieee)](https://ieeexplore.ieee.org/abstract/document/11429242)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green?logo=python)](https://www.python.org/)
[![BERT](https://img.shields.io/badge/Model-BERT%20%7C%20RoBERTa-orange?logo=huggingface)](https://huggingface.co/)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)
[![Google Colab](https://img.shields.io/badge/Training-Google%20Colab-yellow?logo=googlecolab)](https://colab.research.google.com/)

> **A Comparative Study of Machine Learning and Transformer-Based Approaches**  
> *Published at IEEE International Conference on Electrical, Computer & Telecommunication Engineering (ICECTE 2026)*  
> Rajshahi, Bangladesh — January 29–31, 2026

---

## 📄 Abstract

The ongoing Russia–Ukraine crisis has generated unparalleled discourse on social media platforms. This repository presents a comprehensive study analyzing **10,000 YouTube comments** collected from major international news channels (CNN, BBC, Al Jazeera, Sky News, and Euronews), classifying sentiments as **Pro-Ukrainian**, **Neutral**, or **Pro-Russian**.

Our experimental results show that **BERT significantly outperformed** all other approaches with:
- **Accuracy:** 86%
- **Precision:** 85%
- **Recall:** 79%
- **F1-Score:** 81%
- **ROC-AUC:** 0.94

Our findings demonstrate that transformer-based architectures capture complex linguistic patterns and contextual nuances present in geopolitical discourse far more effectively than classical or recurrent models.

---

## 👨‍💻 Authors

| Name | Affiliation |
|------|-------------|
| Abu Bakar Rakib | Dept. of CSE, IUBAT, Dhaka, Bangladesh |
| Obaidul Haque | Dept. of CSE, IUBAT, Dhaka, Bangladesh   |
| Snaholata Mondal | Dept. of CSE, IUBAT, Dhaka, Bangladesh |

📧 Contact: `rakibcdp@gmail.com`

---

## 📊 Dataset

| Class | Train (80%) | Test (20%) | Total |
|-------|------------|-----------|-------|
| Pro-Russian | 2,742 | 685 | 3,425 |
| Pro-Ukrainian | 4,214 | 1,053 | 5,265 |
| Neutral | 1,045 | 261 | 1,305 |
| **Total** | **8,001** | **1,999** | **10,000** |

### Data Collection
- **Sources:** CNN, BBC, Al Jazeera, Sky News, Euronews (YouTube)
- **Period:** March 2022 – June 2025
- **Annotation:** Manual annotation by co-authors; Inter-annotator Kappa score of **0.82**
- **Labels:** Pro-Russian, Pro-Ukrainian, Neutral

### Preprocessing Steps
1. Removed null values and filled missing entries where applicable
2. Stripped HTML tags captured during scraping
3. Normalized and cleaned text
4. 80/20 train-test split

---

## 🧠 Models Compared

| Model | Type | Key Config |
|-------|------|-----------|
| **BERT** | Transformer | `bert-base-uncased`, AdamW, lr=2e-5, 5 epochs |
| **RoBERTa** | Transformer | `roberta-base`, AdamW, lr=2e-5, 15 epochs |
| **SVM** | Classical ML | TF-IDF, vocab=5000, bi-gram, linear kernel |
| **LSTM** | Recurrent DL | 128-dim embeddings, dropout=0.3, lr=2e-4, 30 epochs |
| **RNN** | Recurrent DL | 128-dim embeddings, dropout=0.3, lr=2e-4, 60 epochs |

---

## 📈 Results

### Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score | ROC AUC |
|-------|----------|-----------|--------|----------|---------|
| **BERT** | **0.86** | **0.85** | **0.79** | **0.81** | **0.94** |
| RoBERTa | 0.80 | 0.77 | 0.76 | 0.76 | 0.89 |
| SVM | 0.78 | 0.80 | 0.67 | 0.70 | 0.89 |
| LSTM | 0.78 | 0.74 | 0.73 | 0.73 | 0.84 |
| RNN | 0.53 | 0.68 | 0.34 | 0.26 | 0.52 |

### BERT Classification Report (Per Class)

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| Pro-Russian | 0.88 | 0.91 | 0.89 | 685 |
| Pro-Ukrainian | 0.86 | 0.89 | 0.87 | 1053 |
| Neutral | 0.80 | 0.58 | 0.67 | 261 |
| **Weighted Avg** | **0.86** | **0.86** | **0.85** | **1999** |

---

## 📚 Citation

If you use this findings in your research, please cite our paper:

### BibTeX

```bibtex
@inproceedings{rakib2026sentiment,
  title     = {Sentiment Analysis of YouTube Comments on the Russia Ukraine Conflict: 
               A Comparative Study of Machine Learning and Transformer-Based Approaches},
  author    = {Rakib, Abu Bakar and Alum, Md. Mahbub and Haque, Obaidul and Mondal, Snaholata},
  booktitle = {2026 IEEE International Conference on Electrical, Computer \& 
               Telecommunication Engineering (ICECTE)},
  pages     = {1--6},
  year      = {2026},
  month     = {January},
  address   = {Rajshahi, Bangladesh},
  publisher = {IEEE},
  doi       = {10.1109/ICECTE.2026.11429242},
  url       = {https://ieeexplore.ieee.org/abstract/document/11429242}
}
```
## ⭐ Star This Repo

If you find this work useful, please consider giving it a ⭐ — it helps others discover the research!

---

<p align="center">
  <i>Published at IEEE ICECTE 2026 · International University of Business Agriculture and Technology (IUBAT), Dhaka, Bangladesh</i>
</p>
