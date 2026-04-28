# 🔬 CreditLens — Credit Risk Intelligence Platform

> An end-to-end machine learning platform that predicts **credit card payment default** using 13 trained models, delivered through an interactive **7-tab Streamlit dashboard**.

[![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.56.0-FF4B4B?logo=streamlit)](https://streamlit.io/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.6.1-F7931E?logo=scikitlearn)](https://scikit-learn.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-2.1.4-189AB4)](https://xgboost.readthedocs.io/)

---

## 🚀 Live Demo

👉 **Try the app here:**  
https://capstoneproject1-n5ckeazmkwjaclud7rz6xy.streamlit.app/

No installation required — fully deployed on Streamlit Cloud.

---

## 📂 GitHub Repository

👉 **Source code:**  
https://github.com/Anitha-Gowthami-AIML/Capstone_Project_1_CCD

---

## 🧠 Overview

CreditLens solves the **credit default classification problem** using the UCI dataset of 30,000 Taiwanese bank clients.

### Core Challenge
- Severe **class imbalance (~22% defaults)**
- Standard models tend to **miss defaulters (low recall)**

### Solution Strategy

| Group | Approach | Threshold |
|------|---------|----------|
| **Baseline** | No imbalance handling | 0.5 |
| **Imbalance-Handled** | SMOTE + class weights | 0.3 |
| **Tuned** | Hyperparameter optimization | 0.3 |

---

## 📊 Dataset

| Feature | Value |
|--------|------|
| Source | UCI ML Repository |
| Records | 30,000 |
| Target | `DEFAULT` |
| Class Split | 78% Non-default / 22% Default |
| Time Period | Apr–Sep 2005 |

---

## ⚙️ Feature Engineering

Created **9 high-signal features**:

- `UTIL_RATE` → Credit utilization pressure  
- `AVG_PAY_STATUS` → Repayment delay severity  
- `TOTAL_BILL` → Exposure  
- `TOTAL_PAY` → Payment behavior  
- `PAY_RATIO` → Repayment capacity  
- `BILL_TREND` → Debt growth  
- `PAY_TREND` → Payment change  
- `MAX_PAY_DELAY` → Worst delay  
- `CONSEC_LATE` → Late payment frequency  

👉 **Total Features: 32 (23 original + 9 engineered)**

---

## 🤖 Models Trained (13 Total)

### Baseline Models
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- XGBoost

### Imbalance Handling
- SMOTE + Logistic / RF / XGB
- Class-weighted Logistic / RF / XGB

### Tuned Models
- Tuned SMOTE XGBoost
- Tuned Weighted XGBoost

---

## 🖥️ Streamlit App Features

### 📌 7 Interactive Tabs

1. **Overview & Glossary**
2. **Exploratory Data Analysis**
3. **Feature Engineering**
4. **Model Building**
5. **Model Comparison**
6. **Feature Importance**
7. **Live Predictor**

---

## 📈 Key Results

| Model | AUC | F1 | Recall | Precision |
|------|-----|----|--------|----------|
| Baseline XGBoost | ~0.78 | ~0.47 | ~0.37 | ~0.64 |
| SMOTE XGBoost | ~0.77 | ~0.52 | ~0.61 | ~0.45 |
| Weight XGBoost | ~0.78 | ~0.53 | ~0.62 | ~0.46 |
| **Tuned SMOTE XGB** | **~0.78** | **~0.55** | **~0.65** | **~0.47** |

### 🔍 Insights

- Payment history (`PAY_0`, `AVG_PAY_STATUS`) dominates prediction
- SMOTE & class weights improve **recall significantly**
- Lowering threshold (0.5 → 0.3) corrects bias
- Tuned XGBoost gives best **F1 balance**

---

## ⚡ Quickstart (Local Setup)

```bash
git clone https://github.com/Anitha-Gowthami-AIML/Capstone_Project_1_CCD.git
cd Capstone_Project_1_CCD

```bash
git clone https://github.com/Anitha-Gowthami-AIML/Capstone_Project_1_CCD.git
cd Capstone_Project_1_CCD
