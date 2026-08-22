# Cardiac Patient Monitoring System — AI & ML Individual Project

## 1. Project Objective

A curriculum-aligned machine-learning analysis for cardiac-related patient data.
The project cleans and explores the dataset, trains and compares supervised
classification models, evaluates them with cross-validation and standard
metrics, and adds an unsupervised analysis using PCA and clustering.

## 2. Dataset

**UCI Heart Disease dataset** (Cleveland database, UCI repository ID 45).

- 303 patient records, 13 clinical features (age, sex, chest pain type,
  resting blood pressure, cholesterol, fasting blood sugar, resting ECG,
  max heart rate, exercise-induced angina, ST depression, slope, number of
  major vessels, thalassemia result).
- Target: heart disease presence/severity (0 = no disease, 1–4 = increasing
  severity), converted to a binary target (0 = no disease, 1 = disease) for
  the classification task.
- Public, non-identifiable data — loaded programmatically via the
  `ucimlrepo` package (`fetch_ucirepo(id=45)`), so no manual download is
  needed and data acquisition stays reproducible.

## 3. Project Structure

```
Cardiac-Patient-Monitoring-System/
├── data/                                    # created automatically by notebook 01
│   └── heart_disease_clean.csv
├── notebooks/
│   ├── 01_data_preparation.ipynb            # M1: load, inspect, clean
│   ├── 02_eda_statistics.ipynb              # M2: EDA & statistics
│   ├── 03_supervised_learning.ipynb         # M3+M4: baseline, comparison model, CV
│   ├── 04_feature_engineering_pipeline.ipynb# M5: feature engineering + Pipeline
│   └── 05_unsupervised_learning.ipynb       # M6: PCA & clustering
├── outputs/                                 # exported plots / result summaries (optional)
├── requirements.txt
└── README.md
```

## 4. How to Run

1. Create and activate a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks **in order**, from the `notebooks/` folder, top to bottom:
   1. `01_data_preparation.ipynb` — must be run first; it creates
      `data/heart_disease_clean.csv` that the other notebooks load.
   2. `02_eda_statistics.ipynb`
   3. `03_supervised_learning.ipynb`
   4. `04_feature_engineering_pipeline.ipynb`
   5. `05_unsupervised_learning.ipynb`

Each notebook loads the cleaned CSV independently, so once notebook 01 has
been run once, the others can be re-run individually.

## 5. Methods Summary

| Milestone | Notebook | What it does |
|---|---|---|
| M1 | 01_data_preparation | Load UCI data, inspect columns/dtypes, build a data dictionary, check missing values/duplicates/invalid values. |
| M2 | 02_eda_statistics | Descriptive statistics, distribution plots, correlation matrix, outlier review, EDA findings. |
| M3 | 03_supervised_learning | Define binary target, train/test split, baseline Logistic Regression model. |
| M4 | 03_supervised_learning | Random Forest comparison model, 5-fold cross-validation for both models, ROC-AUC for both models, side-by-side comparison. |
| M5 | 04_feature_engineering_pipeline | Engineered `bp_chol_ratio` feature; single Scikit-learn `Pipeline` (imputation + scaling/encoding + model) usable on the full, non-dropped dataset. |
| M6 | 05_unsupervised_learning | PCA (2 components), KMeans clustering with elbow-method selection of `k`, visualization, comparison of clusters vs. actual diagnosis. |

## 6. Key Findings (fill in after running)

- Baseline Logistic Regression: test accuracy **83.3%**, ROC-AUC **0.949**, 5-fold CV mean accuracy **83.2%**.
- Random Forest comparison: test accuracy **86.7%**, ROC-AUC **0.945**, 5-fold CV mean accuracy **80.5%** (higher test accuracy than the baseline, but slightly lower and more variable under cross-validation).
- Pipeline (M5) on the full 303-patient dataset (missing `ca`/`thal` imputed instead of dropped): test accuracy **85.2%**, 5-fold CV mean accuracy **85.5%** — the best and most stable result of the three, since it uses all available patients.
- PCA: the first 2 principal components explain **36%** of total feature variance. KMeans clustering (k=2, chosen via the elbow method) shows reasonable agreement with the actual diagnosis label — one cluster is mostly disease-free (151/189 patients), the other mostly disease-present (101/114 patients) — though the overlap shows the clusters don't perfectly separate the two groups.

## 7. Limitations

- Deep learning, clinical diagnosis, and production deployment are out of
  scope for this project, per the training track and project guide.
- The dataset is small (303 patients) and from a single clinical source, so
  results may not generalize to other populations.
- `ca` and `thal` contain missing values; they are handled either by
  dropping rows (M3/M4 baseline comparison) or by imputation inside the
  Scikit-learn Pipeline (M5), which is the more robust approach.
- This project is for educational purposes only and must not be used for
  real clinical decision-making.