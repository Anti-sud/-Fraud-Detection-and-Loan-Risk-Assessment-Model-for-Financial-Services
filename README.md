# 🏦 Fraud Detection and Loan Risk Assessment Model

An end-to-end machine learning pipeline for predicting **fraud risk** and **loan approval status** in financial services.  
This project demonstrates how to build scalable fraud detection and credit risk models using real-world inspired loan application data.

---

## 📋 Project Overview

### Goals:
- Predict the likelihood of **fraudulent loan applications** (binary classification: Fraud / Not Fraud).
- Predict **loan approval status** (multi-class classification: Approved, Declined, Fraudulent).
- Handle **severe class imbalance** using SMOTE.
- Create a **reusable pipeline** for production-ready predictions on new loan applications.

---

## ⚙️ Techniques Used

- **Data Preprocessing**:
  - Missing value treatment
  - Outlier capping (1st and 99th percentiles)
  - Ratio-based feature engineering
  - Time-based feature extraction
  - Placeholder transaction aggregations (future enhancement)

- **Imbalance Handling**:
  - SMOTE for minority oversampling in training data

- **Models**:
  - Logistic Regression (binary + multiclass)
  - Random Forest
  - LightGBM (comparison)

- **Evaluation**:
  - Classification report
  - ROC AUC
  - Confusion matrix
  - Fraud recall and F1-score

- **Pipeline Deployment**:
  - Custom prediction function for real-time scoring
  - Handles new application data

---

## 📊 Results

### Fraud Detection (Binary Classification):

| Metric     | Logistic Regression |
|------------|---------------------|
| ROC AUC    | 0.89                |
| Fraud Recall | 0.62              |
| Fraud Precision | 0.32           |
| Fraud F1-score | 0.42            |

**Best fraud detection performance** — outperforming complex models (Random Forest, LightGBM).

---

### Loan Status Assessment (Multiclass Classification - Combined Fraudulent):

| Class        | Precision | Recall | F1-score |
|--------------|-----------|--------|----------|
| Approved     | 0.87      | 0.94   | 0.90     |
| Declined     | 0.51      | 0.29   | 0.37     |
| Fraudulent   | 0.99      | 0.85   | 0.92     |

Overall accuracy: **84%**

Key outcomes:
- The **Logistic Regression fraud model** achieved ~85% fraud recall — critical for preventing fraudulent approvals.
- The **loan status model** (Approved / Declined / Fraudulent) reached 84% accuracy, with strong fraud detection capability (85% fraud recall).
- Predictions on new applications demonstrated the system's ability to:
    - Flag high-risk fraudulent applications
    - Assess approval likelihood based on applicant profile

**Real-world use cases**:
- Can be deployed in a **loan underwriting system** to assist risk analysts.
- Provides **early fraud detection** for compliance teams.
- Automates loan decisioning workflows with transparent, interpretable outputs.
- Reduces potential financial losses by improving fraud capture at application stage.

Future enhancements may include:
- Adding transaction behavior data for even better fraud detection.
- Ensemble modeling to improve classification of borderline cases.
- Threshold tuning to balance false positives and false negatives based on business need.

Overall, this pipeline provides a strong foundation for building **AI-driven risk management tools** in the financial services industry.


