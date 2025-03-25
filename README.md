# EmotionVerse Sentiment Classification

This repository explores sentiment classification on the **EmotionVerse** dataset using a variety of Natural Language Processing (NLP) and machine learning techniques. The EmotionVerse dataset consists of short texts labeled with one of five sentiment categories:

- **Positive**
- **Negative**
- **Neutral**
- **Mixed**
- **Ambiguous**

---

## 🔍 Project Overview

The project is split into two main notebooks:

1. **`preproc.ipynb`** – Focused on:
   - Text cleaning and normalization
   - Exploratory Data Analysis (EDA)
   - Feature extraction with various techniques:
     - Bag-of-Words (BoW)
     - TF-IDF
     - VADER and NRC lexicon features
     - Sentence embeddings (using BERT)
     - Feature combinations and normalization

2. **`models.ipynb`** – Focused on:
   - Sentiment classification using various models:
     - Logistic Regression
     - Linear SVM
     - Random Forest (in specific scenarios)
   - Evaluation across multiple feature sets
   - Model comparison using Accuracy and F1-Score
   - Confusion matrices and per-class performance
   - Fine-tuning with precomputed **BERT** embeddings and advanced classifiers

---

## 🧪 Feature Engineering

We evaluated and combined different types of features:

- **Traditional**: TF-IDF, BoW
- **Lexicon-based**: VADER and NRC
- **Embedding-based**: Sentence-BERT (`all-MiniLM-L6-v2`)
- **Combined**: Multiple fusion strategies (e.g., TF-IDF + VADER + BERT)

---

## 📊 Model Evaluation

We compared models trained on different feature representations. Highlights include:

- **Best non-BERT model**:  
  `Combined All BERT + Logistic Regression`  
  → Accuracy: **0.800**, F1-Score: **0.7968**

- **Best BERT fine-tuned model**:  
  `BERT Fine-tuned + SVM (RBF Kernel)`  
  → Accuracy: **0.7813**, F1-Score: **0.7784**

---

## 📁 Files

- `preproc.ipynb`: Text preprocessing, EDA, and feature extraction
- `models.ipynb`: Model training, evaluation, comparison
- `emotionverse_features_advanced/`: Directory storing precomputed features
- `best_sentiment_model.pkl`: Saved best-performing model
- `sentiment_model_comparison_with_bert.csv`: Summary table of all results

---

## 🚀 How to Reproduce

1. Clone the repo
2. Install dependencies (see below)
3. Run the notebooks in order:
   - `preproc.ipynb`
   - `models.ipynb`

---

## ⚙️ Dependencies

```bash
pip install -r requirements.txt
