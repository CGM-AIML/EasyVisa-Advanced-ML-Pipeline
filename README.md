# EasyVisa – Advanced Machine Learning Pipeline

## Executive Summary
Employment-based U.S. visa sponsorship is a high-cost, high-uncertainty process where denial results in lost time, legal expense, and missed talent opportunities. This project delivers an advanced machine learning pipeline designed to estimate visa approval likelihood using historical labor certification data, enabling earlier risk assessment and more informed petition strategies.

The system is built with production-grade considerations in mind, including class imbalance handling, probability calibration, model interpretability, and business-aligned evaluation thresholds.

---

## Business Objective
Develop a decision-support classification system that:

- Accurately ranks approval likelihood across applications  
- Produces **reliable probability estimates**, not just predictions  
- Supports risk-aware decision-making prior to petition filing  

This project explicitly prioritizes **operational usefulness over leaderboard metrics**.

---

## Data Overview
- Historical U.S. labor certification and visa application records  
- Mixed numeric and categorical features, including:
  - Wage information (normalized across units)
  - Education level
  - Employment type
  - Geographic and employer attributes  
- Strong class imbalance between approved and denied outcomes  

---

## Technical Approach

### 1. Data Integrity & Preprocessing
- Canonical data validation and cleaning  
- Wage normalization and unit harmonization  
- Robust handling of missing and categorical values  
- Feature encoding suitable for both linear and tree-based models  

### 2. Class Imbalance Strategy
- Synthetic Minority Oversampling (SMOTE)  
- Class weighting where appropriate  
- Evaluation metrics selected to reflect real-world imbalance  

### 3. Model Development
Models evaluated include:
- Logistic Regression (baseline and interpretability anchor)  
- Histogram Gradient Boosting  
- Tree-based ensemble methods  

All models were trained using **stratified cross-validation** to preserve class distributions.

### 4. Probability Calibration
To ensure decision reliability:
- Platt scaling and Isotonic regression were applied  
- Calibration curves were evaluated alongside discrimination metrics  
- Outputs are suitable for threshold-based business decisions  

---

## Evaluation Framework
Model performance was assessed using:
- ROC-AUC for ranking quality  
- Precision–Recall analysis for minority-class sensitivity  
- Calibrated probability reliability  
- Confusion matrices evaluated at business-relevant thresholds  

This approach ensures the model’s outputs remain **actionable**, not just statistically strong.

---

## Key Findings
- Wage normalization and education level are dominant approval signals  
- Probability calibration meaningfully improves downstream decision confidence  
- Interpretable models provide insights aligned with regulatory and policy constraints  
- Accuracy alone is insufficient without probability reliability in high-risk decisions  

---

## Limitations
- Historical bias in approval decisions may propagate into predictions  
- Regulatory changes over time can impact model generalizability  
- This system is **decision-support only**, not a legal determination engine  

---

## Next Steps
- Temporal validation across filing years  
- Fairness and bias audits across demographic and employer segments  
- Packaging as an internal screening or advisory tool  
- Integration with policy-aware RAG systems for contextual guidance  

---

## Project Context
This project was completed as part of the **Advanced Machine Learning curriculum** in the  
**UT Austin / Great Learning Post Graduate Program in AI & ML** and has been refactored and extended for **portfolio-grade publication**.

[View FoodHub Project in ePortfolio](https://www.mygreatlearning.com/eportfolio/christopher-gonzalez-mejias)  
