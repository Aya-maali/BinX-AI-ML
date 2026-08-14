# Day 5 - Scikit-learn Pipelines

Today I focused on building a complete machine learning workflow using Scikit-learn Pipelines.

I started by learning about data leakage and why it is important to make sure that information from the test or validation data does not affect the training process. I learned that using a Pipeline helps keep preprocessing and model training together and makes the workflow safer.

After that, I built a Pipeline and used a ColumnTransformer to handle different types of features. I used StandardScaler for the numeric columns and OneHotEncoder for the categorical columns.

I also added an engineered feature to the dataset and included it in the Pipeline workflow. This helped me understand how feature engineering can be combined with preprocessing and model training.

Next, I used GridSearchCV to tune the full Pipeline. I tested different Random Forest hyperparameters and used 5-fold cross-validation to find the best combination.

Finally, I evaluated the tuned Pipeline on the held-out test set using the F1 score and compared its result with a baseline model.

## What I Practiced

- Data leakage and how to avoid it
- Scikit-learn Pipelines
- ColumnTransformer
- StandardScaler
- OneHotEncoder
- Feature engineering
- GridSearchCV
- 5-fold cross-validation
- Hyperparameter tuning
- Baseline vs tuned model evaluation
- Git and GitHub

At the end of the day, I had a complete end-to-end machine learning Pipeline that combines feature engineering, preprocessing, tuning, and final evaluation in one workflow.