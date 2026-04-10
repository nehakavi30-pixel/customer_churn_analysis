# 📉 Customer Churn Prediction

A supervised machine learning project predicting customer churn for a telecom company. Combines SQL-based data preparation, Python modelling, and clear visualisation to identify at-risk customers and surface actionable retention strategies.

---

## 📌 Project Overview

Customer churn is one of the most expensive problems in subscription-based businesses — acquiring a new customer costs 5–7x more than retaining an existing one. This project builds predictive models to identify which customers are likely to churn, understand *why* they churn, and translate those findings into concrete business recommendations.

---

## 🎯 Objectives

- Analyse telecom customer data to uncover churn drivers through EDA
- Build and compare classification models (Logistic Regression vs Random Forest)
- Identify the most influential features driving customer churn
- Visualise churn segments and communicate findings as retention strategy recommendations

---

## 🛠️ Tech Stack

| Library / Tool | Purpose |
|---------------|---------|
| **Python (Pandas, NumPy)** | Data wrangling and feature engineering |
| **SQL** | Data extraction and preparation |
| **scikit-learn** | Model training, evaluation, cross-validation |
| **Matplotlib / Seaborn** | EDA and results visualisation |

---

## 📂 Project Structure

```
customer_churn_analysis/
│
├── data/
│   └── telecom_churn.csv            # Source dataset
│
├── sql/
│   └── churn_data_prep.sql          # Extraction and feature queries
│
├── notebooks/
│   ├── 01_eda_churn.ipynb           # Exploratory Data Analysis
│   ├── 02_feature_engineering.ipynb # Feature prep and encoding
│   └── 03_model_comparison.ipynb    # LR vs RF training & evaluation
│
├── outputs/
│   ├── feature_importance.png       # Top churn drivers chart
│   ├── roc_curve.png                # ROC comparison plot
│   └── churn_segments.png           # Segment visualisation
│
└── README.md
```

---

## 🔍 Exploratory Data Analysis

Key patterns uncovered before modelling:

- **Month-to-month contract** customers churned at 3x the rate of annual contract holders
- Customers with **tenure < 12 months** showed the highest churn probability
- **High monthly charges** combined with low tenure = highest churn risk segment
- Customers without **tech support or online security** add-ons churned significantly more

---

## 🧠 Models Built

### Logistic Regression
- Baseline interpretable model
- Useful for understanding directional impact of each feature
- Strong performance on linearly separable patterns

### Random Forest Classifier
- Ensemble model capturing non-linear feature interactions
- Provided feature importance rankings
- Higher overall performance than Logistic Regression

---

## 📊 Results

| Metric | Logistic Regression | Random Forest |
|--------|--------------------|--------------------|
| **Accuracy** | 81% | **85%** |
| **AUC-ROC** | 0.85 | **0.88** |
| Precision (Churn) | 78% | 82% |
| Recall (Churn) | 74% | 79% |

> ✅ Random Forest outperformed on all metrics and provided interpretable feature importances for business use.

---

## 📈 Top Churn Drivers (Feature Importance)

1. 🥇 **Contract Type** — Month-to-month customers churn most
2. 🥈 **Tenure** — Newer customers are significantly higher risk
3. 🥉 **Monthly Charges** — Higher bills correlate with churn
4. **Tech Support** — Absence increases churn probability
5. **Internet Service Type** — Fibre optic users churned more than DSL

---

## 💼 Business Recommendations

Based on model outputs and churn segment analysis:

- **Target month-to-month customers** with incentives to switch to annual contracts
- **Launch an early-tenure retention programme** for customers in their first 6 months
- **Bundle tech support and security add-ons** as default for high-charge customers
- **Proactive outreach** for customers matching the high-risk segment profile

---

## 🚀 How to Run

```bash
# Clone the repository
git clone https://github.com/nehakavi30-pixel/customer_churn_analysis.git
cd customer_churn_analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Run notebooks in order
jupyter notebook notebooks/01_eda_churn.ipynb
```

---

## 👩‍💻 Author

Neha Bhan — Data Analyst | Python · SQL · Power BI
 neha.kavi30@gmail.com
🔗 [LinkedIn](https://linkedin.com/in/neha-bhan-9b45151aa) | [GitHub](https://github.com/nehakavi30-pixel)
