# ACIS Insurance Risk Analytics & Predictive Modeling

## Project Overview
AlphaCare Insurance Solutions (ACIS) aims to optimize car insurance marketing by identifying low-risk segments and tailoring premiums to attract new clients. This project leverages historical insurance claim data to uncover patterns in risk, profitability, and to build predictive models for risk-based pricing.

## Objectives
- **Task 1:** Understand, clean, and explore the dataset to identify trends, outliers, and key risk factors.
- **Task 2:** Ensure the cleaned dataset is version-controlled, reproducible, and auditable using Data Version Control (DVC).
- **Task 3:** Statistically validate or reject key hypotheses about risk drivers to guide segmentation strategy.
- **Task 4:** Build and evaluate predictive models to estimate claim severity and optimize premiums using machine learning.

## Project Scope & Deliverables
- **Exploratory Data Analysis (EDA):**
  - Numeric and categorical distributions
  - Temporal trends
  - Outlier detection
- **Feature Engineering:**
  - Loss Ratio = TotalClaims / TotalPremium
- **Data Versioning:**
  - DVC-tracked cleaned dataset
- **Hypothesis Testing (Task 3):**
  - Risk differences across provinces
  - Vehicle & policy characteristics
  - Gender impact
  - Margin analysis
- **Predictive Modeling (Task 4):**
  - Claim severity regression models (Linear Regression, Random Forest)
  - Claim probability classification model
  - Evaluation metrics: RMSE, R², ROC-AUC, precision, recall, F1-score
  - Feature importance & interpretability with SHAP / LIME
- **Insights for Business Decisions:**
  - Geographic and vehicle-based risk segmentation
  - Targeted pricing strategies
  - Risk-based premium adjustments

## Tech Stack
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- Scipy, Statsmodels
- Scikit-learn, XGBoost
- SHAP / LIME for model interpretability
- DVC for data versioning
- Git & GitHub for code version control

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/yourusername/Insurance_Risk_Analytics.git
cd Insurance_Risk_Analytics
Create a Python environment and install dependencies:

conda create -n acis_env python=3.12
conda activate acis_env
pip install -r requirements.txt
```

Run notebooks sequentially for each task:

notebooks/task1_eda.ipynb – EDA and data cleaning

notebooks/task2_dvc.ipynb – Data versioning with DVC

notebooks/task3_hypothesis_testing.ipynb – Statistical testing and segmentation

notebooks/task4_predictive_modeling.ipynb – Modeling and evaluation

## Key Insights

Task 1 & 2: Dataset cleaned, missing values handled, features engineered, and versioned. Outliers and skewed distributions addressed. Temporal trends and Loss Ratio variability identified segmentation opportunities.

Task 3:

Geographic Risk Differences: Significant variation exists across provinces; a major factor for segmentation.

Vehicle & Policy Characteristics: Loss ratios vary by vehicle type, guiding vehicle-specific premium adjustments.

Gender Impact: Not statistically significant; premium adjustments based on gender not warranted.

Margin Analysis: Provinces with higher claim frequency and severity show lower margins, guiding targeted pricing strategies.

Task 4:

Claim severity model (Random Forest) outperformed Linear Regression: RMSE ~29,773, R² ~0.11.

Claim probability model achieved ROC-AUC ~0.76 with balanced precision/recall considerations.

Feature importance (via SHAP) highlighted vehicle type, coverage, and vehicle age as key risk drivers.

## Folder Structure
```bash
ACIS_Insurance_Risk_Analytics/
├── data/
│   ├── raw/         # Raw datasets (untracked in Git)
│   ├── processed/   # Cleaned and DVC-tracked datasets
├── notebooks/       # Jupyter notebooks for each task
├── src/             # Optional scripts for modular code
├── dvc.yaml         # DVC pipeline file
├── requirements.txt
└── README.md
```
## Future Work

Incorporate more granular geographic and demographic features for enhanced segmentation.

Deploy predictive models in a dynamic, risk-based pricing framework.

Extend modeling to include multi-year claim predictions and portfolio-level risk simulation.
