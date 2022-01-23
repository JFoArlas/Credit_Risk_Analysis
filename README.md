# Credit_Risk_Analysis

## Overview
The purpose of this analysis was to employ different techniques to train and evaluate machine learning models with unbalanced classes in order to evaluate the performance of each model. Using a credit card credit dataset from LendingClub, a peer-to-peer lending services company, I took the following steps:

1. Oversampled the data using the RandomOverSampler and SMOTE algorithms
2. Undersampled the data using the ClusterCentroids algorithm
3. Used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm
4. Compared two machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

## Results

**RandomOverSampler**
- Balanced accuracy score: 65%
- Precision: 99%
- Recall: 59%

![ros](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/ros.png)

**SMOTE**
- Balanced accuracy score: 66%
- Precision: 99%
- Recall: 69%

![smote](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/smote.png)

**ClusterCentroids**
- Balanced accuracy score: 54%
- Precision: 99%
- Recall: 40%

![cc](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/cc.png)

**SMOTEENN**
- Balanced accuracy score: 65%
- Precision: 99%
- Recall: 57%

![smoteenn](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/smoteenn.png)

**BalancedRandomForestClassifier**
- Balanced accuracy score: 79%
- Precision: 99%
- Recall: 87%

![brfc](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/brfc.png)

**EasyEnsembleClassifier**
- Balanced accuracy score: 93%
- Precision: 99%
- Recall: 94%

![eec](https://github.com/JFoArlas/Credit_Risk_Analysis/blob/main/Resources/eec.png)

## Summary

The Easy Ensemble Classifier resulted in the highest balanced accuracy score, with a 93% chance a given prediction would accurately classify whether someone would be low vs. high credit risk. It also had the highest overall recall score of 94%. That said, the sample included 68,470 low_risk vs. 347 high_risk datapoints, which resulted in all of the models performing poorly in terms of the precision score for predicting high_risk credit in particular. In this case, the best performing model predicted low_risk when someone was actually high_risk 983 out of 1,076 times (9% precision). So despite any high scores for overall accuracy, precision, and recall; I would not reccomend using any of these models due to the low precision scores for predicting high risk credit.
