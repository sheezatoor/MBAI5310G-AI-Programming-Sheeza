# Week [08] – [Assignment8: Natural Language Processing Pipeline and Text Classification]

## Files in This Folder
- Assignment8_MBAI5310G_SheezaToor.ipynb: main notebook for the task
- outputs/
- NLP-data_description.md: dataset provided by instructor 

## Task Overview
- Build a basic Natural Language Processing pipeline using Python
  
## Task 1: Load and Inspect the Dataset
Load your dataset into Python and inspect it.
You should include:
Dataset shape
Column names
First few rows
Missing values
Target variable distribution

Explain what each important column means.
- Feedback ID refers to the unique ID code for each text record
- VisitDate refers to the date the message/text was recieved
- Channel refers to the source of the text record (ie: Google review, Mobile App, etc)
- City refers to the city connected to the record
- AttractionArea refers to the attraction area related to the feedback (ie: aquarium)
- VisitorType refers to the visitor group
- VisitorFeedback refers to the raw message/text
- FeedbackCategory refers to the main classification category
- VisitorRating refers to the rating by visitors on a numerical of 1 to 5

- Visitor Feedback is the main text column to be processed 

## Task 2: Text Preprocessing
Choose the main text column and apply basic NLP preprocessing.

You should complete the following steps:
Convert text to lowercase
Remove punctuation
Remove stopwords
Tokenize the text
Apply stemming or lemmatization
Create a cleaned text column

After preprocessing, explain how the text changed and why preprocessing is important.
The text changed by applying lowercase to each word, removing stopwords like a, an, the, tokenizing the text by breaking down the words into smaller text and applying stemming and lemmatization to reduce presence of suffixes and prefixes as well as reducing words to their meaningful form. For instance: 

We convert: 
We liked the children's meal options

To this: 
liked child meal option

## Task 3: Exploratory Text Analysis
Analyze the text data using simple NLP techniques.

You should include:
Most common words
Word frequency distribution
At least one visualization, such as a bar chart of frequent words
A short interpretation of the most common words

Explain what the frequent words tell you about the dataset and the business problem.
Citymuseum is the most common word followed by ticket, child, staff, parking. Based on these keywords it seems the dataset focuses on visitor experiences. The business problem can be highlighted through these keywords. Perhaps there is a need to address operational aspects of that business that affect visitor experience. 

## Task 4: POS Tagging and Named Entity Recognition
Select at least three example text records from your dataset.

For each example, apply:
POS tagging
Named Entity Recognition, if possible

Then explain:
Which words are nouns, verbs, or adjectives
- Example 1
nouns: ticket, line, citymusuem
adjectives: bought
adverb: long, even

- Example 2
nouns: meal, option, machine, broken
adjectives: child
verbs: liked, drink

- Example 3
nouns: coffee, shop, event
adjectives: evening
verbs: closed, ended

Whether any names, locations, brands, organizations, or dates were detected
No names, locations, brands or organizations were detected. The only location detected was city museum but it was tagged as a noun perhaps to lower capitalization. 

How this information could be useful in business text analysis
- Pos-tagging could help the business identify main issues and opinions within the text by extracting nouns and verbs. 
- Named Entity Recognition could help the business identify specific locations and customer preferences of locations within the text/comments. 

## Task 5: Feature Extraction
Convert the cleaned text into numerical features using one of the following methods:
Bag of Words
or
TF-IDF

Explain why text must be converted into numbers before using a machine learning model.

Machine learning models use algorithms developed through numbers. Some algorithms include linear regression, neural networks, or decision trees. These numerical calculations cannot be applied to text, therefore it is necessary to convert the text into numbers. 

## Task 6: Build a Text Classification Model
Use the text features to train a simple classification model.

You may use one of the following models:
Naive Bayes
Logistic Regression
Decision Tree
Random Forest

** Decision Tree Model was used **

You should:
Define X and y
Split the dataset into training and testing sets
Train the model
Make predictions
Evaluate the model

## Task 7: Model Evaluation
Evaluate your model using appropriate classification metrics.
You should include:
Accuracy
Confusion matrix
Classification report

Then explain the result in simple business language.
For example:
What does the accuracy mean?
- Training accuracy: 57.1%
- Testing accuracy: 33.3%
- Overall the accuracy results are low which indicates underfitting. This means that the model can not efficiently detect patterns within visitor feedback.
Which class was predicted better?
- The model performed best on Parking and Ticketing. 
What type of mistakes did the model make?
- The model could not properly classify different categories with similar words
- Feedback texts/comments were assigned the wrong category 
Why could these mistakes matter for the business?
- These mistakes can affect the business because the business will not correctly interpret the results and this will lead to them solving the wrong issues or adressing issues that don't exist because the data was modeled incorrectly. Accurate classification is important so that businesses can use their resources efficiently to solve exact problems. 
  
## Task 8: Business Interpretation
At the end of your notebook, write a short business interpretation.

Your explanation should include:
What the model is trying to predict
- The model is predicting the specific feedback category for visitor texts/comments
What dataset you used
- I used the data provided by the instructor
What text column and target variable you selected
- My main text column was VisitorFeedback & my target variable was FeedbackCategory
What preprocessing steps you applied
- Load the data, check shape, columns, and info, clean the data, tokenize the VisitorFeedback column, lemmatize and stem, and lastly create bag of words. 
What model you used
- I used the decision tree model. 
What result you obtained
- Training Accuracy: 0.57
- Testing Accuracy: 0.33
- Accuracy: 0.33
- Precison: 0.32
- Recall: 0.33
- F1-Score: 0.28
One business insight from the text data
One limitation of your model or dataset
