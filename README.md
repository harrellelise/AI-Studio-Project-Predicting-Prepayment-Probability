*This is not only my work, these files are a collaboration of my team and our challenge advisors*
*The data we used is a product of Fannie Mae and can be found on their website at: https://capitalmarkets.fanniemae.com/credit-risk-transfer/single-family-credit-risk-transfer/fannie-mae-single-family-loan-performance-data*

# AI-Studio-Project-Predicting-Prepayment-Probability
This repository contains the collaborative work of my team and our challenge advisors during the Break Through Tech AI @ MIT AI student project. The goal of this project was to create a Machine Learning Model to predict prepayment probability concerning mortgages using data provided by Fannie Mae.

## Project Overview
We used Fannie Mae's Single-Family Loan Performance Data, which can be accessed at the link above. 

## Problem Statement
We focused on mortgages originated in 2018, tracking their status monthly until December 2022. The objective of the project was to predict potential borrower prepayment events to:

Maximize borrower assistance options.
Analyze pool-level behavior.
When a borrower prepays, the loan is terminated, which is why understanding prepayment events is crucial.

## Data Overview
Time Period: 2018-2022.
The dataset consists of time-series data, where each month has a separate .xlsx file. We combined all the files into one DataFrame and handled date conversion for the reporting periods.
## Data Preprocessing
Organized the time-series data, ensuring it was in chronological order.
One-hot encoded categorical features.
Created a prepay column that indicated whether a borrower had prepaid (i.e., when the balance code was set to 1, marking a prepay event).
## Model Creation
After preprocessing and splitting the data into training and testing sets, we initially created a decision tree model. The decision tree was highly complex and suitable for predicting individual loans, but we needed a model that could generalize better to pool-level behavior.

## Custom Evaluation Metric
We designed a custom metric to evaluate the model’s performance at a pool level. This metric calculated the mean error by taking the mean value of the predicted prepayment probability (y) and subtracting it from the mean value of the actual prepayment probability (y). This approach gave us better insights into the model’s behavior than standard accuracy scores.

## Model Adjustments
Through the evaluation process, we identified that we needed to increase the bias of the model to allow for better generalization, which would help in predicting pool-level behavior more effectively.
