# House Price Prediction

**Overview**

This project investigates house price prediction using regression models. It includes exploratory analysis, encoding of categorical variables, and evaluation of multiple regressors.

**Dataset**

- File: `anaconda_projects/db/HousePricePrediction.xlsx`
- Notes: The notebook drops the `Id` column and applies imputation for `SalePrice`.

**Approach**

1. EDA: inspect categorical and numeric feature distributions and correlations.
2. Drop `Id`, fill missing values and remove rows with many missing entries.
3. One-hot encode categorical variables using `OneHotEncoder` and merge encoded columns.
4. Split into training and validation sets and train models:
   - Support Vector Regression (SVR)
   - Random Forest Regressor
   - Linear Regression
5. Evaluate using Mean Absolute Percentage Error (MAPE) and other regression metrics.

**Files**

- `anaconda_projects/db/House_Price_Prediction.ipynb` — main notebook
- `anaconda_projects/db/HousePricePrediction.xlsx` — dataset

**Requirements**

- Python 3.8+
- pandas, numpy, scikit-learn, matplotlib, seaborn
- `openpyxl` or `xlrd` to read Excel files

Install with pip:

```powershell
pip install pandas numpy scikit-learn matplotlib seaborn openpyxl
```

**How to run**

1. Open the notebook file in Jupyter or VS Code.
2. Ensure `HousePricePrediction.xlsx` is present at `anaconda_projects/db`.
3. Execute cells sequentially. Training may take some time depending on model choice and machine resources.

**Notes & Suggestions**

- Consider dimensionality reduction or feature selection after one-hot encoding to reduce model complexity.
- Use hyperparameter tuning (GridSearchCV) for each model to improve results.
- Save the final model and preprocessing pipeline for reproducible inference.
