# credit-risk-classification
Repository for Module 20 Challenge

## Overview of the Analysis

In this analysis, we utilized a dataset of hisotrical lending activity from a peer-to-peer lending services company to build a model that coud identify the creditworthiness of borrowers.  The financial information in the dataset included the following information:

* loan size
* interest rate
* borrower income
* debt to income
* number of accounts
* derogatory marks
* total debt
* loan status

The model was designed to predict whether a loan would be healthy (0) or high-risk (1) based on the financial information available for a particular borrower.  To create the model, we first separated the target variable (healthy or high-risk) from the features variables (financial information listed above).  We split the data into training and testing datasets and then fit a logistic regression model to execute the predictions.  The ratio of healthy to high-risk loans in the training set was fairly skewed, so we used a resampling method that uitlized the Random Oversampler to account for that discrepancy. 

## Results

* Machine Learning Model 1 (Logistic Regression):
  * Accuracy: 94%
  * Precision: 100% for healthy loans, 87% for high-risk loans
  * Recall: 100% for health loans, 89% for high-risk loans

* Machine Learning Model 2 (Logistic Regression with Resampled Data):
  * Accuracy: 99%
  * Precision: 99% for healthy loans, 100% for high-risk loans
  * Recall: 100% for healthy loans, 99% for high-risk loans
  
## Summary

Based on the results outlined above, I would recommend the machine learning model that uses the resampled data.  While Model 1 is returning 100% precision for predicting healthy loans, it is only returning 87% precision for high-risk.  In my opinion, this is not accurate enough to predict whether a loan has a high probability of defaulting.  Model 2, however, returns extremely high precision scores for both loan categories.  In this scenario, predicting both health and high-risk loans is equally important.  Model 2 can be used with confidence to do this.

