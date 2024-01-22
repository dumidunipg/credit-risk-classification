
## Overview of the Analysis

The purpose of this analysis is to evaluate whether the linear regression model is able to identify the creditworthiness of borrowers based of loan status (healthy loans or high-risk loans).

Factors that were considered during the analysis were the size of the loan, the interest rate for the loan, the borrowers income, the debt to income ratio, the number of accounts each borrower had, derogatory marks against the borrower, and the total debt of each borrower.

In this dataset, 75,036 loans were considered to be healthy while 2500 were considered to be high risk loans. We were trying to see how accurate a logistic regression model would be at predicting whether a borrowers loan would be healthy or high-risk by splitting the original data into a testing set and a training set.

By separating the data into a training set and testing set, we are able to create a logistic regression model and fit the model using the training data. Then we make predictions using the testing data. We can use the balanced accuracy score which takes into account true positives and true negatives to see how well the model is able to predict both healthy and high risk loans. The confusion matrix provides more insight into how many true positives, true negatives, false positives, and false negatives there were for the predictions. Then the classification report is able to further provide measures for precision, recall, f1-score (precision and recall in a single value) for each of the labels (healthy loan or high risk loan). The classification report also provides the overall accuracy for the model.

Because the instances of healthy loans are very high compared to instances of high-risk loans in the dataset, we use oversampling to try and balance out the distribution between the two labels. By oversampling the data then running the logistic regression model, we are able to see even better if the logistic regression model can accurately predict high-risk loans and healthy loans so that we may be able to better generalize the model.


## Results

* Machine Learning Model 1:
  - Accuracy: 99% accurate at predicting both high-risk and healthy loans
  - Precision: Perfect at predicting healthy loans (100% accuracy) and is 87% accurate in predicting high-risk loans.
  - Recall: Perfect at predicting healthy loans (100% accuracy) and 89% accurate at predicting high risk loans.


* Machine Learning Model 2:
  - Accuracy: 100% accurate in predicting both high-risk and healthy loans.
  - Precision: 100% accurate in predicting healthy loans, 87% accurate in predicting high-risk loans.
  - Recall: 100% accurate in prediciting healthy loans, 100% accurate in predicting unhealthy loans.

## Summary

Logistic regression model 1 had a balanced accuracy score being at 0.944 (close to 1) suggests that this model is highly accurate at making predictions. From the confusion matrix, we are able to see that there are 558 true positives redicted or high risk loans correctly predicted and there are 18,679 true negatives or healthy loans correctly predicted compared to false positives (healhty loans incorrectly predicted) which is 80 and false negatives (high-risk loans incorrectly predicted) which is at 67. From the confusion matrix we can see that the true positives and true negatives are much higher compared to the false positives and false negatives suggesting this is a good model.From the classification report we see that the precision, recall, and F1-Score is 1.00 for healthy loans suggesting it is very good at predicting the healthy loans class. For high-risk loans class, the precision is 0.87, the recall is 0.89 and f1-score is 0.88 suggesting that it is also pretty good at predicting the high-risk loans class. The overall accuracy from the classification report is 0.99 suggesting that the logistic regression model can predict both healthy loan and high-risk loan labels very well. 

However, logistic regression model 2, performs even better than logistic regression model 1. The balanced accuracy score for the oversampled data increased to 0.996 which indicates that the model is very accurate at predicting both the healthy loans and high-risk loans for the oversampled data. The confusion matrix indicates that there were 623 true positives or correctled predicted high risk loans, 18668 true negatives or correctly predicted healthy loans, 91 false positives or incorrectly predicted healthy loans, and 2 false negatives or incorrectly predicted high risk loans. Since the true positives and true negatives highly outnumber the false positives and false negatives, we can conclude that the model is highly accurate. This is also supoorted by the classification report which indicates a perfect precision, recall and f1-score of 1.00 for the model when predicting healthy loans for the oversampled data and similar high values of 0.87, 1.00, and 0.93 for precision, recall, and f1-score when predicting high-risk loans for the oversampled data. The classification report indicates a perfect accuracy of 1.00. The logistic regression model performs very well for predicting both healthy and high-risk loans when fit with oversampled data. 

Logistic regression model 2, with the oversampled data seems to perform best because the accuracy increased to 100% accurate for predicting both healthy and high-risk loans.

It is more important to predict the high risk loans because a high risk loan that is incorrectly predicted as healthy would put the borrower in more debt and their creditworthiness will go down. Therefore, the increased accuracy of logistic regression model 2 is necessary to avoid false negatives.


