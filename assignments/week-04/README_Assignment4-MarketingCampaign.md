# Week [04] – [Assignment4: Decision Tree Model and Business Interpretation Based on a Business Plan]

## Files in This Folder
- Assignment4:MarketingCampaign_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/README_MarketingCampaign-DataPrepOutput.md
- outputs/README_MarketingCampaign-ModelResultsOutput.md
- MarketingCampaign-data_description.md: dataset provided by instructor 

## Task Overview - Marketing Campaign Decision Tree Classification Assignment
-  Building a Decision Tree classification model and interpret the results from a business perspective.

## Task 1: Understand the Business Problem 
What is the business about?
-   The business is called AdVantage Growth Studio. It is a campaign and marketing agency that helps small-medium size businesses design market campaigns. It uses customer data, campaign engagement data, and sales outcomes to businesses understand customer responses to their marketing campaigns. 
What problem is the business trying to solve?
- The are having a problem with marketing inefficiency. Some customers are unlikely to respond and businesses suffer loss by spending money on sending them the marketing campaigns. Similarly, they also face the challenge of identifying cutomers who are willing to buy but require the right marketing strategy. Overall this creates two key issues: wasted marketing budget and missed revenue oppurtunities. 
What decision can machine learning help the business make?
- Machine learning can help the business make decisions by identifying which customers should receive follow-up marketing attention. According to the Business Plan file, the machine learning model will execute the following:
- Identify customers who are more likely to convert after a campaign.
- Support campaign budget allocation across channels such as Email, Social Media, Search Ads, Display Ads, and SMS.
- Understand which customer behaviors and campaign features are most strongly related to conversion.
- Give managers an interpretable decision-support tool using a Decision Tree model. 
What is the target variable in the dataset?
- The target variable in this dataset is whether the customer will convert. 
- Yes = customer converted
- No = customer did not convert
What are the input features?
- Customer demographics: Age, Annual_Income, Region
- Customer relationship: Customer_Segment, Loyalty_Score, Customer_Satisfaction
- Campaign information: Campaign_Channel, Campaign_Type, Discount_Offered_Percent, Ad_Exposure_Count
- Engagement behavior: Email_Opened, Ad_Clicked, Website_Visits_Last_30_Days, Social_Media_Engagement_Score
- Purchase history: Previous_Purchases, Average_Order_Value, Days_Since_Last_Purchase, Prior_Campaign_Response
Why is this prediction useful for the business?
- This prediction is useful because it will help the business decide where to spend money depending on which customers require follow-ups and also help to identify which campaign strategy is most effective. Overall, this prediction will help for better targeting, budget control, campaign improvement, customer experiences, and business commmunications. 

## Task 2: Prepare the Data 
Dataset Used: marketing_campaign_decision_tree_dataset
Dataset was downloaded as an .xls file and converted to a .csv file to be used on Jupyter Notebook for assignment 4.
The dataset contains information such as Customer_ID, Campaign_Date, Age, Annual_Income, Region, Campaign_Channel, etc. 
Steps Completed: 
1. Load the dataset
2. Inspect the dataset
3. Check the number of rows and columns
4. Check data types
5. Check missing values
6. Check duplicate rows
7. Clean the dataset if needed
8. Separate features and target variable
9. Handle categorical and numerical variables if needed
10. Split the data into training and testing sets

## Task 3: Train a Decision Tree Classification Model
Machine-Learning Model Used: Decision Tree Classification Model

## Task 4: Business Interpretation of Model Results
How well did the Decision Tree model perform?
- The decision tree model performed moderately well given it has an accuracy of around 0.6. 
Is there a large difference between training accuracy and testing accuracy?
- Training accuracy: 0.600
- Testing accuracy: 0.597
- No, there is minimal difference between the two. 
Does the model show signs of overfitting? Why or why not?
- The model does not show signs of overfitting because the training and testing accuracy is almost the same value (very close in range, less than 0.01 difference)
Which evaluation metric is most important for this business problem?
- Recall is the most important evaluation metric in this case because we want to find the number of actual customers who converted. By doing so, the business can then identify the customers who are likely to convert and should not be overlooked. 
What do false positives mean in this business context?
- A false positive would mean a customer is showing that will convert, but does not. 
What do false negatives mean in this business context?
- A false negative mean a customer is showing that will not convert, but does. 
Which features were most important in the Decision Tree model?
- The most important features were Loyalty Score, Social_Media_Engagement_Score, and Annual_Income. 
How can these important features help the business make better decisions?
- These features can help the business make better decisions. For instance, Loyalty score can help the business understand which customers should recieve premuium offers.
What is one possible limitation or bias in the model or dataset?
- One of the possible limitations to this dataset is the small sample size. The data currenly shows 600 conversions which may not be an adequate number to fully represent conversion predictions. 
Why should human judgment still be used when making business decisions based on model results?
- Human judgement should still be used when making decisions based on model results because some features or factors may require further interpretation. The business must take into account bias and specific personal attributes of customers. 
