# credit-risk-classification


## Overview of the Analysis

Using data from already existing loans, a bank or lender wants to create a model that will predict if a loan will yield good returns or not, otherwise known as "healthy" and "unhealthy". The data provided includes the loan amount/size, interest rate, borrower income, borrower debt-to-income ratio, the number of accounts/loans in their name, any derogatory marks on their credit report, the borrowers total debt, as well a the loan_status with healthy loans represented with a 0 and unhealthy loans with a 1. After reviewing the data I started by separating the loan_status into one variable otherwise known as the target, and the remaining data into a features variable. We will train and test our model by having it examine the features in an attempt to predict the target. Using the scikit-learn module and train_test_split the data was split into random training and testing subsets. I chose to use a LogisticRegression model (solver='1bfgs', random_state=1) and fitthat model with the training subset. The resulting model was able to use the features provided from each loan and correctly identify the loan_status 99% of the time and can be considered very effective.

## Results

* Machine Learning Model 1:
    * When predicting healthy loans (0) the model returned a precision score of 100%, a recall score of 99% and an f1-score of 100%
    * When predicting unhealthy loans (1) the model returned a precision score of 85%, a recall score of 91%, and an f1-score of 88%
    * The file contained 19,000+ examples of loans, however unhealthy loans made up only 3% of the data with just over 600 records. Therefore, the weighted averages for the overall results was slightly higher than the macro averages. However, both returned metrics that could be classify as very good or excellent.

## Summary

With excellent metrics overall, Machine Learning Model 1 can be considered highly effective, particlarly with predicting healthy loans. And while is precision for unhealthy loans is still very good, additional attention may be needed when reviewing potentially unhealthy loans. The model may be perfected with additional data/examples of unhealthy loans.

* The model has outstanding perforance when predicting helathy loans with perfect precision and near-perfect recall.
* While precision and recall are slightly lower for unhealthy loans, the metrics are still quite high and the results have a good f1-score.
* This model can be used to identify healhty loans based on application data with near-perfect accuracy. This will likely result in an increase in the number of approved loans and a decrease in time spent manually reviewing applications with minimal to no risk to the lender.
* The model's accuracy identifying unhealthy loans is good. It is worth noting that instances where the models prediction of an unhealthy loan was incorrect, those instances do not increase the risk to the lender, as those loans were instead considered healthy. With additional data representing unhealthy loans, this precision of this model could be improved.
