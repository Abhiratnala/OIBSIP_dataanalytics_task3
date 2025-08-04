# 🧠 Customer Segmentation using K-Means Clustering

This project is part of my Data Analytics Internship at **Oasis Infobyte**, focused on segmenting customers using **K-Means clustering** based on their demographics and purchasing behavior. The goal is to help businesses understand their customer base and tailor marketing strategies accordingly.

## 📁 Dataset
- **Source**: `ifood_df (1).csv`

## 📌 Key Steps

### 📦 1. Project Setup & Data Loading
- Imported libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`
- Loaded the dataset into a Pandas DataFrame
- Initial data exploration: `.info()`, `.describe()`, `.nunique()`

### 🧹 2. Data Cleaning & Preprocessing
- Removed non-informative columns: `Z_CostContact`, `Z_Revenue`
- Detected and removed outliers from `MntTotal` and other numerical columns using **IQR method**
- Engineered a new feature: **`Frequency`** = sum of all purchase channels
- Created a cleaned DataFrame `df_cleaned` for further analysis

### 📊 3. Exploratory Data Analysis
- Visualized distributions of **Age** and **Income**
- Box plots to understand income distribution by customer cluster

### 📈 4. Feature Selection & Scaling
- Selected features: `Recency`, `Frequency`, `MntTotal`, `Income`, `Age`
- Standardized features using `StandardScaler`

### 🔍 5. K-Means Clustering
- Used **Elbow Method** and **Silhouette Score** to determine optimal number of clusters (`k`)
- Chose **k = 3** based on analysis
- Applied K-Means and assigned cluster labels

### 📉 6. Dimensionality Reduction & Visualization
- Applied **PCA** to reduce features to 2 components
- Visualized clusters in a 2D space using scatter plots

### 🧠 7. Cluster Analysis
- Merged cluster labels with original data
- Analyzed average feature values for each cluster
- Visualized spending behavior across product categories by cluster
- Calculated size and percentage share of each segment

## 🎯 Customer Segments Identified

| Cluster | Description                     |
|---------|---------------------------------|
| 0       | **High-Value Churn Risk**       |
| 1       | **High-Value Loyal Customers**  |
| 2       | **Budget-Conscious Starters**   |


## ✅ Recommendations

- 🎯 **Cluster 0**: Retention campaigns, loyalty benefits
- 🌟 **Cluster 1**: Upselling opportunities, premium offers
- 💡 **Cluster 2**: Budget product recommendations, referral incentives

## 📌 Tools & Libraries Used

- Python (Pandas, Numpy, Scikit-learn)
- Matplotlib & Seaborn for Visualization
- K-Means Clustering
- PCA for dimensionality reduction

## 📂 Project Structure
```bash
├── ifood_df.csv
├── customer_segmentation.ipynb
├── README.md
