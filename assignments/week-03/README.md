# Week [03] – [Assignment2: End-to-End Machine Learning Pipeline]

## Task Overview
- Using customer information and website behaviour to predict whether a customer will respond.
- This project builds a beginner machine learning pipeline to predict customer response behavior.

## Files in This Folder
- Assignment2_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/Assignment2_Output.png: screenshot of Pipeline output 
- data_description.md: dataset provided by instructor 
  
## Dataset or Input Source
- Dataset was downloaded as an .xls file and converted to a .csv file to be used on Jupyter Notebook for assignment 2.
- The dataset contains customer information such as age, gender, city, income, website visits, ad clicks, etc. 

## Methods Used/Steps Completed
1. Loading Data
2. Basic Data Preparation
3. Defining Features & Target
4. Train/Test Split
5. Defining Preprocessing
6. Building Baseline Model
7. Training Model
8. Predicting Test Set
9. Evaluating Model. 

## Key Results
- Accuracy of 0.783: 78% of predictions are accurate
- No imbalance between Yes responses & No responses; 30 samples each
- Balanced datatset: Macro & Weighted averages are similar

## Responsible AI Reflection
Human review would be needed before using the model in a real business context to account for certain biases or limitations. This model is only a learning example. It should not be used for real customer decisions without checking data quality, bias, fairness, privacy, and business consequences.

## How to Run or Review
1. Open the .ipynb file in GitHub or open Notebook in Jupyter 
2. Install required packages if needed
3. Run all cells from top to bottom
