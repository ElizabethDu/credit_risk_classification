# Module 20 Report Template

## Overview of the Analysis

The purpose of this analysis was to build a machine learning model to predict loan defaults 
using historical financial data from a peer-to-peer lending platform. We aimed to 
create a model capable of predicting whether a borrower would default or 
fully repay a loan, based on various borrower characteristics, such as:

* Loan size
* Interest rate
* Borrower income
* Open lines of credit
* Prior derogatory credit marks
* Total outstanding debt

The target variable in this dataset was the loan_status, with 0 representing a healthy loan (fully paid) and 1 representing a defaulted loan. We needed to predict whether a 
loan would default based on these features.

The machine learning process followed several key steps:

* Data preprocessing: This involved separating the loan_status field from the rest of the dataset, splitting the data into training (75%) and testing (25%) datasets.
* Model creation: We used Logistic Regression to train a model that would find trends between loan and customer credit details and the outcome of the loan (healthy vs. default).
* Model evaluation: After training the model, we evaluated its performance on the test data, calculating metrics such as accuracy, precision, and recall to gauge its predictive power.

## Results
Logistic Regression Model:
Accuracy:
    99% of test cases (19,238/19,384) were correctly predicted.

Precision:
    Healthy loans: 99% of loans predicted as healthy were healthy.
    Defaulted loans: 94% of loans predicted as defaulted were risky.

Recall:
    Healthy loans: Nearly 100% of healthy loans were correctly identified.
    Defaulted loans: 84% of defaulted loans were correctly identified.

F1-Score:
    Healthy loans (0): 1.00
    Defaulted loans (1): 0.89
    Macro average: 0.94
    Weighted average: 0.99

## Summary
The Logistic Regression model performed exceptionally well in predicting loan outcomes, with an overall accuracy of 99%. It was particularly good at predicting healthy loans, 
with a precision and recall of 99% and nearly 100%.

However, the model struggled somewhat with identifying defaulted loans, as it misclassified 16% of defaulted loans as healthy. Despite this, the model achieved strong overall 
precision (94%) and recall (84%) for defaulted loans.