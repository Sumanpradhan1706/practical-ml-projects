# Loan Approval Prediction

**Overview**

This project predicts whether a loan application will be approved based on applicant attributes. The notebook performs data exploration, preprocessing, feature encoding, and model comparison using classical supervised learning algorithms.

**Dataset**

- File: `anaconda_projects/db/LoanApprovalPrediction.csv`
- Notes: Contains applicant demographics and loan-related fields. The `Loan_ID` column is dropped during preprocessing.

**Approach**

1. Exploratory data analysis and visualizations (categorical distributions, correlation heatmap).
2. Missing-value handling (mean imputation for numeric features).
3. Label encoding for categorical variables.
4. Train/test split and model training.
5. Models compared: RandomForest, K-Nearest Neighbours, Support Vector Classifier, Logistic Regression.
6. Evaluation: accuracy (training and test), confusion matrices and visual checks.

**Files**

- `anaconda_projects/db/Loan Approval Prediction.ipynb` — main notebook
- `anaconda_projects/db/LoanApprovalPrediction.csv` — dataset

**Requirements**

- Python 3.8+
- pandas, numpy, matplotlib, seaborn
- scikit-learn

Install with pip:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn
```

**How to run**

1. Open the notebook `anaconda_projects/db/Loan Approval Prediction.ipynb` in Jupyter or VS Code.
2. Ensure the CSV file is present at `anaconda_projects/db/LoanApprovalPrediction.csv`.
3. Run cells sequentially; training and EDA are executed in the notebook.

**Notes & Suggestions**

- Consider using stratified sampling if classes are imbalanced.
- Add cross-validation for robust model selection and hyperparameter tuning.
- For production use, export the selected model and add a small inference script.

---

*If you want, I can add a requirements file (`requirements.txt`) and a small `run_inference.py` script.*