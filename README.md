# Prediction of Credit Card Fraud Detection Capstone Project
## Problem Statement
The objective of this project is to predict fraudulent credit card transactions and we will build a classification model to predict whether a transaction is fraudulent or not.
A credit card is one of the most used financial products to make online purchases and payments. Though the Credit cards can be a convenient way to manage your finances, they can also be risky. Credit card fraud is the unauthorized use of someone else's credit card or credit card information to make purchases or withdraw cash.
It is important that credit card companies are able to recognize fraudulent credit card transactions so that customers are not charged for items that they did not purchase. 
## Business Problem Overview
The most important business objective for banks is to retain highly profitable customers. However, different banks are exposed to a major threat of Banking Fraud. In the context of financial losses, trust and credibility, this is a concerning issue to both banks and customers.
With the rise in digital payment channels, the number of fraudulent transactions is also increasing with new and different ways.
In the banking industry, credit card fraud detection using machine learning is not just a trend but a necessity for them to put proactive monitoring and fraud prevention mechanisms in place. Machine learning is helping these institutions to reduce time-consuming manual reviews, costly chargebacks and fees, and denials of legitimate transactions.
## Understanding and Defining Fraud
Credit card fraud is an act of unauthorized use of an individual's credit card information for financial gain. There are various types of credit card fraud, but one very common type is Skimming where the information is copied from the magnetic strip on the card. Common types includes:
* Identity theft
* Phisihing scams
* Card not present(CNP)
* Lost or Stolen card
## Data Dictionary
The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.
Principal Component Analysis(PCA) has already been applied to maintain confidentiality. The feature Class with a value of 0 indicates normal transaction and 1 indicates fraudulent transaction. The principal components obtained from PCA are features from V1 to V28. The features Time and Amount are not PCA transformed. The feature Time indicates the seconds elapsed between each transaction and the feature Amount indicates the transaction amount.
## Pipeline
A brief summary of the project pipeline is as follows:
* **Data Understanding and Preparation**: First load the data and understand the respective features. This helps in selecting a subset of features to carry out model training.
* **Exploratory data analytics (EDA)**: Usually univariate/bivariate analyses is carried out and then feature transformations, if necessary. But for our dataset there is no need to carry out this. However transformation is used to mitigate and check the skewness in the data.
* **Data Modeling/selection**: The train/test split is performed over here, to identify which ML model works good with the imbalance data and have better results on the test data. Two classification models (RadomForest and XGBoost) has been in the current study.
* **Hyperparameter Tuning**: This is the final step where different models can be tried and then their hyperparameters can be fine tuned until the desired level of performance on the given dataset is achieved. The Stratified K-Fold Cross Validation is used here as the dataset is not really huge.
* **Model Evaluation**: Evaluate the models using appropriate evaluation metrics. The AOC and ROC metric in sklearn is used as the metric as the dataset is highly imbalanced, rest all fails. Choose the best evealuation metric which accomplishes the business objective.
