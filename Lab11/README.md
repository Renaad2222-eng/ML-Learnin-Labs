Final Questions

1. Why is this an unsupervised learning problem?
Because there is no target label (no predefined customer groups). The goal is to discover hidden patterns and group customers based on their behavior using clustering.

2. Why did we remove the CUST_ID column?
Because it is only an identifier and does not represent any behavioral information. It does not help in clustering and can distort distance-based algorithms like K-Means.

3. Which columns had missing values?
The missing values were mainly in:
MINIMUM_PAYMENTS
CREDIT_LIMIT

4. How did you handle the missing values?
We used mean imputation, meaning each missing value was replaced with the average value of its column.

5. Why is scaling important before applying K-Means?
K-Means depends on distance calculations. Since features have different ranges (e.g., BALANCE vs frequency columns), scaling ensures all variables contribute equally to clustering.

6. Which K value did you choose? Explain your answer using the elbow method and silhouette score.
We selected K = 5. Even though the silhouette score reached its highest value at K = 2, the elbow curve indicated that K = 5 gives a better trade-off because the reduction in inertia became slower after that point. In addition, using 5 clusters created more useful and detailed customer segments.

7. Based on the cluster summary table, describe each customer segment in your own words.
Cluster 0: Customers with low spending and moderate use of cash advances. These customers appear to have limited credit card activity.
Cluster 1: Customers who make purchases frequently and use cash advances less often. They mainly use their credit cards for everyday transactions.
Cluster 2: Customers with very high balances, purchases, credit limits, and payments. This cluster represents premium customers with strong and active card usage.
Cluster 3: Customers with high balances and heavy cash advance usage but relatively low purchases. These customers seem to depend more on cash withdrawals rather than shopping purchases.
Cluster 4: Customers with high purchase amounts and frequent transactions along with moderate credit usage. They appear to be active and important customers.

8. Which cluster may represent high-value customers?
Cluster 2 may represent the high-value customers because it has the highest purchases, highest credit limit, and highest payment values, indicating strong spending activity and valuable customers.

9. Which cluster may represent customers who rely more on cash advance?
Cluster 3 may represent customers who rely more on cash advance because it has the highest cash advance amount and cash advance frequency compared to the other clusters.

10. How can a company use these clusters for marketing strategy?
Reward high-value customers with loyalty programs and cashback
Offer financial assistance or lower interest plans for cash-advance users
Encourage inactive customers with promotions to increase usage
Provide personalized credit limits and offers based on each segment
Improve targeted marketing campaigns instead of general advertising

what was done
In this lab, we applied K-Means clustering to segment credit card customers based on their behavior. We cleaned the dataset, handled missing values using mean imputation, removed the CUST_ID column, and scaled the features using StandardScaler. Then, we used the Elbow Method and Silhouette Score to choose the best number of clusters (K = 5). After training the final K-Means model, we analyzed and visualized the customer segments using PCA to better understand different customer behaviors.
