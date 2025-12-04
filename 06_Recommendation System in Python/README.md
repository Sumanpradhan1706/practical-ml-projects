# Recommendation System in Python

Overview
--------

A compact recommendation-system demo that builds item-based recommendations from a movie ratings dataset. The notebook implements a sparse user–item representation and a cosine-based nearest-neighbors retrieval to recommend movies similar to a given title.

Dataset
-------

- Location: `06_Recommendation System in Python/anaconda_projects/db/ratings.csv`
- Format: CSV — columns include `userId`, `movieId`, `title`, `rating`.

What the notebook covers
------------------------

- Load short movie-rating dataset and inspect distributions.
- Construct a sparse item-by-user matrix (CSR) suitable for nearest-neighbors search.
- Fit a cosine-similarity NearestNeighbors model and retrieve top-K similar movies for a given title.
- Example function: `recommend_similar(movie_title, df, X, movie_mapper, movie_inv_mapper, k=5)` returns titles similar to `movie_title`.

Quick start
-----------

1. Create and activate a Python virtual environment (PowerShell):

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

2. Install minimal dependencies:

```powershell
pip install pandas numpy scipy scikit-learn matplotlib seaborn
```

3. Open and run the notebook:

- `06_Recommendation System in Python/anaconda_projects/db/Recommendation System in Python.ipynb`

Implementation notes
--------------------

- The demo uses `scipy.sparse.csr_matrix` for memory-efficient storage and `sklearn.neighbors.NearestNeighbors` with `metric='cosine'` for similarity search.
- The function maps `movieId` ↔ index and returns neighbor movie titles by looking up `movieId` values.
- Because recommendations are computed from co-occurrence in a small dataset, results are illustrative; use larger datasets and SVD/ALS for production systems.

Suggestions & next steps
------------------------

- Replace nearest-neighbors with matrix factorization (SVD, ALS) for scalable latent-factor recommendations.
- Add item metadata (genres, year) and implement hybrid recommenders that combine content and collaborative signals.
- Persist mappings and the fitted nearest-neighbors model for fast inference.

Files
-----

- `anaconda_projects/db/Recommendation System in Python.ipynb` — notebook
- `anaconda_projects/db/ratings.csv` — dataset

If you want, I can:

- (A) Add a small `recommend.py` module wrapping the recommendation functions for programmatic use.
- (B) Add a `requirements.txt` or a `scripts/` helper to run the notebook.

Reply with A or B (or both) and I will proceed.