# 🧠 AI Bootcamp Project — Sales Prediction with Regression Models

### Team G3 — Mariana • Adrian • Roland • Natalie  

---

## 📘 Executive Summary

This project explores different regression models to predict **daily sales** using a dataset (`sales.csv`) containing features such as number of customers, promotions, holidays, and store information.  

After testing multiple approaches, **Polynomial Regression** delivered the best results with an **R² of 0.876**, outperforming both Linear Regression and Random Forest in terms of accuracy and computation efficiency.

---

## 🚀 Project Overview

| Model | R² Score | MAE (€) | Notes |
|--------|-----------|----------|-------|
| **Linear Regression** | 0.85 | ≈ 987 | Strong performance, no overfitting |
| **Polynomial Regression (deg=4)** | 0.88 | ≈ 896 | Best overall accuracy |
| **Random Forest** | — | — | Accurate but too slow for production use |

**Trade-off:** Polynomial regression achieved a good balance between **speed** and **accuracy**, making it the optimal choice for this dataset.

---

## 🧩 Data Preprocessing

1. Loaded and examined the dataset shape and column types.  
2. Checked for null values and deleted irrelevant columns.  
3. Converted date columns into integers.  
4. Analyzed correlations to identify relationships between customer counts and sales.  
5. Created a **correlation heatmap** to visualize feature relationships.  

---

## 🤖 Models & Methods

### 1️⃣ Linear Regression
- **Library:** scikit-learn  
- **Goal:** Predict daily sales from customer and store features.  
- **Steps:**
  - Train/Test split (80/20)
  - Feature scaling
  - Model training and evaluation  
- **Results:**  
  - R² = 0.85  
  - MAE ≈ €987  
  - Similar results across train/test → good generalization  

---

### 2️⃣ Polynomial Regression (degree = 4)
- **Library:** scikit-learn  
- **Goal:** Capture non-linear relationships (promotions, holidays, etc.).  
- **Results:**  
  - R² = 0.88  
  - MAE ≈ €896  
  - Equal train/test R² → no overfitting  
  - Degree 4 provided the best trade-off between accuracy and performance  

---

### 3️⃣ Random Forest
- **Library:** scikit-learn  
- **Goal:** Evaluate ensemble-based prediction performance on time series data.  
- **Approach:**
  - Used **TimeSeriesSplit** for chronological validation (avoiding data leakage).  
  - Trained **RandomForestRegressor** with cross-validation using `cross_val_score`.  
- **Outcome:** Accurate but **computationally expensive** (≈ 20 minutes).  

---

## 📊 Key Takeaways

- **Best model:** Polynomial Regression (degree = 4)  
- **Accuracy:** R² = 0.876  
- **Challenges:**
  - Ensuring data consistency between train/test sets  
  - Managing feature scaling and inverse transformations correctly  
- **Learnings:**
  - Data preprocessing consistency is crucial  
  - Feature scaling must be inverted for accurate result interpretation  

---

## 🛠️ Tech Stack

- **Language:** Python  
- **Libraries:**  
  - pandas  
  - numpy  
  - scikit-learn  
  - matplotlib / seaborn  


