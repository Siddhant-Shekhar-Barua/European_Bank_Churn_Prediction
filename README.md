# Bank Customer Retention: End-to-End Predictive ML Solution

## 📌 Project Overview
This repository contains a full-stack data professional asset designed to stop capital flight in a commercial bank's portfolio. Instead of relying on lagging historical indicators, this project bridges the gap between **Machine Learning Engineering** and **Strategic Business Intelligence** to provide front-line managers with an interactive, proactive retention ecosystem.

### Key Milestones Achieved:
1. **Engineered a High-Recall Machine Learning Engine** in Python to catch escaping accounts *before* they close.
2. **Resolved Enterprise-Level Data Discrepancies** ensuring seamless tabular integration of complex probabilities across 10,000 active customer rows.
3. **Designed a 3-Page Strategic Dashboard Framework** in Power BI to serve both executive leadership (C-Suite) and tactical outreach teams.

---

## 🛠 Tech Stack & Frameworks
* **Data Engine Room (Python):** `Pandas`, `NumPy`, `Scikit-Learn` (Random Forest, SVC, GridSearchCV)
* **Presentation Layer (Business Intelligence):** Power BI Desktop, DAX (Data Analysis Expressions)

---

## 📊 Machine Learning Pipeline & Architecture
A baseline Support Vector Classifier (SVC) originally recorded a high surface accuracy ($85.5\%$) by neglecting the minority class—leaving the bank exposed by missing major capital flight. 

To prioritize proactive enterprise intervention, an optimized **Balanced Random Forest Classifier** was trained using a targeted hyperparameter grid search (`GridSearchCV`).

### Operational Impact of the Models:
* **Slashed the Bank's Blind Spot:** Cut False Negatives down by more than half.
* **Class 1 Recall Boosted to 70%:** The model successfully intercepts the vast majority of active churners.
* **Continuous Feature Generation:** Extracted continuous float value arrays using `.predict_proba()` to enable proactive risk tier segmentation rather than relying on flat binary assumptions.



Predictive Risk Capital = CALCULATE([Total Assets], 'Bank_Churn'[Risk_Segmentation] = "High Risk (Red)")
