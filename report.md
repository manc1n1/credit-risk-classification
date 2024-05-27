# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

-   The purpose of this analysis is to train and evaluate a model based on loan risk. We did this using a dataset of historical lending activity from a peer-to-peer lending services company to build this model that can identify the creditworthiness of borrowers.
-   The target values of `loan_status` are `0` (healthy loan) and `1` (high-risk loan). `0` has a `value_count` of `75036` and `1` has a `value_count` of `2500`.
-   The stages of the machine learning process in this analysis included:
    -   Splitting the data into labels and features. With labels representing a healthy or high-risk loan and the remaining columns being the features DataFrame.
    -   The data was then split into training and testing datasets.
    -   A Logistic Regression model was then created with the original data.
        -   Fit the model by using the training data.
        -   Save the predictions on the testing data labels by using the testing feature data and the fitted model.
        -   Evaluate the model’s performance by doing the following:
            -   Generate a confusion matrix.
            -   Print the classification report.

## Results

**Logistic Regression:**

```sh
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     18759
           1       0.87      0.95      0.91       625

    accuracy                           0.99     19384
   macro avg       0.94      0.97      0.95     19384
weighted avg       0.99      0.99      0.99     19384
```

-   The Logistic Regression Model predicts healthy loans with 100% accuracy and high-risk loans with a lower accuracy of 87%. This wouldn't be a good enough model to predict whether a high-risk loan is worthy since 13% is a big margin of error and could result in a big loss for the lending service.

## Summary

The Logisitic Regression model does a good job predicting healthy loans (`0`) with a precision of 100%. On the other hand it does do a decent job at predicting risky-loans (`1`) with a precision of 87%. This lower precision would not be good enough for a lending service since it leaves a 13% margin for error which could relate to big loss. This low precision could be due to the lack of support (625) vs the huge support for healthy loans (18759).
