# Heart Disease Prediction (Logistic Regression)

**Overview**

This project builds a logistic regression model to predict 10-year risk of coronary heart disease using a subset of clinical features. The notebook focuses on preprocessing, feature selection, model training, and evaluation.

**Dataset**

- File: `anaconda_projects/db/framingham.csv`
- Notes: Standard cardiovascular risk dataset; the `education` column is removed in the notebook and `male` is renamed to `Sex_male`.

**Approach**

1. Data cleaning (dropna to remove incomplete records).
2. Feature selection for model inputs: `age`, `Sex_male`, `cigsPerDay`, `totChol`, `sysBP`, `glucose`.
3. Scaling using `StandardScaler` and splitting into train/test sets.
4. Train logistic regression classifier.
5. Evaluate with accuracy, classification report, confusion matrix and visualizations.

**Files**

- `anaconda_projects/db/Heart Disease Prediction Using Logistic Regression.ipynb` — main notebook
- `anaconda_projects/db/framingham.csv` — dataset

**Requirements**

- Python 3.8+
- pandas, numpy, matplotlib, seaborn
- scikit-learn

Install with pip:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn
```

**How to run**

1. Open the notebook in Jupyter or VS Code.
2. Confirm `framingham.csv` is present under `anaconda_projects/db`.
3. Run the notebook cells in order to reproduce preprocessing, model training, and evaluation.

**Notes & Suggestions**

- Consider exploring additional features and regularization to improve generalization.
- Use stratified cross-validation for stable performance estimates when class imbalance exists.
- Add model persistence (joblib) and a minimal inference example if you want to deploy the model.
