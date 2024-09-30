# credit-risk-classificationcredit-risk-classification
Background
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

Instructions
The instructions for this Challenge are divided into the following subsections:

Split the Data into Training and Testing Sets

Create a Logistic Regression Model with the Original Data

Predict a Logistic Regression Model with Resampled Training Data

Write a Credit Risk Analysis Report

Split the Data into Training and Testing Sets
Open the starter code notebook and use it to complete the following steps:

Read the lending_data.csv data from the Resources folder into a Pandas DataFrame.

Create the labels set (y) from the “loan_status” column, and then create the features (X) DataFrame from the remaining columns.

note
A value of 0 in the “loan_status” column means that the loan is healthy. A value of 1 means that the loan has a high risk of defaulting.

Split the data into training and testing datasets by using train_test_split.

Create a Logistic Regression Model with the Original Data
Use your knowledge of logistic regression to complete the following steps:

Fit a logistic regression model by using the training data (X_train and y_train).

Save the predictions for the testing data labels by using the testing feature data (X_test) and the fitted model.

Evaluate the model’s performance by doing the following:

Calculate the accuracy score of the model.

Generate a confusion matrix.

Print the classification report.

Answer the following question: How well does the logistic regression model predict both the 0 (healthy loan) and 1 (high-risk loan) labels?

Report: Overview of the Analysis
Explain the purpose of the analysis. The purpose of this analysis is to develop a model for credit risk classifications based on financial information to predict whether a loan applicant is likely to have a healthy loan or a high-risk loan, meaning if they are likely to default on payments or not.

Explain what financial information the data was on, and what you needed to predict. The data showed financial information for each applicant and loan including: loan size, interest rate, income, debt-to-income ratio, number of accounts, any derogatory marks, and total debt. This information was used to predict if the applicant was likely to default on their loan payment (making it a high-risk loan).

Provide basic information about the variables you were trying to predict (e.g., value_counts). The variable the model is trying to predict is the loan status, and the 2 possible outcomes are a "healthy loan" or a "high-risk loan". When looking at the breakdown of those status variables, there are more observations of healthy loans (75036) than high-risk loans (2500).

Describe the stages of the machine learning process you went through as part of this analysis. This machine learning process started with data cleaning and some exploratory analysis to view the data being worked with, selecting the X and y features for testing, splitting test and training datasets, fitting the model and working with the test sample to evaluate the accuracy and other metrics.

Briefly touch on any methods you used (e.g., LogisticRegression, or any resampling method). LogisticRegression was used with both samples to classify the feature we were predicting (loan_status). LogisticRegression is a binary classification algorithm. A RandomOverSample was used to resample the data and create an even spread between the imbalanced data set, so there were equal observations of each loan status outcome.

Results
Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Machine Learning Model 1:

Accuracy: 99%
Precision: 93%
Recall: 95%
Machine Learning Model 2:

Accuracy: 99%
Precision: 93%
Recall: 99%
Summary

Both models perform well, and predict both '0's and '1's with 99% accuracy. 
Model 2 has a slightly better recall score than Model 1 for predicting 1's, which are the high-risk loans, so I would recommend using Model 2 for tihs process. 
It feels more important to correctly predict high-risk loans than to correctly predict healthy loans for this particular problem.