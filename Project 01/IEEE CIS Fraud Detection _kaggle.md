# 1. Abstract
The data comes from Vesta's real-world e-commerce transactions and contains a wide range of features from device type to product features. The goal is to predict the probability that an online transaction is fraudulent, as denoted by the binary target isFraud.

The data is broken into two files identity and transaction, which are joined by TransactionID. Not all transactions have corresponding identity information.

The training dataset consists of more than 400 features and 5.9 Million samples. This is supervised binary classification problem and goal is to predict if a credit card transaction is Fraud based on input features mentioned below.

# 2. Methodology
I have used CatBoost Cllassifier, Light GBm -weighted, Cat_5fold models and appended all together at the end. This gives me an accuracy of 0.942334 Public score and 0.912191 Private score in Kaggle submission.
