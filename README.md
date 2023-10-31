# Credit_Card_Approvals_and_Denials_Prediction

## Overview
This project attempts to create the best possible binary classification model that can predict whether or not a given individual will qualify for a new credit card based on 17 factors. The data can be publicly accessed through [kaggle](https://www.kaggle.com/datasets/rohitudageri/credit-card-details?select=Credit_card.csv), although no explaination was given as to how it was assembled or curated. The data is not included in this repository to simulate industry best practices. The goal of this project is to make the most accurate possible classifier model with the given data, with consideration for the specific business use case.

## Business Problem
Approving credit card applications can be a difficult and time consuming process, but using data on previous approvals, we can easily and quickly determine whether or not the bank should approve new applications. This can potentially save financial institutions a significant amount of time, money, and manpower. The coefficients or model weights of the final model may be used to make recommendations about important threshholds in the predictor variables which can be used to guide the approval process. When creating these models, we must be careful to minimize the false positives our model produces, as they are the worst outcome for this purpose and can cost the bank money.

## Data Explanation
For each record, the data contains:
 - The gender of the applicant
 - Whether the applicant owns a car
 - whether the applicant owns a house or condo
 - The number of children the applicant has
 - The applicant's annual income
 - The source of the applicant's income
 - Highest level of education achieved by applicant
 - Marital status of the applicant
 - Housing type of applicant (if applicable)
 - A backwards count to the applicant's birthday starting at the day the data was created
 - A backwards count to the day the applicant became employed (positive value means number of days they have been unemployed)
 - Whether or not the applicant has a mobile phone
 - Whether or not the applicant has a work phone
 - Whether or not the applicant has any other phone number
 - Whether or not the applicant has an email ID
 - The type of occupation of the applicant
 - The number of family members the applicant has
 - Whether or not the application was approved

The dataset is rather small, with only 1500 records. This sort of small dataset is unlikely to produce a highly effective model, but it can at least be used to draw inference about what sort of applicants banks should immediately consider approving. The labels are stored in a separate file from the predictors, so we will have to merge them together to ensure the records stay aligned with their labels as we handle missing values and tweak the data.

## Methodology
The methodology of this study was to exhaustively experiment with different combinations of model type, hyperparameters, and minority oversampling techniques. While experimenting with model types resulted in progressive increases in performances, ultimately the default parameters yielded the best results, and minority oversampling did not yield an increase in performance.

## Best Model
The best model produced in this notebook was a random forest classifier model with the default parameters. It recieved a precision score of 0.786, an F1 score of 0.458, and AUC of 0.657 when evaluated on the testing data, which are all significantly better than the scores of the other model types experimented with.

## Results

## Conclusions

## Next Steps