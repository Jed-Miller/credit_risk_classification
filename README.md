# credit_risk_classification

## Overview of the Analysis

In this Challenge, the goal was to use various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer lending services company, we built a model to identify the creditworthiness of borrowers.

## Data Factors 

* Loan size
* Interest Rate
* Income fo Borrower
* Borrower's Debt Amount to Income
* Number of Accounts for borrower
* Derogatory marks against borrower
* Borrower's total debt

## Logistic Regression Model Testing

From the initial dataset (77,536 data points), a labels set was created from the 'loan_status" column while the other columns became the features set. The two labels within the label set were 'healthy loan' and 'high-risk loan'. These data points were split into a training and testing sets and a logistic regression test was run using the LogisticRegression module from sklearn to see how determine the model's accuracy and precision when predicting the  loan risk of each borrower.

One issue of the initial dataset is the imbalanced nature of the dataset, with 75,036 'healthy loan' data points and 2,500 'high-risk loan' data points. Considering this imbalance, the data set was rebalanced using the RandomOverSampler module from imblearn. The resampling generated 56,271 data points for each of the healthy and high-risk loans.

With the resampled data points, another logistic regression test was run. Again, the purpose of the test was determine the model accuracy and precision when predicting a borrower's loan rick.

## Results


Machine Learning Model with Initial data set:
  * Accuracy Score: 95.2%
  * Precision Scores:
       * Healthy Loan: 100%
    * High Risk loan: 85%
  * Recall: 95%  (macro average) 
<br>
Machine Learning Model with Resampled data set:
* Accuracy Score: 99%
* Precision Scores:
    * Healthy Loan: 99%
    * High Risk loan: 99%
* Recall: 99% (macro average)

## Summary

Based on the results from the two tests, my recommendation would be to use logistic regression model using the resampled data set. While both tests have high accuracy and recall scores, the resampled test performs significantly better (99% vs. 85%) when precisely evaluating false negatives. This would allow loan officers to effectively identify high risk loan applications and mitigate risk when approving different loans.





