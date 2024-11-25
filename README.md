# Customer Segmentation

### Problem Statement: 
Customer Segmentation for Marketing Strategy 
A retail company has collected data on its customers, including various attributes such as age, 
annual income, spending score, purchase frequency, and product preferences. The company's 
goal is to develop targeted marketing strategies by understanding the distinct customer 
segments within its database. Use a clustering algorithm (K-Means or Hierarchical 
Clustering) to identify groups (or clusters) of similar customers. These clusters will enable 
the company to personalize its marketing efforts, improve customer engagement, and 
ultimately increase sales. 
#### Requirements: 
#### Input:
A dataset containing various attributes of each customer. 
#### Output:
Identify distinct clusters representing different types of customers. 
#### Steps to Solve: 
Preprocess the data by scaling the numerical features. 
Use a clustering algorithm (e.g., K-Means or Hierarchical Clustering) to identify clusters in 
the customer data. 
Determine the optimal number of clusters (if using K-Means or Hierarchical). 
Analyze and interpret the clusters to provide actionable insights for marketing. 
### Dataset Used: 
Dataset used was the Mall Customers dataset, available at the following URL: 
https://raw.githubusercontent.com/tirthajyoti/Machine-Learning-with-Python/master/Datasets/Mall_Customers.csv 
This dataset includes information on customers, including: 
CustomerID: Unique ID for each customer. 
Gender: Gender of the customer. 
Age: Age of the customer. 
Annual Income (k$): The annual income of the customer in thousands of dollars. 
Spending Score (1-100): A score assigned by the mall based on customer spending patterns 
and behavior. 
The focus was on the Age, Annual Income (k$), and Spending Score (1-100) attributes, as 
they were relevant to clustering customers based on income, age, and spending habits. 
CustomerID (an identifier with no impact on behavior) and Gender (not essential for this 
particular segmentation task) were excluded. 
### Code Summary: 
The code followed the steps outlined in the problem statement to segment the customers into 
clusters based on their characteristics: 
1. Data Loading and Preprocessing: 
Loaded the dataset from the given URL. 
Removed unnecessary columns (CustomerID and Gender). 
Scaled the numerical features (Age, Annual Income, Spending Score) using StandardScaler to 
ensure comparable scales across features. 
2. Optimal Cluster Determination: 
Used the Elbow Method to identify the optimal number of clusters (k) for K-Means 
clustering. This approach helps determine the best value for k by plotting within-cluster sum 
of squares (inertia) and finding the "elbow point" where additional clusters provide 
diminishing returns. 
Additionally, Silhouette Scores were calculated for different values of k to validate the cluster 
separation quality. 
3. Clustering Using K-Means: 
Applied K-Means clustering with the optimal k value determined from the Elbow Method. 
Assigned each customer to a cluster and added this cluster label to the dataset. 
4. Cluster Analysis and Interpretation: 
Calculated the average Age, Annual Income, and Spending Score for each cluster to 
understand the characteristics of each customer segment. 
Generated scatter plots to visualize the clusters: 
Annual Income vs Spending Score: Shows clusters based on income and spending behavior. 
Age vs Spending Score: Highlights clusters based on age and spending habits. 
Provided actionable insights based on the characteristics of each cluster, offering suggestions 
for targeted marketing strategies for each segment.
