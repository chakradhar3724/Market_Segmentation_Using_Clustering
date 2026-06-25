# Mall Customer Segmentation using Clustering

## Project Overview
Customer segmentation is a critical task in marketing analytics that helps businesses
understand customer behavior and design targeted strategies.

In this project, **unsupervised machine learning techniques** are applied to segment
mall customers based on their demographic and spending behavior. Multiple clustering
algorithms are evaluated and compared to identify the most meaningful customer groups.

---

## Objectives
- Perform customer segmentation using clustering techniques
- Compare multiple clustering algorithms
- Visualize clusters using dimensionality reduction techniques
- Evaluate clustering performance using Silhouette Score
- Generate actionable business insights from customer segments

---

## Dataset
- **Dataset Name:** Mall Customers Dataset
- **Records:** 200 customers
- **Features:**
  - Gender
  - Age
  - Annual Income (k$)
  - Spending Score (1–100)

> The dataset contains no missing values and is well-suited for clustering analysis.

---

## Data Preprocessing
The following preprocessing steps were applied:
- Removed non-informative `CustomerID` column
- Encoded categorical variable (`Gender`) using Label Encoding
- Standardized numerical features using `StandardScaler`
- Verified absence of missing values

Feature scaling was essential as clustering algorithms rely on distance metrics.

---

## Algorithms Implemented
The following clustering techniques were applied and compared:

- **K-Means Clustering**
- **Hierarchical (Agglomerative) Clustering**
- **DBSCAN**

---

## Model Evaluation
Since clustering is an unsupervised task, **Silhouette Score** was used for evaluation.

| Algorithm       | Silhouette Score |
|----------------|------------------|
| K-Means        | 0.27 |
| Hierarchical   | 0.29 |
| DBSCAN         | 0.01 |

> Hierarchical clustering achieved the highest silhouette score, while DBSCAN performed
poorly due to overlapping data distributions.

---

## Dimensionality Reduction & Visualization
To visualize high-dimensional data, the following techniques were used:

- **PCA (Principal Component Analysis)** – Linear dimensionality reduction
- **t-SNE (t-Distributed Stochastic Neighbor Embedding)** – Non-linear visualization

### Visualizations Included:
- Elbow Method for optimal number of clusters
- Dendrogram for hierarchical clustering
- PCA-based cluster visualization
- t-SNE-based cluster visualization
- Annual Income vs Spending Score (business-focused segmentation)

---

## Business Insights
The clustering results reveal distinct customer segments such as:
- **High Income – High Spending:** Target customers for premium offerings
- **High Income – Low Spending:** Upsell and engagement opportunity
- **Low Income – High Spending:** Promotion-sensitive customers
- **Low Income – Low Spending:** Low-priority segment

These insights can support **data-driven marketing strategies**, customer retention,
and personalized promotions.

---

## Project Structure
```
Mall-Customer-Segmentation/
│
├── data/
│ └── Mall_Customers.csv
│
├── notebooks/
│ └── Mall_Customer_Segmentation.ipynb
│
├── outputs/
│ └── Customer_Segments.csv
│
├── requirements.txt
├── README.md
└── .gitignore
```


---

## How to Run the Project

### 1. Install Dependencies
```
pip install -r requirements.txt
```

### 2. Run the Notebook
```
jupyter notebook notebooks/Mall_Customer_Segmentation.ipynb
```

## Output
- **Customer_Segments.csv**  
  Contains the original customer dataset along with the assigned cluster label
  for each customer based on K-Means clustering.

---

## Future Improvements
- Perform feature selection to improve cluster separation
- Tune DBSCAN parameters using k-distance plots
- Apply clustering only on behavioral features (income and spending score)
- Build an interactive dashboard for customer segment exploration

---

## Author
**Chakradhar Peddavenkatagari**  

Aspiring AI Engineer

Masters in Computer Science

The State University of New York at Buffalo 
