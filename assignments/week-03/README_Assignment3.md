# Week [03] – [Assignment3: Classification Models & Evaluation Metrics]

## Task Overview
- Building a baseline model with Logistic Regression & SVM as a comparison model

## Files in This Folder
- Assignment3_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/Assignment3_LogisticRegressionOutput.png: screenshot of Logistic Regression Model Output
- outputs/Assignment3_SVMOutput.png: screenshot of SVM Model Output
- outputs/Assignment3_ConfusionMatrix_LogisticRegression.png: screenshot of confusion matrix for Logistic Regression Model
- outputs/Assignment3_ConfusionMatrix_SVM.png: screenshot of confusion matrix for SVM Model
- data_description.md: dataset provided by instructor 
  
## Dataset or Input Source
- Dataset was downloaded as an .xls file and converted to a .csv file to be used on Jupyter Notebook for assignment 3.
- The dataset contains customer information such as age, gender, city, income, website visits, ad clicks, etc.

## Methods Used/Steps Completed
1. Loading Data
2. Basic Data Preparation
3. Defining Features & Target
4. Train/Test Split
5. Defining Preprocessing
6. Build Logistic Model/SVM Model
7. Compare Actual & Predicted Values
8. Print Classification Metrics
9. Create Display Object for Confusion Matrix 

## Key Results
- Logistic Regression Model performed better given that more true positives and less false negatives than SVM Model as seen through the confusion matrix displays for both
- Recall is the most important metric in this task to identify responding customers.
- False positives would mean customers showing they responded when they did NOT.
- False negatives would mean customers showing they did not respond when they DID.

## Responsible AI Reflection
Human review would be needed before using the model in a real business context to account for certain biases or limitations. This model is only a learning example. It should not be used for real customer decisions without checking data quality, bias, fairness, privacy, and business consequences.

## How to Run or Review
1. Open the .ipynb file in GitHub or open Notebook in Jupyter 
2. Install required packages if needed
3. Run all cells from top to bottom
