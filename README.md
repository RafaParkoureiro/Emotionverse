# EmotionVerse Sentiment Classification

This repository explores sentiment classification on the **EmotionVerse** dataset using a variety of Natural Language Processing (NLP) and machine learning techniques. The EmotionVerse dataset consists of short texts labeled with one of five sentiment categories:

- **Positive**
- **Negative**
- **Neutral**
- **Mixed**
- **Ambiguous**

---

##  Project Overview

The project is organized across three main notebooks:

1. **[`PreProcessingEmotionverseText.ipynb`](https://github.com/RafaParkoureiro/Emotionverse/blob/main/PreProcessingEmotionverseText.ipynb)**  
   Focuses on:
   - Text cleaning and normalization
   - Exploratory Data Analysis (EDA)
   - Preliminary insights into class distribution and word usage

2. **[`Feature_Extraction_EDA.ipynb`](https://github.com/RafaParkoureiro/Emotionverse/blob/main/Feature_Extraction_EDA.ipynb)**  
   Dedicated to feature engineering:
   - Bag-of-Words (BoW)
   - TF-IDF vectorization
   - Lexicon-based features (VADER and Custom Lexicon)
   - Sentence embeddings (Sentence-BERT: `all-MiniLM-L6-v2`)
   - Feature normalization and combination strategies

3. **[`Classification.ipynb`](https://github.com/RafaParkoureiro/Emotionverse/blob/main/Classification.ipynb)**  
   Responsible for training and evaluating sentiment classifiers:
   - Logistic Regression, SVM, Random Forest, Naive Bayes
   - Evaluation on multiple feature sets
   - Confusion matrices and class-wise metrics
   - Model comparison using Accuracy and F1-Score
   - Fine-tuning with BERT embeddings and advanced classifiers
   - Explainability
     
4. **[`robertafinetuned.ipynb`](https://github.com/RafaParkoureiro/Emotionverse/blob/main/robertafinetuned.ipynb)**  
   Uses a pre-trained model (Hugging Face's Roberta-base) and adapts to our domain to classify the sentiment:
   - Fine-tunes the model
   - Cross-validation for robust analysis
   - Visualizations and results
   - Where it fails and why

4. **[`sentimentmodelfinetuned.ipynb`](https://github.com/RafaParkoureiro/Emotionverse/blob/main/sentimentmodelfinetuned.ipynb)**  
   Uses a pre-trained model (Hugging Face's distilbert-base-uncased-finetuned-sst-2-english) and adapts to our domain to classify the sentiment:
   - Fine-tunes the model
   - Cross-validation for robust analysis
   - Visualizations and results
   - Where it fails and why

---

##  Feature Engineering

We evaluated and combined different types of features:

- **Traditional**: TF-IDF, BoW
- **Lexicon-based**: VADER and Custom Lexicon sentiment scores
- **Embedding-based**: Sentence-BERT (`all-MiniLM-L6-v2`)
- **Combined**: Multiple fusion strategies (e.g., TF-IDF + VADER + BERT)

---

##  Files

- `PreProcessingEmotionverseText.ipynb`: Text preprocessing and initial EDA
- `Feature_Extraction_EDA.ipynb`: Feature engineering and vectorization
- `Classification.ipynb`: Model training, evaluation, and comparison
- `emotionverse_features_advanced/`: Directory storing precomputed features
- `best_sentiment_model.pkl`: Saved best-performing model
- `sentiment_model_comparison_with_bert.csv`: Summary table of all results
- `sentimentmodelfinetuned.ipynb`: Using a sentiment pre-trained model from hugging face and fine-tune it 
- `robertafinetuned.ipynb`: Using the roberta-base pre-trained model from hugging face and fine-tune it
- `clean.csv`: The dataset used in most of the notebooks
---

##  How to Reproduce

1. Clone the repo
2. Run the notebooks in order:
   - `PreProcessingEmotionverseText.ipynb`
   - `Feature_Extraction_EDA.ipynb`
   - `Classification.ipynb`
   - `sentimentmodelfinetuned.ipynb` and `robertafinetuned.ipynb` ( the order doesn't matter )

