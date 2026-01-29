# Finding Donors (Income Prediction) — Case Study

[![CI](https://github.com/andigles/finding-donors-ml/actions/workflows/ci.yml/badge.svg?branch=main)](https://github.com/andigles/finding-donors-ml/actions/workflows/ci.yml)

Predict whether an individual earns **more than $50K/year** using census-like demographic data.  
This is a **supervised learning** case study focused on **model comparison**, **hyperparameter tuning**, and **explaining results clearly**.

**Best place to start:**

- 📘 Notebook: `notebooks/finding_donors.ipynb`
- 🌐 HTML report (easy to read in GitHub): `docs/finding_donors.html`

**Read the report (HTML):** 

[finding_donors.html](https://github.com/andigles/finding-donors-ml/blob/main/docs/finding_donors.html)

---

## Results summary

This project prioritizes **F0.5** (F-beta score with beta=0.5), which weighs **precision** more than recall.

### Model comparison (test set, 100% training data)

| Model | F0.5 (Test) | Training Time (s) | Prediction Time (s) |
| --- | ---: | ---: | ---: |
| Logistic Regression | 0.683 | 0.539 | 0.009 |
| Random Forest | 0.680 | 4.626 | 0.245 |
| AdaBoost | 0.703 | 1.966 | 0.162 |

**Selected approach:** AdaBoost (tuned) for best F0.5 with reasonable training time.

> Tip: The notebook contains the full baseline comparison, tuning details, and interpretation.

---

## How to run

### 1) Create and activate an environment (Windows + Git Bash)

From the repo root:

```bash
python -m venv .venv
source .venv/Scripts/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### 2) Add the dataset

This project expects:

- `data/census.csv`

The repo does **not** include the dataset file. See `data/README.md` for instructions.

### 3) Launch Jupyter

```bash
jupyter lab
```

Open:

- `notebooks/finding_donors.ipynb`

(Optional) Export HTML:

```bash
jupyter nbconvert --to html notebooks/finding_donors.ipynb --output docs/finding_donors.html
```

---

## Repository structure

- `notebooks/`
  - `finding_donors.ipynb` — main case study notebook
  - `finding_donors.html` — exported report for quick reading
- `src/`
  - `visuals.py` — helper plotting/visual utilities used by the notebook
- `data/`
  - `README.md` — where to place `census.csv` and how to obtain it
- `reports/figures/`
  - optional saved figures for README/report

---

## Notes and next steps

If extending this beyond a notebook:

- Add threshold tuning (choose a decision threshold that matches outreach cost)
- Add probability calibration (more reliable confidence scores)
- Add fairness/bias checks across groups
- Package preprocessing + training into reusable `src/` modules
- Add automated checks (GitHub Actions) for install + basic imports

---

## Attribution

This project is based on the *Finding Donors* supervised learning project concept from Udacity.  
Implementation, analysis, and packaging in this repository were done by **Andrés**.

---

## License

See `LICENSE`.
