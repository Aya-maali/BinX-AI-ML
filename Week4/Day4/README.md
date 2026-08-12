# Day 4 — Feature Engineering & Hyperparameter Tuning

Today, I learned how I can improve a machine learning model by preparing better features and finding better model settings.

I started with a student performance dataset where I wanted to predict whether a student would pass. I created two new features: `study_efficiency` and `academic_engagement`. I created them by combining existing information such as study hours, previous scores, attendance, and completed assignments. This helped me understand how Feature Engineering can give a model more useful information.

After that, I learned about hyperparameters and used a Random Forest model. I created a hyperparameter grid for `n_estimators`, `max_depth`, and `min_samples_split` instead of choosing their values manually.

Then, I used `GridSearchCV` with 5-fold cross-validation to test different combinations and find the best configuration. I also compared the tuned model with the untuned baseline to see whether tuning improved the performance.

In my experiment, the displayed combinations achieved an F1 score of `1.0`, so there was no clear difference between them based on the cross-validation results.

Finally, I learned how to look at feature importance and how to use the results of GridSearchCV to understand which features and hyperparameters had the most impact.

Overall, today I learned that improving a machine learning model is not only about choosing the model itself. Creating meaningful features and tuning the model systematically can also make a big difference.