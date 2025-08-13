# 🗣️ Arabic Joint Intent Classification & Slot Filling (JICSF)

**Arabic Joint Intent Classification & Slot Filling (JICSF)** is a Natural Language Understanding (NLU) project designed to perform **both intent detection and slot filling** for Arabic text in a single, unified model. The approach leverages **Pre-trained Language Models (PLMs)** to improve performance on Arabic datasets.

---

## 🧭 Overview
- **Joint Task**: Instead of handling intent classification and slot filling separately, this model learns them **simultaneously** to capture dependencies between tasks.
- **Language**: Focused on **Modern Standard Arabic (MSA)** and dialectal variations.
- **Model Base**: Utilizes **AraBERT** and other transformer-based architectures for Arabic NLP.

---

## 📦 Dataset
- **Source**: NADA (*New Arabic Dataset for Text Classification*) — a publicly available Arabic dataset.
  - Paper: [NADA: New Arabic Dataset for Text Classification (PDF)](https://thesai.org/Downloads/Volume9No9/Paper_28-NADA_New_Arabic_Dataset_for_Text_Classification.pdf)  
  - Overview: Combines **OSAC** and **DAA** datasets, classified according to the Dewey Decimal Classification (DDC) schema, balanced using **SMOTE**, and containing **13,066 documents** across **10 balanced categories**.
- **Structure** (adapted for the joint intent classification & slot filling task):
  - **Intents**: High-level user goals (e.g., booking flights, weather queries, etc.).
  - **Slots**: Entity spans within the utterance (e.g., dates, locations, names).
- **Preprocessing**:
  - Tokenization using the model’s tokenizer.
  - Special handling for Arabic script normalization and diacritics removal.
  - Applied stop-word removal and class balancing from the original NADA dataset preprocessing.

---
## ⚙️ Methodology
- **Data Preprocessing** – Arabic text normalization, tokenization, and label encoding.  
- **Model Architecture** – A shared transformer encoder with:  
  - **Intent Classification Head** (classification layer)  
  - **Slot Filling Head** (token classification layer)  
- **Joint Training** – Multi-task loss combining intent classification loss and slot filling loss.  
- **Evaluation** – Intent accuracy, slot F1-score, and joint goal accuracy.  

---

## 🛠️ Preliminary Requirements

### 🐍 Python Environment
Python 3.9 or later.

### 📦 Required Packages
```bash
pip install torch transformers datasets scikit-learn seqeval pandas numpy matplotlib
```

---
## 📊 Models & Evaluation Metrics

### 🧠 Models:
- **AraBERT-based Joint Model**  
- **Multilingual BERT-based Joint Model**  

### 📏 Metrics:
- **Intent Accuracy**  
- **Slot F1-score**  
- **Joint Goal Accuracy**  

---

## 📈 Results
- The **AraBERT joint model** achieved higher performance compared to separate-task baselines.  
- Joint learning improved slot filling by leveraging intent context.  

---

## 📄 Reference
If you use this work, please cite:  
> *Placeholder for citation or reference to the Arabic JICSF study*
