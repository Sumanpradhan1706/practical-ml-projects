# Box Office Revenue Prediction

Overview
--------

Predict domestic box office revenue using movie metadata and derived text features. The notebook focuses on careful data cleaning, feature engineering from `genres`, and training an XGBoost regressor.

Dataset
-------

- Location: `anaconda_projects/db/boxoffice.csv`
- Notes: The notebook strips currency symbols and commas, converts `genres` into bag-of-words features via `CountVectorizer`, and drops low-quality columns.

Workflow
--------

- Clean numeric columns and coerce types (remove symbols, handle commas).
- Fill or drop missing data where appropriate.
- Convert `genres` into token features with `CountVectorizer` and encode categorical metadata.
- Standardize numeric features and train an `XGBRegressor`.
- Evaluate using MAE and other regression metrics.

Quick start
-----------

1. Create and activate a virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install dependencies:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

3. Open `anaconda_projects/db/Box Office Revenue Prediction.ipynb` and run cells.

Notes & improvements
-------------------

- Consider hyperparameter tuning (GridSearchCV / RandomizedSearchCV) for XGBoost to improve performance.
- Persist the trained model and preprocessing objects (scaler, vectorizer) for reproducible inference.
- If more metadata is available (cast, crew, seasonality), add features to expand predictive power.

Files
-----

- `anaconda_projects/db/Box Office Revenue Prediction.ipynb` (notebook)
- `anaconda_projects/db/boxoffice.csv` (dataset)
