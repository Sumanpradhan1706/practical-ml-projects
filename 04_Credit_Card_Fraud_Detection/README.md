# Credit Card Fraud Detection

**Overview**

This project detects fraudulent credit card transactions using machine learning. The notebook focuses on data exploration, handling extreme class imbalance, training a classifier, and evaluating multiple metrics suited for imbalanced classification.

**Dataset**

- Notebook expects: `anaconda_projects/db/creditcard.csv` (commonly available from Kaggle — NOT included in this repository due to size limits).
- If `creditcard.csv` is not present, download from a public source (for example, the Kaggle "Credit Card Fraud Detection" dataset) and place it at `anaconda_projects/db/creditcard.csv`.

**Approach**

1. EDA and correlation analysis.
2. Train-test split and feature/label separation.
3. Train a `RandomForestClassifier` and predict on the test set.
4. Evaluation with accuracy, precision, recall, F1-score, Matthews correlation coefficient, and confusion matrix visualization.

**Files**

- `anaconda_projects/db/Credit Card Fraud Detection.ipynb` — main notebook

**Requirements**

- Python 3.8+
- pandas, numpy, matplotlib, seaborn
- scikit-learn

Install with pip:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn
```

**How to run**

1. Download `creditcard.csv` (if not present) and save it to `anaconda_projects/db/`.
2. Open the notebook and run cells sequentially.

**Notes & Suggestions**

- The original dataset file was large and excluded from the main branch to keep the repository lightweight. If you want this dataset tracked by the repo, I recommend using Git LFS.
- Consider sampling strategies and specialized algorithms (e.g., XGBoost, LightGBM) or resampling (SMOTE) for improved performance on imbalanced data.
- Add a small `data/` README describing the dataset source and licensing if you plan to keep the dataset externally.
