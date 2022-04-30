# Credit_Risk_Analysis

## Overview of the analysis: 
- Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we'll need to employ different techniques to train and evaluate models with unbalanced classes. In this project, we are use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

- we're using the credit card credit dataset from LendingClub. Frist, oversample the data using the RandomOverSampler and SMOTE algorithms
. And then, undersample the data using the ClusterCentroids algorithm. AFter, use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Last, compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Results: Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

- Oversample / RandomOverSampler
    - 
    - Balanced accuracy scores = 0.64
    - High_risk Precision = 0.01
    - High_risk recall (Sensitivity) = 0.64
    - High_risk F1 score = 0.02
    - Low_risk Precision = 1.0
    - Low_risk recall = 0.66
    - Low_risk F1 score = 0.79
    - The high_risk precision score doesn't looks good and this make the f1 score result in worse

    
- Oversample / SMOTE
    - Balanced accuracy scores = 0.63
    - High_risk Precision = 0.01
    - High_risk recall (Sensitivity) = 0.62
    - High_risk F1 score = 0.02
    - Low_risk Precision = 1.0
    - Low_risk recall = 0.64
    - Low_risk F1 score = 0.78
    - The high_risk precision score doesn't looks good and this make the f1 score result in worse

- Undersample / ClusterCentroids
    - Balanced accuracy scores = 0.51
    - High_risk Precision = 0.01
    - High_risk recall (Sensitivity) = 0.57
    - High_risk F1 score = 0.01
    - Low_risk Precision = 1.0
    - Low_risk recall = 0.45
    - Low_risk F1 score = 0.62
    - Undersampleing with ClusterCentroids reports are even worse than the oversample models above. 

- Combine (Over- and Undersample) / SMOTEENN algorithm
    - Balanced accuracy scores = 0.64
    - High_risk Precision = 0.01
    - High_risk recall (Sensitivity) = 0.74
    - High_risk F1 score = 0.02
    - Low_risk Precision = 1.0
    - Low_risk recall = 0.55
    - Low_risk F1 score = 1.0
    - We don't see much improvement using resampling with SMOTEENN, only some of the metrics such as recall score has an improvement over undersampling.

- BalanceRandomForestClassifier
    - Balanced accuracy scores = 0.999
    - High_risk Precision = 0.83
    - High_risk recall (Sensitivity) = 1.0
    - High_risk F1 score = 0.91
    - Low_risk Precision = 1.0
    - Low_risk recall = 1.0
    - Low_risk F1 score = 1.0
    - Using ensemble algorithms with Balance Random forest Classifier is impressive, we have a great balanced accuracy score, all the metrics on classification report looks great.

- EasyEnsebleClassifier
    - Balanced accuracy scores = 1.0
    - High_risk Precision = 1.0
    - High_reish recall (Sensitivity) = 1.00
    - F1 score = 1.00
    - Low_risk Precision = 1.0
    - Low_risk recall = 1.0
    - Low_risk F1 score = 1.0
    - Using ensemble algorithms with Easy Enseble Classifier is impressive, we have a great balanced accuracy score, all the metrics on classification report are score in 1.0

## Summary: 
- According to the balanced accuracy scores, and the metric scores from classification reports of each models, I think Easy Enseble Classifier has the best balance, Balance Random Forest Classifier in second place. I would recommend both ensemble model.