# CVSS Severity & Base Score Prediction using BERT

A Machine Learning and NLP-based cybersecurity project that uses **BERT (Bidirectional Encoder Representations from Transformers)** to automatically predict:

-  **CVSS Severity Level** (Classification)
-  **CVSS Base Score** (Regression)

using only the **CVE vulnerability description/summary** as input.

The system analyzes vulnerability text descriptions and generates:
- A numeric **CVSS Base Score (0–10)**
- A categorical **Severity Level**:
  - None
  - Low
  - Medium
  - High
  - Critical

Both tasks are implemented independently using **HuggingFace Transformers** and fine-tuned BERT models.

---

#  Project Objective

The main objective of this project is to automate vulnerability risk assessment by leveraging Natural Language Processing (NLP) and Deep Learning techniques.

Traditional CVSS scoring requires manual analysis by security professionals. This project reduces manual effort by predicting vulnerability severity directly from textual vulnerability descriptions.

---

#  Features

-  BERT-based Vulnerability Severity Classification
-  BERT-based CVSS Score Regression
-  End-to-End NLP Pipeline
-  Automated Text Cleaning & Preprocessing
-  Tokenization using BERT Tokenizer
-  Label Encoding for Severity Classes
-  Accuracy, Precision, Recall & F1 Evaluation
-  Real-time Single Input Inference
-  Modular and Reusable Python Scripts
-  Compatible with:
  - Kaggle GPU
  - Google Colab
  - Local GPU Environment

---

#  Workflow

## 1. Data Collection
The dataset is collected from publicly available CVE/NVD vulnerability databases containing:
- CVE ID
- Vulnerability Description
- CVSS Base Score
- Severity Labels

---

## 2. Data Preprocessing
The raw vulnerability descriptions are cleaned and processed using:
- Lowercasing
- Removing unwanted symbols
- Handling null values
- Text normalization
- Label encoding

---

## 3. Tokenization
The cleaned text is tokenized using the **BERT Tokenizer** (`bert-base-uncased`) to convert textual data into transformer-readable tokens.

---

## 4. Model Training

### 🔹 Classification Model
Predicts:
- None
- Low
- Medium
- High
- Critical

### 🔹 Regression Model
Predicts:
- CVSS Base Score (0–10)

Both models are fine-tuned independently using pretrained BERT architecture.

---

## 5. Evaluation
The models are evaluated using:

### Classification Metrics
- Accuracy
- Precision
- Recall
- F1-Score

### Regression Metrics
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)

---

## 6. Inference
The trained model accepts a new vulnerability description as input and predicts:
- CVSS Severity Level
- CVSS Base Score

---

#  Architectural Diagram

```text
CVE Vulnerability Description
            │
            ▼
Text Cleaning & Preprocessing
            │
            ▼
BERT Tokenization
            │
            ▼
BERT Encoder (bert-base-uncased)
            │
 ┌──────────┴──────────┐
 ▼                     ▼
Severity            CVSS Score Regression
Classification
 |                     | 
 ▼                     ▼
Severity Label      CVSS Base Score
```

---

#  Tech Stack

- Python
- BERT
- HuggingFace Transformers
- PyTorch
- Scikit-learn
- Pandas
- NumPy

---

#  Project Structure

```text
CVSS-Severity-Prediction/
│
├── notebooks/
│   ├── cvss-severity-score-prediction.ipynb
│   └── inference-cvss.ipynb
│
├── src/
│   ├── inference.py.txt
│   ├── preprocess.py.txt
│   ├── train_classification.py.txt
│   ├── train_regression.py.txt
│   └── utils.py.txt
│
├── .gitignore.txt
├── README.md
└── requirements.txt
```
---

#  Installation & Execution

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Train Severity Classification Model

```bash
python src/train_classification.py
```

---

## Train CVSS Regression Model

```bash
python src/train_regression.py
```

---

## Run Inference

```bash
python src/inference.py
```

---

#  Future Enhancements

- Multi-task Learning using single BERT model
- Explainable AI (XAI) integration
- Deployment using Flask/FastAPI
- Real-time CVE feed integration
- Web Dashboard for prediction visualization

---



Made with ❤️ by **Himavanth A Bhat**
