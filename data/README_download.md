# Data placement

This repo does **not** commit raw data. Place your prepared CSVs here, e.g.:
- `data/books.csv` — catalog with `book_id,title,authors,description,...`
- `data/ratings.csv` — user-item interactions `user_id,book_id,rating`
- `data/reviews.csv` — (optional) text reviews if doing NLP/SHAP feature work

### Option A — Use your existing files
Copy your exported CSVs into `data/` with the names above.

### Option B — Minimal sample (quick demo)
Create small CSVs (e.g., 1–5k interactions) to run notebooks fast. You can filter your full data by a subset of popular books/users.

### Option C — Scrape (small) via scripts
See `scripts/get_books.py` and `scripts/get_reviews.py` for reference. **Scrape responsibly**: follow robots/TOS, rate-limit, and only for personal/educational use.