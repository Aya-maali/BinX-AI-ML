# Week 4 - Machine Learning Model Evaluation and Pipelines

This week I focused on improving my machine learning workflow and learning how to properly evaluate and improve models.

I started by learning about model evaluation and how to use different metrics to understand model performance. I worked with metrics such as accuracy, precision, recall, F1 score, and ROC-AUC, and learned that the right metric depends on the problem and the type of errors I care about.

Then I learned about cross-validation and how it can give me a more reliable estimate of model performance by training and evaluating the model on different parts of the training data.

After that, I moved to hyperparameter tuning using GridSearchCV. I learned how to test different combinations of model parameters and select the configuration that performs best during cross-validation.

In the final part of the week, I learned about Scikit-learn Pipelines and data leakage. I used ColumnTransformer to handle numeric and categorical features, added engineered features, and connected the preprocessing steps with the model inside one Pipeline.

I then tuned the complete Pipeline using GridSearchCV with 5-fold cross-validation and evaluated the final tuned model on the held-out test set against a baseline.

## What I Practiced

- Model evaluation metrics
- Cross-validation
- Hyperparameter tuning
- GridSearchCV
- Data leakage
- Scikit-learn Pipelines
- ColumnTransformer
- Feature engineering
- Baseline comparison
- Final model evaluation
- Git and GitHub

By the end of the week, I had a better understanding of how to build a more reliable and organized machine learning workflow, from evaluating models to tuning them and creating a complete end-to-end Pipeline.