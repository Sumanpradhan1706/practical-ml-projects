# Customer Segmentation (Unsupervised ML)

Overview
--------

This project demonstrates customer segmentation using unsupervised learning. The notebook walks through data cleaning, encoding, scaling, dimensionality reduction (t-SNE), and K-Means clustering to identify customer segments.

Dataset
-------

- Location: `07_Customer Segmentation using Unsupervised Machine Learning in Python/anaconda_projects/db/new.csv`
- Format: CSV — typical marketing/customer attributes, includes `Dt_Customer` and response-related fields.

What the notebook covers
------------------------

- Read and inspect the dataset (`new.csv`), check shapes and missing values.
- Drop or impute columns with nulls and remove noisy identifier fields (`Z_CostContact`, `Z_Revenue`, `Dt_Customer`).
- Encode categorical variables using `LabelEncoder` and scale numeric features with `StandardScaler`.
- Visualize feature distributions and correlations; use t-SNE for 2D visualization of customer structure.
- Use the elbow method (inertia) to select `k` and apply `KMeans` for segment discovery.

Quick start
-----------

1. Create and activate a Python virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install required packages:

```powershell
pip install pandas numpy scikit-learn matplotlib seaborn
```

3. Open the notebook:

- `07_Customer Segmentation using Unsupervised Machine Learning in Python/anaconda_projects/db/Customer Segmentation using Unsupervised Machine Learning in Python.ipynb`

Implementation notes
--------------------

- The notebook encodes object columns with `LabelEncoder`. For categorical features with many levels, consider one-hot encoding or target encoding as needed.
- Standard scaling is applied before clustering; this is critical for distance-based algorithms like K-Means.
- t-SNE is used for visualization, not for clustering — avoid using t-SNE output as input to KMeans for production clustering.

Suggestions & next steps
------------------------

- Evaluate clusters using silhouette score, Davies-Bouldin, or Calinski-Harabasz metrics.
- Profile clusters (average spend, demographics) and create descriptive labels (e.g., "High-value frequent buyers").
- Persist cluster assignments and integrate into downstream personalization or marketing pipelines.

Files
-----

- `anaconda_projects/db/Customer Segmentation using Unsupervised Machine Learning in Python.ipynb` — notebook
- `anaconda_projects/db/new.csv` — dataset

If you want, I can:

- (A) Add a small `segment.py` utility to run preprocessing and return cluster labels programmatically.
- (B) Add a `requirements.txt` for reproducibility.

Reply with A or B (or both) and I will proceed.