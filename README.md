# Mall Customer Segmentation Using K-Means Clustering

## Project Overview

This project focuses on customer segmentation using **Unsupervised Machine Learning**. The objective is to identify groups of customers with similar purchasing patterns based on their annual income and spending scores.

The project uses the K-Means clustering algorithm to segment customers into meaningful groups and derive business insights that can support targeted marketing strategies and customer engagement.

## Dataset

- **Dataset:** Mall Customer Segmentation Dataset
- **Source:** [Kaggle – Customer Segmentation Tutorial](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial)
- **Total Records:** 200
- **Features Used:**
  - Annual Income (k$)
  - Spending Score (1–100)

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Data Exploration and Analysis

- Inspected dataset structure and data types.
- Checked missing values and duplicate records.
- Explored numerical feature distributions.
- Visualized the relationship between annual income and spending score.

### 2. Feature Selection

Selected two numerical features for clustering:

- Annual Income (k$)
- Spending Score (1–100)

CustomerID was excluded because it is an identifier and does not represent customer behaviour.

### 3. Feature Scaling

Applied **StandardScaler** to standardize numerical features.

Scaling ensures that both features contribute appropriately to distance calculations in K-Means.

### 4. K-Means Clustering

Implemented K-Means clustering with different values of K.

The number of clusters was evaluated using:

- **Elbow Method:** Used inertia to identify diminishing improvements as the number of clusters increased.
- **Silhouette Score:** Evaluated cluster cohesion and separation.

### 5. Model Selection

Selected **K = 5** based on the highest Silhouette Score among the tested configurations.

- Selected clusters: 5
- Highest Silhouette Score: 0.555

### 6. Cluster Visualization

Visualized the resulting customer segments using a scatter plot, with cluster centroids displayed to understand the distribution of customers.

### 7. Cluster Profiling and Business Insights

Analyzed the average annual income, spending score and customer count for each cluster.

| Cluster | Customer Segment | Characteristics |
|---|---|---|
| 0 | Standard Customers | Medium income, medium spending |
| 1 | Premium Customers | High income, high spending |
| 2 | High-Spending, Lower-Income Customers | Low income, high spending |
| 3 | Careful Spenders | High income, low spending |
| 4 | Low-Income, Low-Spending Customers | Low income, low spending |

These interpretations help identify potential customer groups and support targeted marketing decisions.

## Key Findings

- Identified five distinct customer segments.
- Cluster 0 represents the largest segment, with 81 customers.
- Cluster 1 represents high-income, high-spending customers.
- Cluster 3 identifies high-income customers with relatively low spending.
- Cluster 2 highlights customers with lower income but higher spending scores.

## Project Structure

```text
Mall_Customer_Segmentation/
│
├── data/
│   └── Mall_Customers.csv
│
├── notebooks/
│   └── customer_segmentation.ipynb
│
└── README.md
```

## How to Run the Project

**1. Clone the repository**

```bash
git clone <your-repository-url>
```

**2. Navigate to the project directory**

```bash
cd Mall_Customer_Segmentation
```

**3. Install dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

**4. Launch Jupyter Notebook**

```bash
jupyter notebook
```

Open `notebooks/customer_segmentation.ipynb` and run the cells.

## Conclusion

This project demonstrates how unsupervised machine learning can be used to discover customer behaviour patterns without predefined labels.

Using K-Means clustering, five customer segments were identified and interpreted through cluster profiling. These insights can help businesses understand their customers, develop targeted marketing strategies and improve customer engagement.

---

**Project Focus:** Unsupervised Learning | Customer Segmentation | K-Means Clustering | Data Analysis