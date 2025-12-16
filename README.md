# Credit Risk Scoring System (Fintech ML Project)

## Overview
This project builds a **credit risk scoring model** used by fintech companies and banks to predict the probability of loan default.  
The model converts raw applicant data into a **risk score (0–100)** that can be used for loan approval, rejection, or risk-based pricing.

This project is **production-aligned** and focuses on:
- Imbalanced data handling  
- Mixed numerical + categorical features  
- Interpretable, regulator-friendly models  

---

## Problem Statement
Given historical loan applicant data, predict whether a borrower will **default** on a loan.

This mirrors real fintech use cases such as:
- Personal loans
- BNPL risk checks
- Credit underwriting
- SME lending

---

## Dataset
**Keyword:** `loan default prediction dataset`

Typical features:
- Applicant income
- Loan amount
- Credit history
- Employment details
- Loan purpose

**Target variable (auto-detected):**
- `loan_status`, `default`, `is_default`, or similar

---

## ML Approach

### Preprocessing
- Numerical features → Standard Scaling  
- Categorical features → One-Hot Encoding  
- Missing values → Dropped (can be improved with imputation)

### Model
- **Logistic Regression**
  - Widely accepted in banking
  - Explainable & regulator-safe
  - Handles imbalanced data using class weighting

### Evaluation Metrics
- ROC-AUC (primary fintech metric)
- Precision / Recall
- F1-Score

---

## Project Pipeline
1. Load & inspect dataset  
2. Auto-detect target column  
3. Split data (stratified)  
4. Preprocess features  
5. Train credit risk model  
6. Evaluate performance  
7. Generate credit risk score  
8. Save model for deployment  

---

## Output
- **Probability of default**
- **Credit risk score (0–100)**
- Trained model file: `credit_risk_fintech.pkl`

---

## Example Use Case
```python
credit_score(applicant_data)
