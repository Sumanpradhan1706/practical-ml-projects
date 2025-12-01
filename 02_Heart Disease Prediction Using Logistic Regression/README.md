# Heart Disease Prediction (Logistic Regression)

Overview
--------

Predict 10-year coronary heart disease (CHD) risk using clinical features. The notebook focuses on standard preprocessing, scaling, logistic regression modeling, and evaluation with classification metrics.

Dataset
-------

- Location: `anaconda_projects/db/framingham.csv`
- Notes: The notebook removes the `education` column and renames the `male` field to `Sex_male` for clarity.

Workflow
--------

- Clean data and drop incomplete records.
- Select predictive features: `age`, `Sex_male`, `cigsPerDay`, `totChol`, `sysBP`, `glucose`.
- Scale numeric features with `StandardScaler`.
- Train a `LogisticRegression` baseline and evaluate using accuracy, classification report, and a confusion matrix.

Quick start
-----------

1. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn
```

3. Open `anaconda_projects/db/Heart Disease Prediction Using Logistic Regression.ipynb` and run cells.

Notes & improvements
-------------------

- Try regularization and hyperparameter tuning to reduce overfitting.
- Use stratified cross-validation to account for class imbalance.
- Save the final model with `joblib` and add a small inference script for deployment.

Files
-----

- `anaconda_projects/db/Heart Disease Prediction Using Logistic Regression.ipynb` (notebook)
- `anaconda_projects/db/framingham.csv` (dataset)
