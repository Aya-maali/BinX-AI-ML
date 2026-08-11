# Day 1 — Train / Validation / Test Splits

Today, I learned how to split a dataset into **training, validation, and test sets** and understood the purpose of each one.

I applied a **60/20/20 split** to the student dataset, then trained a KNN model and used the validation set to tune the `n_neighbors` parameter.

Finally, I evaluated the selected model on the test set and learned why the test set should only be used for the final evaluation to avoid biased results.
