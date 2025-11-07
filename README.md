🧠 Customer Segmentation using Unsupervised Learning (K-Means)
🌟 Project Summary

This project is about understanding customer behavior using unsupervised learning — specifically, the K-Means clustering algorithm.
The main goal was to group customers into segments based on their credit limits, number of cards, and interaction patterns (visits, calls, online usage).

By doing this, we can uncover patterns that aren’t obvious at first glance — for example, which customers are high-value, which are highly engaged, and which might need more support.

🎯 Objective

To use machine learning (without labeled data) to:

Identify distinct customer groups

Understand how each group behaves

Generate insights that can help improve decision-making, customer engagement, and targeted marketing

📊 Data Overview

The dataset contained customer information such as:

Average credit limit

Total credit cards

Number of visits to bank branches

Online portal visits

Calls made to customer support

Each of these variables helps paint a picture of how customers interact with a financial institution.

🧩 Approach & Methodology
1️⃣ Data Preprocessing

Before training, the data was cleaned and prepared:

Removed irrelevant columns like Customer Key and Sl_No

Filled missing values using SimpleImputer

Scaled all numerical features using StandardScaler (since K-Means is sensitive to scale)

2️⃣ Feature Selection

Kept only numerical columns — perfect for clustering algorithms to find hidden patterns.

3️⃣ Clustering Model (K-Means)

Tested different numbers of clusters (k = 2 to 10)

Used both:

Inertia (WCSS) → measures cluster compactness

Silhouette Score → measures how well clusters are separated

✅ The best result came with k = 3

Inertia (WCSS): 933.04

Silhouette Score: 0.5157

A silhouette score above 0.5 indicates well-defined clusters — good separation and meaningful grouping.

4️⃣ Cluster Profiling

After clustering, each customer was assigned a cluster label (0, 1, or 2).
Then, we grouped data by cluster to see the average values for each feature — revealing clear behavioral differences.

💡 Key Insights
Cluster	Behavior Summary	Interpretation
Cluster 0	Moderate credit limit, balanced visits and calls	Regular customers
Cluster 1	Very high credit limit, fewer calls, fewer visits	Premium or high-value customers
Cluster 2	Low credit limit, more calls and visits	Credit-sensitive or service-dependent customers

These insights can help a company:

Target premium customers with exclusive offers

Support service-heavy customers more efficiently

Build loyalty among regular customers through personalized engagement

🧠 Challenges Faced

Every project comes with its own set of hurdles — here’s what stood out:

Scaling imbalance: The credit limit values were much larger than others, making early visuals misleading. Solved this by standardizing all features.

Choosing the right k: Finding the optimal number of clusters required trial, plotting, and interpretation.

Visualization clarity: The initial cluster profiles were hard to read due to scale differences, so heatmaps and normalization were used to make patterns more visible.

📈 Visuals & Analysis

Throughout the project, multiple visualizations were used to understand and validate the results:

Correlation Heatmap to identify relationships between variables

Elbow Plot to determine optimal cluster count

Silhouette Plot to validate cluster quality

Cluster Profile Heatmap to understand cluster characteristics

Each visualization helped confirm that the clusters were meaningful and well-separated.

🏁 Conclusion

The K-Means model effectively grouped customers into three distinct behavioral segments, helping uncover patterns in spending and activity.
With a Silhouette Score of 0.51, the clusters are well-separated and provide actionable business insights.

This unsupervised learning approach can be a foundation for:

Customer targeting

Churn prediction

Marketing optimization

Personalized product recommendations
