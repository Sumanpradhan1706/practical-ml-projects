# Practical ML Projects

**Overview**

This repository contains five small-to-medium end-to-end machine learning projects created for learning and demonstration purposes. Each project includes a Jupyter notebook with exploratory data analysis, preprocessing, model training, and evaluation. Projects are organized into separate folders so you can open, run, and adapt them independently.

**Projects**

- **01_Loan Approval Prediction** — Predict whether a loan application will be approved. The notebook demonstrates EDA, label encoding, missing-value handling, and compares several classifiers (Random Forest, KNN, SVC, Logistic Regression).
  - Location: `01_Loan Approval Prediction`
  - Notebook: `01_Loan Approval Prediction/anaconda_projects/db/Loan Approval Prediction.ipynb`

- **02_Heart Disease Prediction Using Logistic Regression** — Build a logistic regression classifier to predict 10-year risk of coronary heart disease using clinical features. Includes scaling, train/test split, evaluation and confusion matrix.
  - Location: `02_Heart Disease Prediction Using Logistic Regression`
  - Notebook: `02_Heart Disease Prediction Using Logistic Regression/anaconda_projects/db/Heart Disease Prediction Using Logistic Regression.ipynb`

- **03_House_Price_Prediction** — Regression task predicting house sale prices. The notebook includes one-hot encoding of categorical features, model comparison (SVR, Random Forest, Linear Regression), and MAPE evaluation.
  - Location: `03_House_Price_Prediction`
  - Notebook: `03_House_Price_Prediction/anaconda_projects/db/House_Price_Prediction.ipynb`

- **04_Credit_Card_Fraud_Detection** — Detect fraudulent credit card transactions. Shows EDA, class imbalance handling, trains a RandomForestClassifier, and reports precision/recall/F1/MCC with confusion matrix. NOTE: the original `creditcard.csv` is large and may be excluded from this repository.
  - Location: `04_Credit_Card_Fraud_Detection`
  - Notebook: `04_Credit_Card_Fraud_Detection/anaconda_projects/db/Credit Card Fraud Detection.ipynb`

- **05_Box Office Revenue Prediction** — Predicts domestic box office revenue using structured metadata and bag-of-words features from genres. Uses XGBoost for regression after thorough preprocessing and feature engineering.
  - Location: `05_Box Office Revenue Prediction`
  - Notebook: `05_Box Office Revenue Prediction/anaconda_projects/db/Box Office Revenue Prediction.ipynb`

**Quick Start**

1. Clone or open the repository in VS Code / Jupyter Lab.

```powershell
# Example: clone the repo (if not already cloned)
git clone https://github.com/Sumanpradhan1706/practical-ml-projects.git
cd "practical-ml-projects"
```

2. (Recommended) Create and activate a Python environment, then install required packages.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

If you prefer to install only common packages used across projects:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn xgboost openpyxl
```

3. Open any project's notebook in Jupyter or VS Code and run cells sequentially.

**Data & Large Files**

- Small datasets are included in their respective `anaconda_projects/db/` folders (e.g., `LoanApprovalPrediction.csv`, `framingham.csv`, `HousePricePrediction.xlsx`, `boxoffice.csv`).
- The `creditcard.csv` dataset used by the credit-card fraud project is large and may be intentionally excluded from version control to keep the repository lightweight. If you need it, download from a public source (for example the Kaggle dataset) and place it at:

```
04_Credit_Card_Fraud_Detection\anaconda_projects\db\creditcard.csv
```

- If you want large datasets tracked by the repo, consider enabling Git LFS and migrating them (`git lfs install` / `git lfs track \"path\"`).

**Recommended Workflow**

- Keep datasets out of Git when they exceed size limits. Instead: store locally, use cloud storage, or use Git LFS for tracked large files.
- Use `requirements.txt` per project to pin reproducible environments. I can generate these for each project on request.
- When editing notebooks, clear output before committing to keep repository size small.

**Contributing**

Contributions are welcome. Suggested workflow:

- Create a branch for your change: `git checkout -b feat/your-change`
- Run and validate notebooks locally.
- Open a Pull Request describing your improvements.

If you want me to: I can add per-project `requirements.txt`, small inference scripts, or CI hooks to validate notebooks automatically.

**Contact & License**

- Author: Suman Pradhan
- Repository: `practical-ml-projects`

License: add an open-source license file if you want this repo publicly reusable (MIT, Apache-2.0, etc.).

---

If you'd like, I can now:
- (A) Generate per-project `requirements.txt` files, or
- (B) Add a small `scripts/` folder with `run_notebook.ps1` helpers, or
- (C) Configure Git LFS and migrate selected large files (e.g., `creditcard.csv`).

Tell me which and I will proceed.