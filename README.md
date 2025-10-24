# Smishing Detection Using Machine Learning

A machine learning-based system for detecting **Smishing (SMS Phishing)** messages that trick users into sharing sensitive information such as passwords or banking credentials.  
This project uses natural language processing (NLP) and multiple ML classifiers to automatically differentiate between **legitimate (ham)** and **fraudulent (smishing)** SMS messages.

---
🧠 Project Overview

With the rise of mobile communication, **smishing attacks** have become a serious cybersecurity threat.  
This project develops a **privacy-preserving, on-device smishing detection model** that identifies deceptive text messages—even those using obfuscated words like “cl!ck” or “v3rify.”

Key features include:
- Automated text preprocessing and feature extraction using **TF-IDF**.
- Handling class imbalance using **Random OverSampling**.
- Evaluation of multiple ML models.
- Adversarial testing for real-world message manipulation.

---
⚙️ System Architecture

The project follows a modular pipeline:

1. **Data Collection** – SMS dataset from Kaggle with ham and smishing messages.  
2. **Text Preprocessing** – Lowercasing, stopword removal, URL and punctuation cleaning.  
3. **Feature Extraction** – TF-IDF vectorization (max 5000 features).  
4. **Label Encoding** – Encoding “ham” and “smishing” labels numerically.  
5. **Balancing Dataset** – Using `RandomOverSampler` to address class imbalance.  
6. **Model Training** – Logistic Regression, SVM, Random Forest, AdaBoost, and XGBoost.  
7. **Adversarial Testing** – Evaluating robustness to obfuscated keywords.  
8. **Evaluation** – Accuracy, F1-score, ROC-AUC, and confusion matrix analysis.

---
🧩 Machine Learning Models Used

| Model | Accuracy | Precision | Recall | F1-Score |
|:------|:---------:|:----------:|:-------:|:--------:|
| Logistic Regression | 96.86% | 1.00 | 0.76 | 0.86 |
| **SVM** | **99.00%** | **1.00** | **0.95** | **0.98** |
| Random Forest | 98.89% | 1.00 | 0.93 | 0.96 |
| AdaBoost | 92.12% | 1.00 | 0.35 | 0.52 |
| XGBoost | 98.41% | 0.98 | 0.92 | 0.95 |

✅ **SVM performed best**, achieving **99% accuracy** and robust detection of adversarial messages.

---
📊 Visual Outputs

- Heatmaps for feature correlation (before & after preprocessing)
- Class distribution graphs (original vs balanced)
- ROC Curves for all classifiers
- Confusion matrices for model comparison
- Sample and adversarial predictions

---

