## Title
### Financial Customer Segmentation Analysis

## Objective
#### The primary goal of this project is to segment financial customers based on their transaction patterns and behaviours. This segmentation can enable businesses to derive actionable insights and tailor strategies for different customer groups.

## Data Analysis Process
### 1. Data Loading
- Load the dataset for analysis.
### 2. Data Exploration and Cleaning
- **Check Data Types**: Identify numerical and categorical variables.
- **Validate Transactions**: Ensure all transaction values are non-negative.
- **Statistical Overview**: Compute and examine statistical metrics, including:
  - Mean balance.
  - Average purchases.
  - One-off purchase average.
  - Purchase frequency.
  - Average tenure.
  
- **Handle Missing Values**:
Since CREDIT_LIMIT and MINIMUM_PAYMENTS are highly right-skewed, the median is used as a robust measure for imputation.
Remove Irrelevant Columns: Drop unnecessary fields such as CUST_ID.

### 3. Feature Engineering
- **Correlation Analysis**: Use correlation matrices and heatmaps to detect multicollinearity and refine feature selection.
- **Data Normalisation**: Since different attributes have different scales, if calculated together for distance, the number with bigger will contribute the most to the distance and lead to a biased result.

### 4. Customer Segmentation with K-Means
#### Cluster Identification:
- Use the elbow method to determine the optimal number of clusters (k).
- Validate the clustering quality with silhouette scores, identifying that k = 3 offers the best segmentation.
- Cluster Centres Analysis: Examine the average characteristics of each cluster to better understand customer behaviour.

### 5. Dimensionality Reduction with PCA
Apply PCA to reduce the dataset dimensions while retaining most of the original variability.

![image](https://github.com/user-attachments/assets/57021c1c-b3a2-4394-b64c-4662a55b7d83)


## Cluster Insights
### Cluster 0:
Customers have a relatively low balance, use more frequently than other clusters in cash advances. With low purchase activity and High tenure. This might be a long-term customer who prefer using cash advances over making purchases.

### Cluster 1:
Moderate balance, low cash advances. Make purchases frequently but with smaller amounts and prefer to make purchases in instalments. These customers are frequent shoppers who prefer to spread their payments over time and rarely use cash advances.

### Cluster 2:
Highest balance with highest credit limit makes high-value purchases. In addition, they tend to pay their balance in full. These can be seeming as high-value customers.


## Business Strategies 

### Cluster 0:

Offer incentives for making more purchases. Encourage the use of other financial products besides cash advances.

### Cluster 1:

Offer promotions or discounts to increase spending. Provide personalized recommendations and rewards for frequent purchases.

### Cluster 2:

Offer premium services and Introduce high-end financial products to retain these high-value customers.
