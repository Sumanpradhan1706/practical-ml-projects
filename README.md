# Practical ML Projects

> A curated collection of five practical, end-to-end machine learning demos. Each project is self-contained, reproducible, and designed for rapid experimentation and learning.

---

## Table of contents

- [Project overview](#project-overview)
- [Quick start](#quick-start)
- [Project summaries](#project-summaries)
- [Data & large files](#data--large-files)
- [Environment & reproducibility](#environment--reproducibility)
- [Recommended workflow](#recommended-workflow)
- [Contributing](#contributing)
- [Contact & license](#contact--license)

---

## Project overview

This repository contains five focused machine-learning projects with notebooks that cover data exploration, preprocessing, feature engineering, modeling, and evaluation. Projects are organized so you can run a single notebook end-to-end or extend components into production-ready pipelines.

Folder list:

- `01_Loan Approval Prediction`
- `02_Heart Disease Prediction Using Logistic Regression`
- `03_House_Price_Prediction`
- `04_Credit_Card_Fraud_Detection`
- `05_Box Office Revenue Prediction`

---

## Quick start

1. Clone the repository:

```powershell
git clone https://github.com/Sumanpradhan1706/practical-ml-projects.git
cd "practical-ml-projects"
```

2. Create and activate a Python virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

3. Install core dependencies used across projects (or use per-project `requirements.txt` if present):

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl
```

4. Open a project's notebook in Jupyter or VS Code and run cells sequentially.

---

## Project summaries

### 01 — Loan Approval Prediction
- Notebook: `01_Loan Approval Prediction/anaconda_projects/db/Loan Approval Prediction.ipynb`
- Summary: Classification of loan approval outcomes. Demonstrates EDA, label encoding, imputation, and baseline comparison across RandomForest, KNN, SVC, and Logistic Regression.

### 02 — Heart Disease Prediction (Logistic Regression)
- Notebook: `02_Heart Disease Prediction Using Logistic Regression/anaconda_projects/db/Heart Disease Prediction Using Logistic Regression.ipynb`
- Summary: Predict 10-year CHD risk with clinical features. Shows standard scaling, train/test split, logistic regression baseline, and confusion-matrix analysis.

### 03 — House Price Prediction
- Notebook: `03_House_Price_Prediction/anaconda_projects/db/House_Price_Prediction.ipynb`
- Summary: Regression pipeline including one-hot encoding, model comparison (SVR, RandomForest, Linear Regression), and evaluation with MAPE.

### 04 — Credit Card Fraud Detection
- Notebook: `04_Credit_Card_Fraud_Detection/anaconda_projects/db/Credit Card Fraud Detection.ipynb`
- Summary: Fraud detection on transactional data. Includes EDA for imbalanced classes, RandomForest baseline, and evaluation with precision/recall/F1 and MCC.

### 05 — Box Office Revenue Prediction
- Notebook: `05_Box Office Revenue Prediction/anaconda_projects/db/Box Office Revenue Prediction.ipynb`
- Summary: Predicts domestic revenue using structured features and text-derived genre features (CountVectorizer) with XGBoost regression.

---

## Data & large files

- Small datasets are stored in each project's `anaconda_projects/db/` directory (for example: `LoanApprovalPrediction.csv`, `framingham.csv`, `HousePricePrediction.xlsx`, `boxoffice.csv`).
- The `creditcard.csv` dataset is large and may not be included in the repository to keep the repo lightweight. To run the fraud notebook, download the dataset (for example from Kaggle) and place it at:

```
04_Credit_Card_Fraud_Detection\anaconda_projects\db\creditcard.csv
```

- To track large files in Git, use Git LFS. Example:

```powershell
git lfs install
git lfs track "04_Credit_Card_Fraud_Detection/anaconda_projects/db/creditcard.csv"
```

---

## Environment & reproducibility

- Use virtual environments (venv or conda) and pin dependencies with `requirements.txt` or `environment.yml` for reproducibility.
- I can generate per-project `requirements.txt` files on request.

Example (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r "01_Loan Approval Prediction/requirements.txt"
```

---

## Recommended workflow

- Keep large datasets out of Git history. Use cloud storage, shared drives, or Git LFS.
- Clear notebook outputs before committing to reduce repository size.
- Work in feature branches and open small pull requests for review.

---

## Contributing

Contributions are welcome. Suggested flow:

1. Fork the repository and create a feature branch: `git checkout -b feat/your-change`
2. Run and validate notebooks locally.
3. Open a Pull Request with a clear description and any results or evaluation metrics.

If you want, I can add CI that validates notebooks and runs lightweight tests.

---

## Contact & license

- Author: Suman Pradhan
- Repo: `practical-ml-projects`

If you want the repository to be publicly reusable, add a license file (MIT or Apache-2.0 are common choices). I can add an appropriate `LICENSE` file for you.

---

## Next steps I can take

- (A) Generate `requirements.txt` files for each project.
- (B) Add `scripts/` helpers (for example `run_notebook.ps1`) to open notebooks in a clean environment.
- (C) Configure Git LFS and migrate large datasets (e.g., `creditcard.csv`).

Reply with the option letter(s) you prefer and I'll proceed.
