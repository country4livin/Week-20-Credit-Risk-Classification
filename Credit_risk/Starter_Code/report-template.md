# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis was to create a supervised machine learning model that would predict a person's credit risk by evaluating if a loan is healthy(paid-off) or high-risk(not paid). The data set was in a csv file that contained columns of loan data including the amount and interest rate, and the borrower's income, debt and accounts, as well as a column classifying the loan as healthy (0) or high-risk(1). There were 2,500 loans classified as high-risk.

To preform the machine learning process, the data was:

First, split data into labels and features, with the loan status (healthy or high-risk) being the label and the remaining seven columns as features.
The data was then split into training and testing data sets.
A Logistic Regression model from sklearn was created with the Limited-memory BFGS ('lbfgs') solver.
The Logistic Regression was chosen to classify loans as healthy OR high-risk.
The model was then fit with the training data.
Predictions were made with the test data.
The model was then evaluated by comparing the predictions with the test labels.


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model: Logistic Regression
    - Accuracy: .99
    - Precision: 
        - Healthy: 1.00
        - High-Risk: .84
    - Recall scores:
        - Healthy: .99
        - High-Risk: .94

## Summary
The Logistic Regression model does well at predicting healthy loans. However, according to the test data, the high-rish loans only have .84 precision, meaning some of them are classified as healthy. This could be problematic for the company because they would lose more money from a default loan than interest earned from the healthy loans.

There are not as many high-risk loans compared to healthy loans for the model to learn from, which can lead to some of the errors. So it would helpful if more high-risk loans were added to train the model better.

To solve the companies problem of default loans, it is more important to classify high-risk loans to prevent the significant loss that comes from defaults.
