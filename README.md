# Customer Churn Prediction 📊

A concise, professional README for the Customer Churn Prediction project. This repository contains a dataset and two Jupyter notebooks that demonstrate regression and classification approaches for customer analytics. The README below explains the project, how to run the notebooks, required packages, and helpful notes.

---

## Overview ✨

This project explores customer churn and billing patterns using the provided `Customer-Churn-Prediction.csv`. It contains two main analyses:

- `liner_regression.ipynb` — Linear regression to predict `TotalCharges` and analyze relationships with features like `tenure` and `MonthlyCharges`. 🧮
- `logistic.ipynb` — Logistic regression for predicting customer churn (`Churn`) including handling class imbalance with SMOTE. 🔍

These notebooks include data cleaning, encoding/scaling, model training, evaluation, and visualizations.

## Repository Contents 📁

- `Customer-Churn-Prediction.csv` — Raw dataset (customer records). ✅
- `liner_regression.ipynb` — Notebook for regression analysis and evaluation. 📈
- `logistic.ipynb` — Notebook for churn classification and model evaluation. 🤖
- `README.md` — This file. 📝
- `requirements.txt` — Minimal Python package list for running the notebooks. 🧰

## Quick Highlights 🔎

- Data cleaning steps include converting `TotalCharges` to numeric and filling missing values with the median.
- Categorical variables are encoded with `LabelEncoder`, and numeric features are scaled with `MinMaxScaler` (except the regression target where appropriate).
- For the classification notebook, SMOTE is used to balance the target classes before training.

## Requirements & Setup ⚙️

Recommended: Python 3.9+ (or 3.8+). The minimal package list is provided in `requirements.txt`.

Open PowerShell and run:

```powershell
# create and activate a virtual environment (optional but recommended)
python -m venv .venv; .\.venv\Scripts\Activate.ps1

# install required packages
pip install -r "d:\New folder\requirements.txt"

# start Jupyter (or open notebooks in VS Code)
jupyter notebook
```

If you prefer installing packages manually:

```powershell
pip install pandas scikit-learn imbalanced-learn matplotlib seaborn numpy notebook
```

## How to use the notebooks ▶️

1. Open `liner_regression.ipynb` or `logistic.ipynb` in Jupyter or VS Code's Notebook editor.
2. Inspect and run cells from top to bottom. The notebooks include comments and visual outputs (plots, metrics).
3. For `logistic.ipynb`, SMOTE is applied; ensure `imblearn` (imbalanced-learn) is installed.

## Typical workflow / contract ✅

- Input: `Customer-Churn-Prediction.csv` (tabular customer data).
- Outputs: Trained models (in-notebook), evaluation metrics (R², RMSE for regression; accuracy, precision/recall/F1 for classification), and diagnostic plots.
- Error modes: Missing or malformed `TotalCharges` entries are coerced to numeric and median-imputed in the notebooks.

## Notes & Edge Cases ⚠️

- The dataset contains entries like "No internet service" and "No phone service"; the notebooks encode these consistently but you may want to create more explicit feature engineering for production models.
- `TotalCharges` sometimes loads as string — the notebooks convert it to numeric with `errors='coerce'` and fill NaNs with median.
- For larger experiments, consider using train/validation/test splits, cross-validation, and saving models to disk (joblib/pickle).

## Suggested Next Steps 🚀

- Add a reproducible `requirements.txt` (already included here) and a small `Makefile` or script to run common experiments.
- Add unit tests for data preprocessing functions if you refactor the notebooks into scripts.
- Experiment with more advanced models (XGBoost, RandomForest) and hyperparameter tuning.

## Author & License 🧾

Created for exploratory analysis and model prototyping. Feel free to reuse or adapt the notebooks for learning or prototyping purposes.

Licensed under MIT — see LICENSE (add if you want explicit license file). 🛡️

---

If you want, I can also:
- Convert the notebooks into clean, reusable Python scripts/modules.
- Add a small runner script that trains and saves models.
- Create unit tests for preprocessing steps.

Tell me which extra step you'd like next! 👍
