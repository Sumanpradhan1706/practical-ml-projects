# Box Office Revenue Prediction

**Overview**

This project predicts domestic box office revenue using structured movie metadata and text-derived features. It includes preprocessing, feature engineering, and training a gradient-boosted regressor (XGBoost).

**Dataset**

- File: `anaconda_projects/db/boxoffice.csv`
- Notes: The notebook cleans numeric columns (removing symbols and commas), converts `genres` to bag-of-words features using `CountVectorizer`, and drops columns with excessive missing values.

**Approach**

1. Data cleaning: remove `world_revenue` and `opening_revenue`, handle missing values, convert currency strings to numeric.
2. Feature engineering: tokenize `genres` using `CountVectorizer`, one-hot encoding of frequent genres, and label encoding for `distributor` and `MPAA`.
3. Transform target variables (log transform for revenue features), standardize features with `StandardScaler`.
4. Train `XGBRegressor` and evaluate with mean absolute error (MAE).

**Files**

- `anaconda_projects/db/Box Office Revenue Prediction.ipynb` — main notebook
- `anaconda_projects/db/boxoffice.csv` — dataset

**Requirements**

- Python 3.8+
- pandas, numpy, matplotlib, seaborn
- scikit-learn, xgboost

Install with pip:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```

**How to run**

1. Open the notebook in Jupyter or VS Code.
2. Ensure `boxoffice.csv` is present in `anaconda_projects/db`.
3. Run cells step-by-step; training uses XGBoost which benefits from a machine with multiple cores.

**Notes & Suggestions**

- Consider hyperparameter tuning (GridSearchCV / randomized search) for XGBoost.
- Persist the trained model and preprocessing objects (scaler, vectorizer) for reproducible inference.
- If available, expand features (e.g., cast, crew, seasonality) to improve predictive power.
