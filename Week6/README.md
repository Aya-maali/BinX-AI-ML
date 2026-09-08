# Week 6 — Deep Learning Intro (Sprint 1)
## Project: Melanoma Skin Cancer Classification (Benign vs Malignant)
**BinX Tech AI & Machine Learning Internship — Phase 3, Sprint 1**

## What I Did
Built the full Sprint 1 pipeline for my capstone: picked a melanoma dataset 
from Kaggle, preprocessed it, trained a baseline, then built and compared 3 
neural network iterations in Keras.

## Dataset
Melanoma Skin Cancer Dataset (Kaggle) — real dermoscopic images, binary 
classification (Benign vs Malignant). Resized to 64x64, flattened, normalized, 
and shuffled for a Dense network.

## What I Built
- **Baseline (Logistic Regression):** 86.85% accuracy — the number every NN had to beat.
- **NN v1** (plain Dense, no regularization): 70.70% — overfit badly.
- **NN v2** (+ BatchNorm, Dropout 0.3, EarlyStopping): 82.20% — better, still unstable.
- **NN v3** (Dropout 0.4, lower LR): 82.60% — my best NN result.

## Result
**None of my neural networks beat the baseline.** This proved the sprint goal: 
a complex model only counts if it beats a simple one. It also showed that a 
plain Dense network can't handle raw image pixels well — setting up why I need 
a CNN in Week 7.

## What I'll Fix Next Sprint
- Change one hyperparameter at a time (not two, like v2→v3).
- Investigate the unstable validation loss curves (batch size / augmentation).
- Move to a CNN, which should exploit the image's spatial structure properly.

## Tools
Kaggle API • TensorFlow/Keras • Scikit-learn • NumPy • Matplotlib • Colab (GPU) • Git & GitHub