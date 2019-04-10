# Identify Customer Segments

This project involves the application of k-means clustering to the demographic and spending data for a sample of German
households. Similar clustering is also applied to the demographic data of the customers of a mail-order sales company 
still in Germany. The objective of the project is to identify the cluster in the general population dataset which should 
be the target audience for a mail outreach campaign for potential customers. The datasets for the project are real-life data
and have been provied by the Arvato Financial Services.  

## Model Description

The k-means model consist of three clusters, which capture the different income levels in the datasets. Prior to applying
the k-means model, the datasets had to be cleaned to rid them of missing values and outliers. In addition to the cleaning,
principal component analysis (PCA) transformation was applied to the datasets to reduce dimensionality and eliminate noise.
The k-means object was first trained on the general population dataset and used to segment the general population into clusters,
the same object was used to predict the cluster membership of the data points in the customer data set. A comparison was 
made, of the relative size of identical clusters from both datasets. If the size of a cluster in the customer dataset 
was relatively and significantly larger than the size of similar cluster in the general population dataset, then such cluster
was considered to be a target cluster for the mail campaign. The rationale for the technique is that since the two datasets
are obtained from similar population then the distribution of cluster sizes should be the same for both datasets. Any 
discrepancy then shows either an over or under representation of the cluster members in the general population dataset.