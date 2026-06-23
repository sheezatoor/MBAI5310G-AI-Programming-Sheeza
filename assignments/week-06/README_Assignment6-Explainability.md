# Week [06] – [Assignment6: Model Evaluation, Explainability, and Fairness Reflection]

## Files in This Folder
- Assignment6_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/
- Explainability-data_description.md: dataset provided by instructor 

## Task Overview
- Evaluate a machine learning classification model, explain its predictions, analyze its errors, and reflect on fairness and bias.

## Task 1: Load and Understand the Dataset
Students must load and inspect the dataset.
The submission must include:
Dataset size
Column names
Data types
Missing values
Duplicate records
Target variable distribution

Students must write a short explanation describing the dataset, the target variable, and whether the target variable is balanced or imbalanced.

The dataset seems to hold financial information including invoice amounts, payment term days, client satisfaction score etc. of various customers from various locations and age ranges. The target variable in this case invoice_paid_late suggesting that the data is looking at whether customers paid their invoices or not as outlined by its binary classification of 0 & 1 in the dataset (1=yes, paid late, 0=no, not paid late). Based on the target distribution, 58.6% of customers paid on time (0) while 41.4% paid late (1). This shows a balanced target variable as the difference is small. 

## Task 2: Define Features and Target Variable
Students must define the input features and the target variable.

The submission must explain:
Which column is the target variable
- invoices_paid_late
Which columns are used as input features
- client_age
- client_type
- industry
- contract_type
- invoice_amount
- payment_term_days
- previous_late_invoices
- number_of_previous_invoices
- days_since_last_invoice
- client_satisfaction_score
- reminder_emails_sent
- auto_payment_enabled
Which columns were removed from the model input
- invoice_id
Which columns are kept only for fairness reflection
- age_group
- gender
- region

Students must remove identifier columns and should not use fairness/group columns directly as model input.

## Task 3: Data Preprocessing
Students must prepare the dataset for machine learning.
The submission must include:
Handling missing values
Converting categorical variables into numerical format
Preparing the final feature set for model training

Students must explain why preprocessing is necessary before training a machine learning model.

Preprocessing is necessary to prepare the data for a machine learning model. for insrance, most machine learning models use numerical data, it is therefore important to convert categorical columns into numerical ones so the data can be ready for processing. Likewise, handling missing values reduces the chance of skewed or biases results. To add on, we also remove fairness columns for the machine learning model as they can be used later for fairness and bias reflection as outlined in our Week6 lecture notes. 

## Task 4: Train/Test Split
Students must split the dataset into training and testing sets.
The submission must include:
Size of the training set
- 0.8 (80% of data goes into training)
Size of the testing set
- 0.2 (20% of data goes into testing)

Explanation of why the dataset is divided into training and testing data
Students must explain the difference between training data and testing data.

The dataset is divided into traning and testing data to observe model efficiency. Essentially after training the model on the training data, we want to examine how the model interprets new and unseen data. To do so, we train the model using 80% of the data and then keep the remaining 20% for testing. In training data, the model learns and in the testing data the model is evaluated. 

## Task 5: Train a Classification Model
Students must train a simple Decision Tree classification model.
The submission must include:
Model training
Model prediction on the test data
A comparison table of actual and predicted values

Students must explain what the model is trying to learn and whether the first few predictions are correct or incorrect.

The model is trying to learn patterns from X_train and y_train. It uses important parameters such as max_depth and random_state to outline tree growth and reproducibility. 
Based on the comparison table in the week-06 outputs folder, out of the first five preditions, 4 of them were correct while one was incorrect. There was actual late invoice payment but the model detected it as not late invoice payment. 

## Task 6: Evaluate the Model
Students must evaluate the model using classification metrics.
The submission must include:
Accuracy
Precision
Recall
F1-score

Students must explain the meaning of each metric in simple language and identify which metric is most important for their business problem.

- Accuracy: refers to the percentage the model predicted correctly, according to the metrics output, the model has an accuracy of 72.6% (mostly correct). 
- Precision: refers to the percentage of predictions that were actual late invoice payments, according to the metrics output, 67.9% (correct by 67%). 
- Recall: refers to the amount of correctly identified late invoice payments out of the total actual amount of late payments, according to the metrics output, the recall was 63.3%. (model finds 63.3% of all late payments). 
- F1-Score: refers to the calculated outcome between precision and recall, according to the metric output, it was 65.5% (signifies ok to good performance. 

Recall is the most important metric for this business problem because the business would like to identify correctly identified late payments (true positives) to be able to handle as soon as possible. 

## Task 7: Confusion Matrix
Students must create and interpret a confusion matrix.
The submission must include:
Confusion matrix table
Confusion matrix visualization
True Negative
False Positive
False Negative
True Positive

Students must explain the business meaning of false positives and false negatives. They must also discuss which type of error is more serious for their dataset.

In this business problem, false positives refer to payments that were flagged for being late but were not actually late and false negatives refer to payments that flagged for being NOT late but were actually late payments. For this dataset,  a false negative would be a more serious concern becaise we are looking for actual late payments and if the model labels an actual late payment as NOT late, that can have big financial consequences. 

## Task 8: Error Analysis
Students must analyze the model’s wrong predictions.
The submission must include:
Actual values
Predicted values
Correct or incorrect prediction status
Error type for each prediction
Count of each error type
Visualization of error type counts
A table showing wrong predictions

Students must explain the most common error type and its business impact.

In this business problem as seen by the Error Type plot in the outputs folder, the most common error type is true negatives which means the business is not to properly detect payments that are actually NOT late. The business impacted of this is that the model can recognise on time payments and this reduces focus on those payments and helps to better isolate the actual LATE payments instead. 

## Task 9: Cross-Validation
Students must apply cross-validation to evaluate the stability of the model.
The submission must include:
Accuracy score for each fold
Mean cross-validation accuracy
Standard deviation
Visualization of cross-validation results

Students must explain whether the model performance is stable across different folds.

The model has varying accuracy across the a five folds which means that it is not completely stable. However, the accuracy is between 0.70 to 0.75 which means it is a good level which shows the model is not completely random. 

## Task 10: Overfitting and Underfitting Analysis
Students must compare training performance and testing performance.
The submission must include:
Training accuracy
Testing accuracy
Comparison of model performance with different tree depths
Visualization of training and testing accuracy

Students must explain whether the model shows signs of overfitting or underfitting.

The chart shows overfitting because the training accuracy line in blue increases as the model tree gets deeper whereas the testing accuracy remains lower and sometimes increases and decreses as it goes into further depth. Higher training accuracy compared to testing accuracy is a signal of overfitting which can be seen in this Overfitting/Underfitting output. 

## Task 11: Feature Importance
Students must analyze which features are most important in the model.
The submission must include:
Feature importance table
Top important features
Feature importance visualization

Students must explain the business meaning of the most important features. They must also mention that feature importance does not prove cause and effect.

The most important features include invoice_amount, previous_late_invoices and number_of_previous_invoices. Invoice is most important because it shows the number of invoices within the business and higher amounts could mean higher late invoice payments. Previous late payments also helps to identify previous behaviours and helps to foreshadow how many late payments roughly the business could expect. Similarly again, the number of previous invoices can help the business detect previous patterns and help to predict future outcomes. However, it is important to clarify that feature importance only predicts model behaviour not cause of problem. 

## Task 12: SHAP Explanation
Students must use SHAP to explain the model.
The submission must include:
SHAP summary explanation
- This summary bar plot portrays the impact of each feature and its average on late payment prediction. Longer bars suggest greater effects on the output. The most important feature on the SHAP bar plot is previous_late_invoices which means historical payment behaviour has the most effect in prediciting whether a payment is late or not.
SHAP explanation for one individual record
- The most influential feature for this invoice is record is previous_late_invoices. The positive SHAP values push the feature to late payments while negative SHAP values push the feature to NOT late payment. 
Interpretation of how important features affect the prediction
- The strongest SHAP values were negative, this allows us to interpret the prediction as NOT late payment. 
Students must explain how SHAP helps us understand the model beyond basic feature importance.
- SHAP helps us understand the model beyond basic feature importance by narrowing down on single records and helping us understand why a specific prediction becomes the outcome for a record. 

## Task 13: LIME Explanation
Students must use LIME to explain one individual prediction.
The submission must include:
Prediction probability for one selected record
LIME explanation table or visualization
Interpretation of features supporting the prediction
- The green bars show features that support the prediction
- The strongest features supporting the prediction are invoice_amount. 
Interpretation of features working against the prediction
- The red bars show features that work against the prediction
- The strongest features working against the prediction are number_of_previous_invoices. 
Students must explain how LIME can help business users understand one model prediction.
- LIME helps by showing the features that influenced the decision and how they increase or decreased the relative predictive outcome.
  
## Task 14: Fairness and Bias Reflection
Students must analyze model performance across different groups.
The submission must include fairness analysis for at least two group-related columns.
For each group column, students must report:
Number of records in each group
Actual positive rate
Predicted positive rate
Accuracy by group
Students must also include visualizations comparing model behavior across groups.

Students must reflect on whether the model performs equally across groups and whether the results may create unfair business decisions.

It seems that the model may have higher accuracy for males than females. This can be the result of bias and can also lead to unfair business decisions. It could perhaps assume that one gender has higher tendency for late payments than another even if that may not be the case. It also seems that accuracy is higher for the age group of 36-50 compared to other age groups and higher accuracy for South region compared to other regions. 


## Task 15: Final Business Interpretation
Students must write a final business interpretation of the model results.
The final interpretation must discuss:

What the model predicts
- The model predicts whether an invoice is paid late or  not. 
Overall model performance
- Overall, the model performance at a moderate level. However, the training accuracy was 90% while the testing accuracy was 66% which may indicate overfitting. 
Most important evaluation metric
- The most important evaluation metric was Recall. As this shows us the amount of correctly identified late payments. This is our main target. 
Main error type
- The main error type was true negatives (actual NOT late payments). 
Business impact of model errors
- The model may help flag on-time payments and reduce false predictions.  
Overfitting or underfitting evidence
- The model shows overfitting as training accuracy is higher than testing accuracy. 
Most important features
- The most important features include invoice_amount, previous_late_invoices and number_of_previous_invoices
SHAP or LIME insight
- SHAP and LIME can help the business understand the effects of each feature and how much they impact the predictive outcomes. 
Fairness and bias concern
- Gender as a catergory may have potential bias as seen in the fairness and bias results. It is important for the business to understand this bias when addressing operational problems. 
Final recommendation
- This model should not be the only key decision-making system to improve business needs. It can be used as a predicitive model for planning future strategies to mitigate false positive risks and other issues. However, it is highly important to have human oversight in this model reflection to mitigate bias. Overall, the model provides useful insights and can be used to support decision making, however further improvements on training and testing would be beneficial. 
