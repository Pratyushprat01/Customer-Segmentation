# 🧠 Customer Segmentation using Unsupervised Learning (K-Means)

---

##  Project Summary  
This project focuses on **understanding customer behavior** using the **K-Means clustering algorithm**, an **unsupervised learning** technique.  

The primary goal was to group customers into meaningful segments based on:
- Average Credit Limit  
- Total Number of Credit Cards  
- Bank Visits  
- Online Visits  
- Calls Made  

By uncovering these patterns, businesses can better identify:
- Which customers are high-value  
- Which are highly engaged  
- Which need additional support or attention  

---

## Objective  

To use **machine learning (without labeled data)** to:  
-  Identify distinct customer groups  
-  Understand behavioral patterns within each segment  
-  Generate actionable insights to improve customer engagement, decision-making, and marketing strategies  

---

## 📊 Data Overview  

The dataset included customer information such as:  
- **Average Credit Limit**  
- **Total Credit Cards**  
- **Number of Bank Visits**  
- **Online Portal Visits**  
- **Customer Support Calls Made**

Each of these variables helps paint a clear picture of how customers interact with a financial institution.

---

##  Approach & Methodology  

###  Data Preprocessing  
- Removed irrelevant columns (`Customer Key`, `Sl_No`)  
- Handled missing values using **SimpleImputer**  
- Standardized numerical features using **StandardScaler** (since K-Means is scale-sensitive)

###  Feature Selection  
- Retained only numerical columns to help K-Means discover hidden patterns effectively  

###  Clustering Model — **K-Means**  
- Tested multiple values of **k (2–10)**  
- Evaluated each using:  
  - **Inertia (WCSS):** Measures how compact the clusters are  
  - **Silhouette Score:** Measures how distinct and well-separated clusters are  

 **Best Results:**  
- **k = 3**  
- **Inertia (WCSS):** 933.04  
- **Silhouette Score:** 0.5157 *(indicating well-defined clusters)*  

###  Cluster Profiling  
Each customer was assigned a cluster (0, 1, or 2).  
We then compared average feature values per cluster to interpret behavioral differences.

---

## 💡 Key Insights  

| Cluster | Behavior Summary | Interpretation |
|----------|------------------|----------------|
| **Cluster 0** | Moderate credit limit, balanced visits & calls | Regular customers |
| **Cluster 1** | Very high credit limit, fewer calls & visits | Premium / high-value customers |
| **Cluster 2** | Low credit limit, more calls & visits | Credit-sensitive or service-dependent customers |

### 💬 Business Implications  
-  Target premium customers with **exclusive offers**  
-  Support service-heavy customers with **priority help**  
-  Retain regular customers through **personalized engagement**  

---

## ⚙️ Challenges Faced  

| Challenge | Solution |
|------------|-----------|
| **Imbalanced feature scales** (credit limit dominating visuals) | Applied StandardScaler |
| **Choosing optimal k** | Used both Elbow and Silhouette methods |
| **Cluster interpretability** | Used normalized heatmaps and visual profiling |

---

## 📈 Visualizations & Analysis  

Visual tools used to validate and interpret the results:

- **Correlation Heatmap** — Understanding variable relationships  
- **Elbow Plot** — Optimal cluster count selection  
- **Silhouette Plot** — Cluster quality validation  
- **Cluster Heatmap** — Clear profile comparison  
- **2D PCA Scatter Plot** — Visualizing clusters in two dimensions  

---

## Conclusion  

The **K-Means model** effectively identified **three customer segments**, uncovering patterns in spending, credit usage, and engagement.  
With a **Silhouette Score of 0.51**, clusters are **well-separated** and **actionable**.

This analysis enables:
- Smarter **customer targeting**  
- Early **churn detection**  
- Optimized **marketing campaigns**  
- Better **product personalization**

---

## Future Enhancements  

-  Try **DBSCAN** or **Hierarchical Clustering** for comparison  
-  Use **PCA** for dimensionality reduction and advanced visualization  
-  Integrate **demographic & transaction data** for deeper segmentation  
-  Deploy clustering results in a **Power BI Dashboard** for business reporting  

---

## Tech Stack  
- **Python** (pandas, numpy, matplotlib, seaborn, scikit-learn)  
- **Jupyter Notebook / VS Code** for experimentation  
- **Power BI (optional)** for dashboard visualization  

---
