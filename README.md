# SmartCart — Customer Segmentation

## Overview

SmartCart is an unsupervised machine learning project that identifies customer segments based on their income, spending habits, purchasing behaviour, and campaign responses.

The goal is to understand different customer groups and explore how a retail business could use these insights to develop more targeted marketing strategies.

## Problem Statement

Customers have different purchasing habits, spending levels, and responses to marketing campaigns. Treating all customers the same may not be the most effective approach.

This project uses clustering techniques to discover groups of customers with similar characteristics and interpret their behaviour.

## Objectives

- Clean and prepare customer data.
- Perform exploratory data analysis (EDA).
- Create useful features such as age, customer tenure, and total spending.
- Apply encoding and feature scaling.
- Use Principal Component Analysis (PCA) for dimensionality reduction.
- Apply K-Means and Agglomerative Clustering.
- Compare customer segments and identify potential marketing opportunities.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Data Cleaning
- Handled missing income values using the median.
- Removed extreme age and income values using selected thresholds.
- Reduced the dataset from 2,240 to 2,236 customer records.

### 2. Feature Engineering
Created features including:
- `Age`
- `Customer_Tenure_Days`
- `Total_Spending`
- `Total_Children`

### 3. Exploratory Data Analysis
Used visualizations, pair plots, and a correlation heatmap to explore customer characteristics and relationships between numerical features.

### 4. Encoding and Feature Scaling
Applied One-Hot Encoding to categorical variables and StandardScaler to put features on comparable scales.

### 5. Dimensionality Reduction
Applied PCA to reduce 18 features to 3 principal components. These components retained approximately 44.95% of the original variance.

### 6. Choosing the Number of Clusters
Explored different cluster counts using the Elbow Method and Silhouette Score. The saved Elbow Method output suggested four clusters.

### 7. Clustering
Applied two unsupervised learning algorithms using four clusters:
- **K-Means:** Groups customers around cluster centroids.
- **Agglomerative Clustering:** Builds groups by progressively merging similar observations.

### 8. Cluster Characterization
Compared average income, total spending, website visits, purchasing behaviour, and campaign response to understand how the resulting customer groups differ.

## Key Findings

The saved Agglomerative Clustering results showed different spending patterns across four customer segments.

- Clusters 1 and 3 had higher average income and spending than Clusters 0 and 2.
- Cluster 3 had an observed campaign response rate of approximately 32%, the highest among the four groups.
- Clusters 0 and 2 had higher average monthly website visits but substantially lower average spending.

These findings describe patterns in the dataset and do not establish causation.

## Business Applications

The customer profiles could help a retail business explore:
- Loyalty programs and premium offers for higher-spending customers.
- Affordable promotions and relevant product recommendations for lower-spending customers.
- Different campaign strategies for groups with different response rates.

These strategies would need to be tested to determine whether they improve business outcomes.

## Limitations and Future Improvements

- The three PCA components retained approximately 44.95% of the original variance.
- The choice of four clusters should be validated further using Silhouette Scores and cluster interpretability.
- Clustering results should also be compared with results obtained using all scaled features.
- Suggested marketing strategies require real-world testing.

## How to Run

1. Clone or download this repository.
2. Install the dependencies listed in `requirements.txt`.
3. Obtain the dataset and place it at the file path expected by the notebook.
4. Open `smartcart.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook cells in order.

## Project Type

Unsupervised Machine Learning · Customer Analytics · Clustering · Exploratory Data Analysis

