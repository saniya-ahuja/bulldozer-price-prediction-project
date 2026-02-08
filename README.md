# 🚜 Predicting the Sale Price of Bulldozers using Machine Learning

> **End-to-end regression modeling on real-world auction data**

This project builds a complete **machine learning regression pipeline** to predict the **sale price of bulldozers** using historical auction data.  
The notebook demonstrates real-world ML problem solving — from messy raw data to a tuned, interpretable model.

---

## 🎯 Problem Statement

Heavy machinery auctions involve high financial stakes, yet pricing is often uncertain due to:

- Variability in machine age and usage  
- Diverse equipment specifications  
- Market fluctuations over time  

The goal of this project is to **learn pricing patterns from historical auction data** and generate **accurate sale price predictions** using machine learning.

---

## 🧠 Project Overview

This notebook walks through the full ML workflow:

📦 **Raw Auction Data**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

📅 **Date Parsing & Sorting**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

🧠 **Feature Engineering**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

🧹 **Missing Value Handling**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

🏷️ **Categorical Encoding**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

🌲 **Random Forest Regression**  
&nbsp;&nbsp;&nbsp;&nbsp;⬇️  

📊 **Model Evaluation & Interpretation**


The focus is on **robust preprocessing, correct evaluation metrics, and model interpretability**.

---

## 📊 Dataset Description

The dataset contains historical bulldozer auction records with features such as:

- Sale date  
- Machine age  
- Usage hours  
- Equipment and product group  
- Machine configuration details  

The target variable is:

- **SalePrice** — the final auction sale price of the bulldozer

---

## 🛠️ Key Steps in the Notebook

### 1️⃣ Data Preprocessing
- Parsed `saledate` into datetime format
- Sorted data chronologically to avoid data leakage
- Extracted date-based features (year, month, day, etc.)
- Preserved a clean copy of the original dataset

### 2️⃣ Feature Engineering
- Converted string-based categorical features into categories
- Encoded categorical variables numerically
- Added time-based features derived from sale date

### 3️⃣ Handling Missing Values
- Filled missing numerical values using statistical strategies
- Filled missing categorical values with placeholder categories
- Ensured model compatibility without dropping large amounts of data

---

## 🤖 Modeling Approach

### Model Used
- **Random Forest Regressor**

### Why Random Forest?
- Captures non-linear relationships
- Handles mixed feature types well
- Robust to outliers
- Minimal assumptions about data distribution

---

## 📐 Model Evaluation

### Metric: RMSLE (Root Mean Squared Logarithmic Error)

RMSLE is used because:
- It penalizes **under-prediction more heavily**
- It is robust to large differences in scale
- It aligns well with real-world pricing accuracy expectations

A custom evaluation function is implemented to consistently measure performance.

---

## 🔍 Hyperparameter Tuning

- Used **RandomizedSearchCV** to efficiently search hyperparameter space
- Tuned parameters such as:
  - Number of trees
  - Max depth
  - Minimum samples per split
- Trained the final model using the best-performing configuration

---

## 📈 Model Insights

### Feature Importance
The notebook visualizes feature importance to show:
- Which variables most influence price
- How machine age, usage, and configuration affect predictions

This step improves **model interpretability**, a key requirement in real-world ML systems.

---

## 🧪 Test Set Predictions

- Applied the same preprocessing pipeline to test data
- Generated predictions on unseen data
- Ensured consistency between training and inference pipelines

---

## 🧰 Tools & Technologies

- **Python**
- **Pandas / NumPy**
- **Scikit-learn**
- **Random Forest Regression**
- **Matplotlib / Seaborn**
- **Jupyter Notebook**

---

## 💡 What This Project Demonstrates

- Real-world data cleaning and preprocessing
- Thoughtful feature engineering
- Correct metric selection for regression
- Hyperparameter tuning at scale
- Model interpretability via feature importance
- End-to-end ML pipeline design

---

## 🚀 Next Steps / Extensions

- Deploy model behind an inference API
- Integrate into a web-based prediction app
- Add model monitoring and drift detection
- Experiment with gradient boosting models

---

## 📌 Summary

This notebook is not just about training a model —  
it demonstrates **how to think like a machine learning engineer** when solving a real, noisy, high-impact business problem.

Ideal for:
- ML portfolios  
- Resume projects  
- Technical interviews  

⭐ If you found this project useful, feel free to explore and build on it!
