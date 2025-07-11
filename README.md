# Online-Retail-Data-Analysis--K-Means-Clustering
Analyzing online retail data to group customers so that they can better be served to increase vendor and customer relations and ultimately profits. This is a very large file and dataset. Used the following Python Packages; pandas, matplotlib, seaborn, scikit-learn and openpyxl.

Dataset pulled from https://archive.ics.uci.edu/dataset/502/online+retail+ii

K-Means Clustering Steps in main file

1. Exploratory Data Analysis EDA
   
2. Data Cleaning

Created a cleaned DF. Removed invalid price values (0 and below) and null customers from dataset. Limited invoice column length to 6 digits to remove specialty invoices. 
length of the cleaned data divided by length of original was 0.773249 or 77.3%. 22.7% of the data was removed in cleaning.

3. Feature Engineering

  Added a "SalesLineTotal" column, the cost of the item multiplied the quantity to accurate represent each sale.
  Aggregated data - grouped by "Customer ID" based on
Monetary Value. Provides sum of the SalesLineTotal by customer ID.
Frequency - Number of unique values of invoices
Recency - Last invoice data
   
4. K-Means Clustering

Analyzed the data based on the proper number of clusters. Compared number of clusters from 2-12 and compared against Inertia value. Used the elbow method to select best cluster value. This was 4 according to the K-Means Inertia chart that was plotted. Verified this against the Silhouette score.

5. Analysis of Clusters

Provided 4 Customer Groups
   Cluster 0 Blue - Retain. High Value Customers who purchase regularly.
   Cluster 1 Orange - Re-engage, lower value and infrequent buyers. Should be re-engaged into purchasing.
   Cluster 2 Green - Nurture - This cluster represents the least active and lowest value customers. Build a relationship and provide excellent customer service.
   Cluster 3 Red - Reward = High-Value very frequent customers. Implement a robust loyalty program.

6. Analysis of Outliers

Provided 3 Further customer Groups
   Cluster -1 Pamper (Monetary Outliers) High spenders. Large value but infrequent customers. 
   Cluster -2 UPSELL (Frequency Outliers) Frequent Buyers. Customers that consistently engage.
   Cluster -3 DELIGHT (Monetary and Frequency Outliers) Most Valuable Outlier customer. Top Tier customers that require special attention.

7. Final Visualization

Provided a final visualization for the company to see the customer clusters. Showed that the nurture group is the biggest potential for company growth. Though the customers had the lowest value, they represented the bulk of customers and thus potential for growth. Also, showed scores for Recency, Frequency and Monetary Value by our 7 clusters (Clusters-3 through 3.
