# Data Dictionary — UCI Heart Disease Dataset

Source: UCI Machine Learning Repository, Heart Disease dataset (Cleveland
database), ID 45. Loaded via `ucimlrepo.fetch_ucirepo(id=45)`.

| Feature | Type | Meaning | Notes |
|---|---|---|---|
| `age` | numeric | Age in years | |
| `sex` | categorical | Sex (1 = male, 0 = female) | |
| `cp` | categorical | Chest pain type (1–4) | 1: typical angina, 2: atypical angina, 3: non-anginal pain, 4: asymptomatic |
| `trestbps` | numeric | Resting blood pressure (mm Hg) | |
| `chol` | numeric | Serum cholesterol (mg/dl) | |
| `fbs` | categorical | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) | |
| `restecg` | categorical | Resting electrocardiographic results (0–2) | |
| `thalach` | numeric | Maximum heart rate achieved | |
| `exang` | categorical | Exercise-induced angina (1 = yes, 0 = no) | |
| `oldpeak` | numeric | ST depression induced by exercise relative to rest | |
| `slope` | categorical | Slope of the peak exercise ST segment (1–3) | |
| `ca` | categorical | Number of major vessels (0–3) colored by fluoroscopy | contains missing values |
| `thal` | categorical | Thalassemia result (3 = normal, 6 = fixed defect, 7 = reversible defect) | contains missing values |
| `target` | numeric | Original disease severity (0 = no disease, 1–4 = increasing severity) | as provided by UCI |
| `target_binary` | categorical | Binary label used for classification (0 = no disease, 1 = disease present) | derived in notebook 03/04/05: `1 if target > 0 else 0` |

## Notes

- No identifiable patient information (names, dates, medical record numbers)
  is present in this dataset.
- Missing values occur only in `ca` (5 records) and `thal` (2 records).
  These are handled either by dropping rows (baseline model in
  `03_supervised_learning.ipynb`) or by imputation inside the Scikit-learn
  `Pipeline` (`04_feature_engineering_pipeline.ipynb`).