# Week 5 - Day 4

## What I Did Today

Today I continued Week 5 by moving from clustering and PCA into two new topics: **t-SNE** for visualization and **Anomaly Detection**.

I started by learning what t-SNE (t-distributed Stochastic Neighbor Embedding) does and how it is different from PCA. While PCA preserves the global variance of the data, t-SNE focuses on keeping points that are close together in high dimensions close together in the 2D plot. I practiced applying t-SNE to a high-dimensional dataset and compared the resulting visualization with the PCA plot from Day 3.

After that, I moved on to **Anomaly Detection**. I learned that anomaly detection means finding data points that are significantly different from the rest of the data, such as an unusual transaction, a defective product, or a system failure. I understood why this task is usually unsupervised — anomalies are rare and are rarely labeled in advance.

I practiced using **Isolation Forest** to detect anomalies. I learned how the algorithm isolates unusual points faster than normal points because they sit farther away from the dense areas of the data, and how the `contamination` parameter represents my own estimate of the expected percentage of anomalies, rather than something the model discovers on its own.

Finally, I connected this to what I learned in Day 2, since DBSCAN also flags noise points (label `-1`), which is another simple form of anomaly detection.

## What I Learned

Today I learned how to:

* Apply t-SNE to reduce high-dimensional data to 2D for visualization.
* Explain the difference between PCA and t-SNE and when to use each.
* Understand that t-SNE axes have no direct meaning and should only be used for visual inspection, not for feeding into a model.
* Explain what anomaly detection is and why it is often unsupervised.
* Apply Isolation Forest to detect anomalies in a dataset.
* Understand the role of the `contamination` parameter.
* Interpret which points were flagged as anomalies and hypothesize why.
* Recognize the overlap between clustering (DBSCAN noise points) and anomaly detection.

## Tools I Used

* Python
* Scikit-learn (TSNE, IsolationForest)
* Matplotlib
* Jupyter Notebook

## Final Takeaway

Today helped me understand that not every dimensionality-reduction technique is meant for the same purpose — PCA is useful for compression and modeling, while t-SNE is useful purely for visual exploration. I also learned that anomaly detection is about judgment, not a fixed answer: I have to decide what fraction of the data I expect to be unusual, then interpret the flagged points rather than blindly trusting the model's output.