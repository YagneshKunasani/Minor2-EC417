# Data
- Dataset and version: IBM Telco Customer Churn (Standard Kaggle Version)
- Official source URL: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- Access date: November 2026
- License / terms: Database Contents License (DbCL) / Kaggle Terms of Use
- Required citation: IBM Sample Datasets
- Files used: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Download/preparation command: `python download.py` (uses Kaggle API)
- Preprocessing and filtering: Dropped `customerID`. Converted `TotalCharges` from text to numeric, coercing errors to NaN and filling resulting blanks (new customers with 0 tenure) with 0.
- Label mapping: `Churn` mapped from {'Yes': 1, 'No': 0}
- Train/validation/test split: 80% Train / 20% Test split (stratified on target `Churn`). Hyperparameter tuning performed using 3-fold cross-validation on the training set only.
- Random seed(s): `42` used for train/test split, model initialization, and randomized search.
- Known limitations, leakage risks, privacy concerns: `Tenure` and `TotalCharges` are heavily collinear. 

To reproduce:
1. `pip install -r requirements.txt`
2. `python download.py`
3. Run `python main.py` as documented in the project README.