# Telco Customer Churn Prediction

This project predicts customer churn in the telecom industry using the **Telco Customer Churn dataset** from Kaggle.
It was developed as part of my Master's Thesis at GISMA University (2025).

---

##  Project Structure


Telco-Churn-Prediction/
│
├── data/
│ └── telco_churn.csv # dataset
│
├── notebooks/
│ └── churn_pipeline.ipynb # Jupyter Notebook with code
│
├── reports/
│ └── thesis_pipeline.html # full pipeline report with figures
│
└── README.md # project overview




---

## 1) Dataset
- 7,043 customers, 23 features, target: `Churn` (Yes/No)
- Features include demographics, services, billing, and contract details
- Class imbalance: ~27% churn vs 73% non-churn

---

## 2) Exploratory Data Analysis (EDA)
Main findings from EDA:
- Senior citizens and single households churn more
- Fiber optic internet users churn at a much higher rate
- Lack of online security and tech support strongly increases churn
- Month-to-month contracts and electronic check payment methods show the highest churn
- Higher monthly charges increase churn, while longer tenure reduces it

---

## 3) Preprocessing
- Missing values imputed (median / most frequent)
- One-hot encoding for categorical variables
- Standard scaling for numerical features (for Logistic Regression and Neural Networks)
- SMOTE applied to handle class imbalance
- Separate preprocessing pipelines for linear vs. tree-based models

---

## 4) Models
- Logistic Regression
- Random Forest
- XGBoost
- Neural Network

---

## 5) Results
- **Logistic Regression (balanced):** Highest ROC-AUC (0.841), most interpretable
- **XGBoost:** Best predictive performance, highest Average Precision (0.649), strong recall
- **Random Forest:** Stable baseline, but slightly below LR and XGB
- **Neural Network:** Competitive, high recall but lower precision and more complexity

---

## 6) Conclusion
- **Best predictive model:** XGBoost → best balance of precision and recall
- **Best interpretable model:** Logistic Regression → highest ROC-AUC and clear explanations
- Business takeaway:
  - Promote long-term contracts
  - Encourage secure payment methods (avoid electronic checks)
  - Bundle value-added services such as online security and tech support

---

## 7) How to Run
This project runs directly in **Google Colab**.
If running locally, please install the following packages:



---
