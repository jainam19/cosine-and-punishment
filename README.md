# Book Recsys Lab — Collaborative Filtering (+ SHAP for insights)

A reproducible **Python** project for a **book recommendation system**. It demonstrates **item-based** and **user-based** collaborative filtering on ratings data, optional scraping helpers, and model introspection (e.g., **SHAP** on content features if used).

---

## 1) Dataset
Bring your own data as CSVs in `data/` (see `data/README_download.md` for expected columns):  
- `ratings.csv`: `user_id, book_id, rating`  
- `books.csv`: metadata (title, authors, description, genres, etc.)  
- `reviews.csv` (optional): free-text reviews for NLP features

> Raw data is **not** committed. Use small samples to keep notebooks <5 min.

## 2) Methods (overview)
- **Item-based CF**: cosine similarity on item vectors (e.g., TF-IDF or co-occurrence).  
- **User-based CF**: neighborhood-based recommendations from user similarity.  
- **Evaluation**: holdout split with precision@k / recall@k (add as needed).  
- **Explainability (optional)**: SHAP on a content-based scorer to show why a title is recommended.

## 3) Reproduce
```bash
python -m venv .venv && .venv\Scripts\activate # Windows
# or: source .venv/bin/activate  # macOS/Linux
pip install -r requirements.txt
jupyter lab  # open notebooks/final_notebook.ipynb or item/user notebooks
```
Place data under `data/` before running. For scraping references, see `scripts/`.

## 4) Repository layout
```
/data/                      # local data only (not committed)
/figs/                      # exported plots/images
/notebooks/
  final_notebook.ipynb      # main E2E walkthrough
  item_based.ipynb          # item-based CF (optional)
  user_based.ipynb          # user-based CF (optional)
/scripts/                    # scraping helpers (reference)
/src/                        # (optional) helpers if you modularize
requirements.txt
```
## 5) Notes
- Respect website TOS and robots; scrape responsibly and minimally.
- Results depend on your data sample and evaluation protocol.
- UI (Streamlit) and metrics (P@K/R@K/MAP) can be added later if desired.
