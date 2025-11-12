# 🛡️ Network Intrusion Detection using Machine Learning (UNSW-NB15)

> A machine learning-based Intrusion Detection System (IDS) designed to classify normal and malicious network traffic using the UNSW-NB15 dataset.

---

## 📘 Overview
This project aims to build a **Network Intrusion Detection System (IDS)** using **machine learning and deep learning models**.  
It leverages the **UNSW-NB15 dataset**, which contains modern network traffic including both normal and attack patterns.

The goal is to preprocess the dataset, train classification models (such as **KNN**, **MLP**, etc.), and evaluate their ability to accurately detect attacks.

---

## 🧠 Objectives
- Detect and classify malicious network activities.
- Compare different ML models (KNN, MLP, etc.).
- Apply preprocessing, balancing, and feature selection techniques.
- Evaluate models using accuracy, ROC curve, and confusion matrix.

---

## ⚙️ Project Pipeline

1. **Data Loading & Cleaning**
   - Load `UNSW_NB15.csv` and feature descriptions.
   - Remove invalid or missing entries (e.g., `service` = '-').
   - Convert target column `label` into binary format (0 = normal, 1 = attack).

2. **Preprocessing**
   - Apply **StandardScaler** to normalize numerical features.
   - Encode categorical features using **One-Hot Encoding**.
   - Remove highly correlated features to avoid redundancy.

3. **Balancing Classes**
   - Handle class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**.

4. **Model Training**
   - Implement **K-Nearest Neighbors (KNN)** classifier.
   - Use **RandomizedSearchCV** for hyperparameter tuning.
   - Compare with a **Deep Learning model (MLP)** for further evaluation.

5. **Evaluation**
   - Use metrics such as **accuracy**, **confusion matrix**, and **ROC-AUC**.
   - Visualize **learning curves** to detect overfitting.

---

## 🧩 Best KNN Parameters Found
```python
{'weights': 'distance', 'n_neighbors': 3, 'metric': 'manhattan'}
