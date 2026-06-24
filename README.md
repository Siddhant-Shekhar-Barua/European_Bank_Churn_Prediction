# Bank Customer Retention: End-to-End Predictive ML & BI Solution

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

---

## 📈 Power BI Strategic Dashboard Layout
The data pipeline exports an enriched dataset featuring predictive features (`Churn_Probability` and `Risk_Segmentation`) directly into an optimized 3-Page Power BI layout:

### Page 1: The Executive Portfolio Dashboard
* Monitors the macro-level health of the bank’s total managed asset base.
* Visualizes portfolio capital division across custom risk tiers using dynamic DAX measures.

### Page 2: The Historical Diagnostic Layer
* Performs an operational "autopsy" on past losses (`Exited = 1`).
* Uncovers critical business anomalies, including a near-100% historical churn rate spike among customers holding 3 or 4 products.

### Page 3: The Front-Line Tactical Action Plan
* A searchable operational workspace built explicitly for account relationship managers.
* Uses conditional formatting traffic lights and quadrant analysis to route retention calls to high-value, high-risk accounts first.

---

## 💡 Key Core DAX Metrics Implemented
```dax
Total Assets = SUM('Bank_Churn'[Balance])

Historical Churn Capital = CALCULATE([Total Assets], 'Bank_Churn'[Exited] = 1)

Predictive Risk Capital = CALCULATE([Total Assets], 'Bank_Churn'[Risk_Segmentation] = "High Risk (Red)")
