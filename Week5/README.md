# Week 05 — Unsupervised Learning & Capstone Kickoff

## Overview

Week 5 marked the transition from **Phase 2 (Supervised Learning & Foundations)** to **Phase 3 (Capstone Project)** of the BinX Tech AI & Machine Learning Internship.

The first four days covered **unsupervised learning** — working with data that has no labels — through clustering, dimensionality reduction, and anomaly detection. Day 5 closed the week by selecting my capstone project and planning its first sprint, with mentor sign-off required before Phase 3 work begins.

## Daily Breakdown

| Day       | Topic                                          | Summary                                                                                                                                                                                                   |
| --------- | ---------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Day 1** | K-Means Clustering                             | Learned the difference between supervised and unsupervised learning. Applied K-Means, chose the number of clusters `k` using the Elbow Method and Silhouette Score, and scaled data before clustering.    |
| **Day 2** | DBSCAN & Hierarchical Clustering               | Learned the limitations of K-Means. Applied DBSCAN (density-based clustering with noise detection) and Hierarchical Clustering (dendrograms), then compared all three methods on the same dataset.        |
| **Day 3** | PCA (Dimensionality Reduction)                 | Learned the curse of dimensionality. Applied PCA, interpreted explained variance ratio, and reduced high-dimensional data to 2D for visualization.                                                        |
| **Day 4** | t-SNE & Anomaly Detection                      | Used t-SNE to visualize high-dimensional data and compared it to PCA. Applied Isolation Forest for anomaly detection and understood the role of the `contamination` parameter.                            |
| **Day 5** | Capstone Project Selection & Sprint 1 Planning | Selected my capstone project (Customer Churn Risk Prediction & Analysis), chose a dataset, wrote the problem statement and Definition of Done, and planned the Sprint 1 backlog with acceptance criteria. |

## Key Concepts Learned

* Supervised vs. unsupervised learning
* Clustering: K-Means, DBSCAN, Hierarchical Clustering
* Choosing `k`: Elbow Method and Silhouette Score
* Dimensionality reduction: PCA and explained variance
* Visualization: t-SNE vs. PCA
* Anomaly detection with Isolation Forest
* Translating a project idea into a problem statement, Definition of Done, and a sprint backlog with acceptance criteria

## Tools & Technologies

* Python 3.10+
* Scikit-learn (KMeans, DBSCAN, PCA, TSNE, IsolationForest)
* SciPy (hierarchical clustering / dendrograms)
* Pandas, Matplotlib
* Jupyter Notebook
* Git & GitHub

## Contents

```text
Week5/
├── Day1/   → K-Means Clustering
├── Day2/   → DBSCAN & Hierarchical Clustering
├── Day3/   → Dimensionality Reduction with PCA
├── Day4/   → t-SNE & Anomaly Detection
├── DAY5/   → Capstone Project Selection & Sprint 1 Plan
└── Project_Sprint1/  → Capstone project skeleton (data, notebooks, src, models, app.py)
```

## Week 5 Deliverables

* K-Means notebook with Elbow Method, Silhouette analysis, and interpreted clusters.
* Clustering-comparison notebook (K-Means vs. DBSCAN vs. Hierarchical) with a method recommendation.
* PCA notebook with a cumulative explained-variance plot and a justified component count.
* t-SNE and anomaly-detection notebook with a 2D visualization and Isolation Forest results.
* Capstone project selection, problem statement, and Sprint 1 plan (backlog + acceptance criteria), pending mentor sign-off.
* Initialized capstone project repository structure on GitHub.

## Capstone Project — Sprint 1 Status

**Project:** Customer Churn Risk Prediction & Analysis
**Dataset:** IBM Telco Customer Churn Dataset (7,043 customers, 21 features)
**Current Stage:** Sprint 1 planning complete — implementation (data understanding, cleaning, EDA, and baseline model) starts once the plan is approved by the mentor.

## Final Takeaway

Week 5 showed me that not all machine learning problems come with an answer key. Unsupervised learning requires more judgment: scaling data properly, validating the number of clusters or components with real metrics, and interpreting results rather than trusting them blindly. Day 5 was the hinge point of the program — closing Phase 2 and opening Phase 3 with a clear, mentor-approved plan instead of jumping straight into code.