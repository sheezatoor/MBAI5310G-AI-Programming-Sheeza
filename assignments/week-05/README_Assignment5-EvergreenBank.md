# Week [05] – [Assignment5: Unsupervised Learning for Pattern Discovery and Customer/User Segmentation]

## Files in This Folder
- Assignment5_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/Customer Clusters.png
- outputs/Customer Segments.png
- EvergreenBank-data_description.md: dataset provided by instructor 

## Task Overview
-  Use unsupervised learning to discover patterns in a marketing-related dataset.

## Task 1: Understand the Business Problem
What is the main business problem?
- Evergreen bank would like to find existing credit card customers which are most suitable for the premium card update without wasting marketing budget and reducing customer satisfaction as not all customers are the same. 
Why is customer/user segmentation useful for this business?
- Segmentation helps group customers into clusters that are similar based on different characteristics such as spending, engagement, risk and satisfaction patterns. The bank can create more personalized offers using one campaign. 
What kind of marketing decisions could be improved by discovering customer/user groups?
The bank should examine which customers should receive the premium offer and what channel of communication should be used. It can help decide other aspects too such as loyalty rewards, education and reactivation. 

## Task 2: Prepare the Dataset
Load the dataset in Python.
Inspect the dataset by checking:
Number of rows and columns
Column names
Data types
Missing values
Duplicate rows
Clean the dataset if needed.
Select the numerical features that are useful for clustering.
Scale the selected features before applying K-means clustering.

## Task 3: Apply K-means Clustering
Explain why you selected that number of clusters.
- There were three clusters used. The decrease in intertia became more gradual after around K = 3. Customers can be interpreted as low engagement, at-risk, or highly engaged. 

## Task 4: Analyze and Interpret the Clusters
How many customer/user segments did you find?
- Three cluster segments were found 
What are the main characteristics of each segment?
- Cluster 0: 174 customers (low spending, lower reward points, lower digital engagement)
- Cluster 1: 66 customers (highest logins, highest credit utilization, late payments)
- Cluster 2: 100 customers (highest monthly card spend, highest travel spend share)
How are the segments different from each other?
- Cluster 2 appears financially valuable
- Cluster 1 is digitally active but riskier
- Cluster 0 is lower-value and less engaged.
Which segment may be the most valuable for the business? Why?
- High Value Spenders; highest average monthly card spend at $1505.62 & reward points balance at 9028.54.
Which segment may need more marketing attention? Why?
- Low engagement/at-risk customers; largest group but lowest average spend and lowest reward points. 

## Task 5: Visualize the Clusters
Visualization 1: Spending vs. Engagement (Customer Clusters)
- customers are group based on average monthly card spend and digital app engagement 
- higher spenders are more separated than lower spenders
Visualization 2: Spending vs. Engagement (Customer Segments)
- uses segment names instead of only cluster numbers
- show each customer based on spending and app activity 

## Task 6: Business Interpretation
What patterns did you discover?
- main customer difference by spending level, reward points, digital engagement and risk indicators. 
- more revenue potential with high value customers 
How can the business use these customer/user segments?
- use segments to create personalized marketing strategies including card upgrade campaigns.
- prioritze high value customers and re-engage lower activity customers. 
What marketing strategy would you suggest for each segment?
- high value spenders: offer premium rewards
- highly engaged customers: offers through app or email
- low engagement/at-risk: reactivation campaign
How can this analysis help the business improve decision-making?
- make targeted marketing decisions
- reduce wasting market budget

## Task 7: Limitations and Responsible AI Reflection
What is one limitation of your dataset or clustering model?
- limited amount of data, a great model works well with diverse and large data. 
Why does K-means not always produce perfect customer segments?
- it based on mathematical distances and does not account for real-world context. 
What kind of bias or unfair decision could happen if the business uses these clusters without human review?
- they could favour some customers over others given race, gender, or economic status. 
Why should human judgment still be used when making marketing decisions?
- human judgement would essential to evaluate fairness and affordiblity in customer needs. 
