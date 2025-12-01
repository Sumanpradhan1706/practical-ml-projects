# Loan Approval Prediction

Overview
--------

Predict whether a loan application will be approved using applicant attributes. This project demonstrates a concise EDA → preprocessing → modeling workflow and compares several classical classifiers.

Dataset
-------

- Location: `anaconda_projects/db/LoanApprovalPrediction.csv`
- Notes: Typical loan-application attributes; `Loan_ID` is removed during preprocessing in the notebook.

What this notebook does
----------------------

- Exploratory data analysis and visualizations (categorical distributions, correlation heatmap).
- Handle missing values (mean imputation for numeric features).
- Encode categorical variables (LabelEncoder).
- Train/test split and train baseline models (RandomForest, KNN, SVC, LogisticRegression).
- Evaluate using accuracy and confusion matrices.

Quick start
-----------

1. Create and activate a Python environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install minimal dependencies:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Open `anaconda_projects/db/Loan Approval Prediction.ipynb` and run cells.

Notes & next steps
------------------

- Use stratified sampling or cross-validation to handle class imbalance and obtain robust scores.
- For deployment, save the trained pipeline (preprocessing + model) with `joblib` and add a small inference script.
- I can generate a `requirements.txt` or an inference script on request.

Files
-----

- `anaconda_projects/db/Loan Approval Prediction.ipynb` (notebook)
- `anaconda_projects/db/LoanApprovalPrediction.csv` (dataset)