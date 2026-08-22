# Outputs

This folder is populated automatically when the notebooks in `notebooks/`
are run — nothing needs to be added here by hand.

Expected files after running all 5 notebooks:

| File | Produced by |
|---|---|
| `target_distribution.png` | `02_eda_statistics.ipynb` |
| `correlation_matrix.png` | `02_eda_statistics.ipynb` |
| `baseline_confusion_matrix.png` | `03_supervised_learning.ipynb` |
| `rf_confusion_matrix.png` | `03_supervised_learning.ipynb` |
| `model_comparison.csv` | `03_supervised_learning.ipynb` |
| `pipeline_confusion_matrix.png` | `04_feature_engineering_pipeline.ipynb` |
| `pca_clusters.png` | `05_unsupervised_learning.ipynb` |

If this folder is empty, it simply means the notebooks haven't been run yet
on this machine — run them in order (see the main `README.md`) to generate
these files.