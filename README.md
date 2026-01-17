# Donor Income Classifier

Predict whether a person earns more than **$50K/year** using census-like demographic data.

This is a repository packaging of a Udacity-style supervised learning project: it keeps the core analysis, but makes the work easy to review and easy to run.

## Quick links

- Notebook: `notebooks/finding_donors.ipynb`
- HTML report (easy to read in GitHub): `notebooks/finding_donors.html`
- Udacity fork archive (for original context): [https://github.com/andigles/udacity-finding-donors-archive](https://github.com/andigles/udacity-finding-donors-archive)

## Results

Replace the placeholders below with your final numbers.

| Model | What it represents | Metric (fill with Accuracy / F1 / etc.) |
| --- | --- | --- |
| Naive baseline | Simple baseline to set a minimum bar | TODO |
| Model A | First trained model (e.g., Logistic Regression) | TODO |
| Model B | Second trained model (e.g., Random Forest) | TODO |
| Best model | Best-performing model after tuning | **TODO** |

Notes:

- If you report more than one metric (for example Accuracy and F1 score), add more columns.
- If the dataset is imbalanced, F1 score is often more informative than Accuracy.

## How to run

### Option 1: Windows + Git Bash (recommended)

```bash
python -m venv .venv
source .venv/Scripts/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter lab
```

Then open:

- `notebooks/finding_donors.ipynb`

### Option 2: macOS / Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter lab
```

## Re-create the HTML report

If you want to regenerate the HTML version from the notebook:

```bash
jupyter nbconvert --to html notebooks/finding_donors.ipynb --output finding_donors.html
```

## Repository layout

- `notebooks/` — notebook + exported HTML report
- `src/` — optional reusable code (preprocessing, training, evaluation)
- `reports/figures/` — saved plots used in the README/report
- `data/` — dataset notes (and download instructions if you do not commit raw data)

## Data

- If you **do not** include the raw dataset in the repo, add a short explanation in `data/README.md` describing where the data comes from and how to obtain it.
- If you **do** include data, keep it small and make sure you are allowed to distribute it.

## Next improvements

Pick a few that match your goals (do not do everything).

- Add a small script (for example `src/train.py`) to train/evaluate from the command line.
- Add basic tests for preprocessing (for example checking missing values handling).
- Add CI (continuous integration) with GitHub Actions to verify `pip install -r requirements.txt` works.
- Add a short “model card” section: what the model is good at, what it struggles with, and risks.

## Attribution

This project is based on a supervised learning project concept used in Udacity coursework.

- Analysis, packaging, and repository structure: **Andrés**
- Original course context and starter materials: Udacity (see the archived fork linked above)
