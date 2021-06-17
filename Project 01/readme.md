# 1. Abstract
The data comes from Vesta's real-world e-commerce transactions and contains a wide range of features from device type to product features. The goal is to predict the probability that an online transaction is fraudulent, as denoted by the binary target isFraud.

The Dataset was given to the [Kaggle IEEE-CIS Fraud Detection Competition](https://www.kaggle.com/c/ieee-fraud-detection).

The data is broken into two files identity and transaction, which are joined by TransactionID. Not all transactions have corresponding identity information.

The training dataset consists of more than 400 features and 5.9 Million samples. This is supervised binary classification problem and goal is to predict if a credit card transaction is Fraud based on input features mentioned below.

# 2. Methodology
I have used CatBoost Classifier, Light GBM -weighted, Cat_5fold models and appended all together at the end. This gives me an accuracy of 0.942334 Public score and 0.912191 Private score in Kaggle submission.

# 3. Result Analysis
I have used Single CatBoost Modeling method, trained the data and then fit the model with CatboostClassifier Parameters. 
```
model_single = CatBoostClassifier(**params)
model_single.fit(train_data, eval_set=holdout_data, plot=True, verbose=False)
```
Then used Light GBM with selective parameters, trained the model & finally after 736 iterations the best AUC score I got was 0.96051.
```
bst.best_score
defaultdict(collections.OrderedDict,
            {'valid_0': OrderedDict([('auc', 0.9605100655661709)])})
```
Then I have used the CV approach with 5 fold using the full dataset. After that, I have appended the CatBoostClassifier with the K-fold model and used mean of the models predictions for the final submission test dataset.

# 4. Performance Evaluation

The ROC plot compares the Single CatBoost model with the Light GBM AUC scores. It's clear that Single CatBoost model performed better.

![ROC_ieee](https://user-images.githubusercontent.com/76067046/122374436-32368a80-cf84-11eb-8bb7-8d5980fcbdd2.PNG)

The Kaggle submission for the competition gives the following evaluations.

![kgl_graud](https://user-images.githubusercontent.com/76067046/122374604-53977680-cf84-11eb-9e39-b03fb0e6ee24.PNG)

# 5. Conclusion

The models used for this notebook can be improved with further Hyperparameter tuning. Although the current Score for the final model evaluation was 0.96051 & 0.942334 in Kaggle submission, it can be imrpoved with Tree based Gradients like XGBoost, Neural Network, etc. It seems having a powerful machine support like higher CPU, GPU & Memory can also play a significant role in improving the models performance.
