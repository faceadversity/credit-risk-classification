# Module 12 Report Template

## Overview of the Analysis

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

The balanced accuracy score for this model is approximately 99%. Low-risk loan predictions [`0`] comes at a higher rate and similar recall values (100%, 99% respectively) compared to high-risk loans [`1`] (84%, 99% respectively) making this model similarly well suited for predicting the likelihood of healthy loan labels. The prediction for high-risk loans has a bit more accuracy in this model compared to the first. In the confusion matrix we see there were 4 false positives, and 116 false negatives.

## Summary

Going off the balanced accuracy score and recall values, the second model is a bit more accurate at predicting high-risk loans [`1`] while both models are well suited at predicting low-risk loans [`0`]. Model 2 in this regard gets a very slight advantage once again for low-risk loans having the more pinpoint balanced accuracy score at roughly 99%. When it comes to numbers pertaining to false positives, the second model has a major advantage here with 4 false positives compared to the first at 56. In conclusion I would recommend using machine learning model 2 since the Logistic Regression with Resampled Data model has better performing scores on average across the board.
