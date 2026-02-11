# Customer Segmentation using Clustering

## Project Overview
This project performs **Customer Segmentation** using unsupervised machine learning techniques.  
Customers are grouped into different segments based on their **Annual Income** and **Spending Score** to help businesses understand customer behavior.

---

## Dataset
Dataset used: **Mall Customers Dataset (Kaggle)**  
It contains the following features:

- CustomerID – Unique customer identifier
- Gender – Customer gender
- Age – Customer age
- Annual Income (k$) – Annual income of customer
- Spending Score (1–100) – Score assigned based on customer behavior and spending nature

---

## Objectives
- Perform **data exploration and visualization**
- Apply **feature scaling**
- Determine optimal number of clusters using the **Elbow Method**
- Apply **K-Means clustering**
- Visualize customer segments using **2D plots**
- Compare clustering with **DBSCAN** (Bonus)
- Analyze **average spending per cluster**

---

## Tools & Libraries
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## Methodology
1. Load and explore the dataset
2. Select relevant features (Income and Spending Score)
3. Standardize features using StandardScaler
4. Determine optimal clusters using the Elbow Method
5. Apply K-Means clustering
6. Visualize clusters
7. Evaluate cluster averages
8. Apply DBSCAN clustering (bonus)

---

## Results
The clustering model successfully segmented customers into groups representing different spending behaviors such as:
- High income – high spending
- High income – low spending
- Low income – high spending
- Average income – average spending

These segments can help businesses create targeted marketing strategies.

---

## Conclusion
Customer segmentation using clustering provides valuable insights into customer behavior without labeled data.  
K-Means clustering effectively identified meaningful customer groups, and DBSCAN provided an alternative clustering approach for comparison.
