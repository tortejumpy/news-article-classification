# 📰 News Article Classification using NLP & Machine Learning

An end-to-end Natural Language Processing (NLP) project that automatically classifies news articles into multiple categories using classical machine learning techniques. The project demonstrates a full data science workflow—from data preprocessing and feature engineering to model evaluation, statistical validation, and final model selection.

---

## 📌 Project Overview

In modern digital platforms, thousands of news articles are published daily across diverse categories such as **Politics, Sports, Business, Wellness, and Entertainment**. Manual categorization is time-consuming, inconsistent, and not scalable.

This project builds an **automated news article classification system** that assigns articles to predefined categories using their textual content, enabling scalable content management and recommendation systems.

---

## 🎯 Objectives

- Automatically classify news articles into **10 predefined categories**
- Apply advanced **text preprocessing and feature extraction**
- Compare multiple **machine learning models**
- Perform **robust evaluation and statistical validation**
- Select a **production-ready, interpretable model**

---

## 📂 Dataset Description

- **Total Articles:** 50,000  
- **Categories:** 10 (Balanced dataset – 5,000 articles per category)
- **Features:**
  - Headline
  - Short Description
  - Keywords
  - Category (Target)

Balanced class distribution ensured fair training and evaluation without resampling.

---

## 🛠️ Tech Stack & Tools

- **Programming:** Python  
- **Libraries:**  
  - Data Handling: `pandas`, `numpy`  
  - NLP: `nltk`, `gensim`, `scikit-learn`  
  - Visualization: `matplotlib`, `seaborn`  
  - Modeling & Evaluation: `scikit-learn`  

---

## 🔄 Project Workflow

### 1️⃣ Data Cleaning & Preprocessing
- Lowercasing text
- Removing punctuation and special characters
- Stopword removal
- Tokenization and lemmatization
- Handling missing and empty text entries

Result: Clean, model-ready text with zero missing values.

---

### 2️⃣ Exploratory Data Analysis (EDA)
- Category distribution analysis
- Headline and description length analysis
- Word clouds for category-level insights
- Identification of overlapping vocabulary between similar categories

Key Insight:  
Lifestyle categories (e.g., Wellness, Parenting) share vocabulary, explaining later misclassifications.

---

### 3️⃣ Feature Engineering
Multiple text representations were explored:

| Method | Description |
|------|------------|
| Bag of Words | Count-based baseline representation |
| TF-IDF | Weighted representation emphasizing informative words |
| Word2Vec | Dense semantic word embeddings |

**TF-IDF** was selected as the primary feature set due to superior classification performance with classical ML models.

---

### 4️⃣ Dimensionality Reduction (Validation)
- **PCA** and **t-SNE** used for visualization
- Confirmed that articles form meaningful clusters based on language usage

Purpose: Validate that extracted features capture learnable structure.

---

### 5️⃣ Model Training
The following models were trained and evaluated:

- Logistic Regression
- Multinomial Naive Bayes
- Support Vector Machine (SVM)

Techniques used:
- Stratified train-test split
- Cross-validation
- Sampling for efficient experimentation

---

### 6️⃣ Model Evaluation
- Accuracy, Precision, Recall, F1-score (Macro & Weighted)
- Confusion matrix analysis
- Class-wise F1-score comparison

Observation:
- Strong performance for Sports, Style & Beauty, Food & Drink
- Confusion between semantically similar categories (e.g., Politics vs World News)

---

### 7️⃣ Hyperparameter Tuning
- GridSearchCV applied to all models
- Tuned parameters improved stability more than raw accuracy

---

### 8️⃣ Statistical Validation
To ensure decisions were not based on random variation:
- Bootstrap confidence intervals
- McNemar’s test for pairwise model comparison

Result:
- Logistic Regression and SVM were statistically comparable
- Logistic Regression showed better stability and consistency

---

## 🏆 Final Model Selection

### ✅ **Selected Model: Logistic Regression (TF-IDF Features)**

**Why Logistic Regression?**
- Best **Weighted F1-score (~0.60)**
- Most stable cross-validation performance
- Interpretable coefficients
- Production-friendly and scalable
- Statistically comparable to SVM with lower complexity

---

## 📊 Final Results (Summary)

| Model | Test Accuracy | Weighted F1 | CV Stability |
|-----|---------------|-------------|--------------|
| Logistic Regression | ~0.61 | **~0.60** | **High** |
| Naive Bayes | ~0.61 | ~0.59 | Medium |
| SVM | ~0.62 | ~0.60 | Lower |

---

## 🚀 Business Impact

- Automates large-scale news categorization
- Improves content discovery and personalization
- Reduces manual editorial effort
- Scalable for real-world deployment
- Interpretable and monitorable ML solution

---

## 📈 Key Learnings

- Feature quality matters more than model complexity in NLP
- TF-IDF remains highly effective for classical text classification
- Statistical validation is essential for trustworthy model selection
- Interpretability and stability are critical for production ML systems

---

## 📌 Future Improvements

- Try transformer-based models (BERT) for improved semantic understanding
- Incorporate full article text instead of headlines only
- Deploy as an API or web application
- Add real-time prediction pipeline

---

## 👤 Author

**Harsh Pandey**  
Aspiring Data Scientist | Machine Learning & NLP Enthusiast  

---

⭐ If you found this project helpful, feel free to star the repository!
