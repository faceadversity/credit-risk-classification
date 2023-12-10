# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* The purpose of this analysis is to use various machine learning techniques to train and evaluate a transgression model in determining the accuracy for healthy and high risk loans.
* The lending data provided includes the following: loan size, interest rate, borrower income, debt to income ratio, number of accounts, derrogatory marks, total debt and loan status.
* The general goal was to predict if a loan is healthy or high-risk.
* The target variable `y` is the `loan_status` which can be classified as 0 or 1 and our main focal point of predictive analysis. The healthy loan is represented by 0 while the high-risk loan is represented by 1.
* Stages of the Machine Learning Process includes the following:
  I. Data Collection and Preparation
  II. Model Preference
  III. Model Training
  IV. Model Prediction
  V. Model Utilization
* The Logistic Regression Model with the `random_oversampler` model was used to determine credit risk classification accuracy. The model's performance was evaluated based on the accuracy score.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Balanced Accuracy Score: 0.9520479254722232
  * Confusion Matrix:
    [[18663   102]
    [   56   563]]
  * Classification Report:

                   precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.85      0.91      0.88       619

    accuracy                           0.99     19384
   macro avg       0.92      0.95      0.94     19384
weighted avg       0.99      0.99      0.99     19384

The balanced accuracy score for this model is approximately 95%. Low-risk loan predictions [`0`] comes at a higher rate and recall (100%, 99% respectively) compared to high-risk loans [`1`] (85%, 91% respectively) making this model well suited for predicting the likelihood of healthy loan labels. In the confusion matrix we see there were 56 false positives, and 102 false negatives.

* Machine Learning Model 2:
  * Balanced Accuracy Score: 0.9936781215845847
  * Confusion Matrix:
    [[18649   116]
    [    4   615]]
  * Classification Report:

                  precision    recall  f1-score   support

           0       1.00      0.99      1.00     18765
           1       0.84      0.99      0.91       619

    accuracy                           0.99     19384
   macro avg       0.92      0.99      0.95     19384
weighted avg       0.99      0.99      0.99     19384

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:
* Which one seems to perform best? How do you know it performs best?
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )

If you do not recommend any of the models, please justify your reasoning.
