# Module 12 Report Template

## Overview of the Analysis

The analysis aimed at testing how well financial information can predict the creditworthiness of borrowers. The financial information included loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt of a borrower.

The model attempted to predict the creditworthiness of a borrower. The value of 1 means that the loan has a high risk of defaulting. The value of 0 means the loan has a low risk of defaulting. The machine learning process included:

(1) spliting the data into training and testing sets;
(2) creating a logistic regression model with the training data;
(3) making predictions for the testing data; and
(4) evaluating the model's performance by generating a confusion matrix and printing the classification report.

The scikit-learn modules used include train_test_split to perform (1) mentioned above, LogisticRegression to perform (2), and confusion_matrix and classification_report to perform (4).

## Results

The model did well in predicting the creditworthiness of borrowers. The classification report on the testing predictions is as follows:

              precision    recall  f1-score   support

   0 (low-risk)    1.00      0.99      1.00     18765
   1 (high-risk)   0.84      0.94      0.89       619

    accuracy                           0.99     19384
   macro avg       0.92      0.97      0.94     19384
weighted avg       0.99      0.99      0.99     19384

Precision: The precision ratios are high. All the instances predicted as low-risk were actually low-risk (100% precision). 84% of the instances predicted as high-risk are actually high-risk.

Recall: The recall ratios are high. 99% of the actual low-risk instances were correctly identified as low-risk. 94% of the actual high-risk instances were correctly identified as high-risk.

F1-score: The f1-score is the harmonic mean of precision and recall. For the low-risk class, the score indicates a very good balance. For the high-risk class, the score indicates a quite good balance.

Accuracy: The accuracy score is the overall percentage of correctly classified instances. With an accuracy of 99%, the model did very well on average across both low-risk and high-risk classes.

## Summary

Given the very high accuracy of the model in predicting creditworthiness of borrowers, I would recommend it for use by the company.