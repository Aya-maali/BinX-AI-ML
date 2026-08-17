# Week 5 - Day 2

## What I Did Today

Today I continued Week 5 by learning more about **clustering methods**.

I started by learning why **K-Means is not always the best choice**. I understood that K-Means works better with round-shaped clusters and that it always assigns every point to a cluster, even if there are outliers.

After that, I learned about **DBSCAN** and how it works based on the density of the data points. I practiced using DBSCAN to find clusters and identify noise points.

I also learned about the two main DBSCAN parameters, `eps` and `min_samples`, and how changing them can affect the clustering results.

Then, I learned about **Hierarchical Clustering**. I practiced creating a dendrogram to see how data points are grouped together step by step.

Finally, I compared **K-Means, DBSCAN, and Hierarchical Clustering** on the same dataset. I looked at the different results and thought about which method fits the data better.

## What I Learned

Today I learned how to:

* Understand the limitations of K-Means.
* Apply DBSCAN to a dataset.
* Understand `eps` and `min_samples`.
* Identify noise points using DBSCAN.
* Apply Hierarchical Clustering.
* Create and read a dendrogram.
* Compare different clustering methods.
* Choose a clustering method based on the shape and characteristics of the data.

## Tools I Used

* Python
* Scikit-learn
* SciPy
* Matplotlib
* Jupyter Notebook

## Final Takeaway

Today I learned that there is no single clustering method that works best for every dataset. I need to look at the data and choose the method that fits it better.

For the dataset I worked with today, I found that **DBSCAN** was a good choice because it could handle the irregular shape of the data and identify noise points.
