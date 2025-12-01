# House Price Prediction

Overview
--------

Predict house sale prices using structured features and categorical encoding. The notebook demonstrates preprocessing, one-hot encoding, and evaluation of multiple regression models.

Dataset
-------

- Location: `anaconda_projects/db/HousePricePrediction.xlsx`
- Notes: `Id` column is removed; `SalePrice` missing values are imputed in the notebook.

Workflow
--------

- Inspect numeric and categorical features; visualize correlations and distributions.
- Drop identifier columns and handle missing values via imputation or row removal.
- One-hot encode categorical features using `OneHotEncoder` and assemble final feature matrix.
- Train and compare SVR, RandomForestRegressor, and LinearRegression models.
- Evaluate using Mean Absolute Percentage Error (MAPE) and similar metrics.

Quick start
-----------

1. Create and activate a virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
```

3. Open `anaconda_projects/db/House_Price_Prediction.ipynb` and run cells.

Notes & improvements
-------------------

- After one-hot encoding, consider dimensionality reduction (PCA) or feature selection to reduce model size.
- Use hyperparameter search (GridSearchCV/RandomizedSearchCV) to tune models.
- Persist the best model and preprocessing pipeline for deployment.

Files
-----

- `anaconda_projects/db/House_Price_Prediction.ipynb` (notebook)
- `anaconda_projects/db/HousePricePrediction.xlsx` (dataset)
