# Customer Churn Prediction

## Business Problem

In a telecommunication company every month, the business loses clients, and we're not really sure why.  We may be able to take action to retain customers if we can identify which ones are most likely to depart in advance.  We have information about their phone plan usage, whether they have contacted customer support, the plans they are on, and other details.  The goal is to use this data to predict who’s likely to churn so the company can try to retain them before they go.

## Project Overview

This project aims to develop a predictive model to identify customers likely to churn (leave) from a U.S. telecommunications company

## Business Understanding

Some of our clients discontinue using this services each month, and we are not always sure why.  Over time, this leads to lower revenue and less devoted users.  We want to identify which clients are most likely to leave before they do in order to fix this problem.  We'll use data such as how frequently they've contacted customer service, what kind of plan they have, and how often they use their phone.  Early detection of these clients will enable the business to take steps to keep them on board, such as providing assistance or exclusive offers.

 Our prediction is whether a customer will depart (a situation known as churn).

 How we gauge success: We'll concentrate on a metric called recall, which indicates the proportion of consumers that actually departed that were accurately identified earlier
## Data Understanding

The SyriaTel dataset is available on Kaggle (https://www.kaggle.com/becksddf/churn-in-telecoms-dataset)

The dataset contains 3,333 customer records with 21 columns, the following key information:

Usage-related features: total day minutes, evening minutes, number of customer service calls

Plan-related features: voice mail plan, international plan

Demographics: area code, state

Target: churn (binary: 0 = no churn, 1 = churn)

Basic checks performed:

There were no missing values

We encoded categorical variables

## Modelling and Evaluation

Baseline Logistic Regression

Recall: 76.2%
(Could identify 76% of customers who actually churned)

Tuned Logistic Regression (Improved version)

Recall: 83.2%  Best at catching churners
(Now identifies 83% of churning customers)

Baseline Decision Tree

Recall: 75.2%
(Simple tree model performed similarly to first logistic regression)

Tuned Decision Tree (Improved version)

Recall: 80.2%
(Better than baseline but not as good as tuned logistic regression)

The tuned Logistic Regression performed best at finding customers who will churn (highest recall). All models improved when we did tuning. We prioritized recall because it's worse for business to miss a churning customer than to accidentally flag a loyal one


## Conclusion
This project developed a machine learning solution to predict customer churn with 83.2% recall using an optimized logistic regression model. By prioritizing recall during model selection, we ensured the business identifies the maximum number of potential churners, as false negatives (missed churn cases) are more costly than false positives in this scenario.
