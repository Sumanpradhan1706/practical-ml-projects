# Credit Card Fraud Detection

Overview
--------

Detect fraudulent credit card transactions using supervised learning. This notebook demonstrates EDA for imbalanced data, a RandomForest baseline, and comprehensive evaluation (precision, recall, F1, MCC).

Dataset
-------

- Expected location: `anaconda_projects/db/creditcard.csv` (commonly obtained from Kaggle's "Credit Card Fraud Detection" dataset).
- Note: This dataset is large and may be excluded from the repository. Download and place locally to run the notebook.

Workflow
--------

- Load and inspect the dataset; visualize class imbalance and amounts.
- Separate features and labels, split into train/test sets.
- Train a `RandomForestClassifier` baseline and compute predictions on the test set.
- Evaluate using accuracy, precision, recall, F1-score, Matthews correlation coefficient, and confusion matrix visualization.

Quick start
-----------

1. Download `creditcard.csv` from a public source (for example, Kaggle) and place it in:

```
04_Credit_Card_Fraud_Detection\anaconda_projects\db\creditcard.csv
```

2. Create a virtual environment and install dependencies:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Open `anaconda_projects/db/Credit Card Fraud Detection.ipynb` and run cells.

Notes & improvements
------------------

- Strong class imbalance requires careful metric selection; consider using precision-recall curves and ROC AUC.
- Try resampling strategies (SMOTE/undersampling) or tree-based gradient boosters (XGBoost / LightGBM) for improved performance.
- If you plan to keep the dataset under version control, use Git LFS to avoid exceeding GitHub limits.

Files
-----

- `anaconda_projects/db/Credit Card Fraud Detection.ipynb` (notebook)
