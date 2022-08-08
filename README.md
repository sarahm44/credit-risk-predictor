# Credit Risk Predictor
 
![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/credit-risk.jpg)

## Table of Contents

- [Overview](#overview)
- [Resampling](#resampling)
  * [Logistic Regression](#logistic-regression)
  * [Oversampling](#oversampling)
  * [Undersampling](#undersampling)
  * [Combination Sampling](#combination-sampling)
  * [Conclusions](#conclusions)
- [Ensemble Learning](#ensemble-learning)
  * [Balanced Random Forest](#balanced-random-forest)
  * [Easy Ensemble Classifier](#easy-ensemble-classifier)
  * [Conclusions](#conclusions-1)

## Overview

This task required that I build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. 

Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so I employed different techniques for training and evaluating models with imbalanced classes. 

I used the [imbalanced-learn](https://imbalanced-learn.org/stable/) and [Scikit-learn](https://scikit-learn.org/stable/) libraries to build and evaluate models using the two following techniques, each contained in their own code file:

1. [Resampling](https://github.com/sarahm44/credit-risk-predictor/blob/main/credit_risk_resampling.ipynb)
2. [Ensemble Learning](https://github.com/sarahm44/credit-risk-predictor/blob/main/credit_risk_ensemble.ipynb)

## Resampling

### Logistic Regression

I completed a simple linear regression. I then generated the balanced accuracy score, confusion matrix and classification report, as below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/logistic_regression.png)

### Oversampling
In this section, I compared two oversampling algorithms to determine which algorithm results in the best performance. 

These algorithms were: 
* naive random oversampling algorithm
* SMOTE algorithm. 

I then generated the balanced accuracy score, confusion matrix and classification report for each.

See naive random oversampling algorithm results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/nro.png)

See SMOTE algorithm results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/smote.png)

### Undersampling

In this section, I tested an undersampling algorithm to determine which algorithm results in the best performance compared to the oversampling algorithms above. 

I undersampled the data using the Cluster Centroids algorithm.

I then generated the balanced accuracy score, confusion matrix and classification report.

See Cluster Centroids algorithm results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/cc.png)

### Combination Sampling

In this section, I tested a combination over- and under-sampling algorithm to determine if the algorithm results in the best performance compared to the other sampling algorithms above. 

I resampled the data using the SMOTEENN algorithm.

I then generated the balanced accuracy score, confusion matrix and classification report.

See the SMOTEENN algorithm results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/smoteenn.png)

### Conclusions

#### Best Balanced Accuracy Score

| Model | Balanced Accuracy Score |
| --- | --- |
| Simple logistic regression | 0.9892813049736127 |
| Naive random oversampling | 0.9946414201183431 |
| SMOTE oversampling | 0.9946680739911509 |
| Cluster Centroids undersampling | 0.9932813049736127 |
| SMOTEENN combination sampling | 0.9946680739911509 |
   
SMOTE oversampling and combination sampling with SMOTEENN had the best balanced accuracy scores.

#### Best Recall Score

| Model | High Risk | Low Risk | Average |
| --- | --- | --- | --- |
| Simple logistic regression | 0.98 | 0.99 | 0.99 |
| Naive random oversampling | 1.00 | 0.99 | 0.99 | 
| SMOTE oversampling | 1.00 | 0.99 | 0.99 |
| Cluster Centroids undersampling | 0.99 | 0.99 | 0.99 |
| SMOTEENN combination sampling | 1.00 | 0.99 | 0.99 |
   
Naive random oversampling, SMOTE oversampling and combination sampling with SMOTEENN have the best recall scores.

#### Best Geometric Mean Score

| Model | High Risk | Low Risk | Average |
| --- | --- | --- | --- |
| Simple logistic regression | 0.99 | 0.99 | 0.99 |
| Naive random oversampling | 0.99 | 0.99 | 0.99 |
| SMOTE oversampling | 0.99 | 0.99 | 0.99 |
| Cluster Centroids undersampling | 0.99, | 0.99 | 0.99 |
| SMOTEENN combination sampling | 0.99 | 0.99 | 0.99 |
   
Every model had the same geometric mean score.

## Ensemble Learning

In this section, I trained and compared two different ensemble classifiers to predict loan risk and evaluate each model. 

These were: 
* Balanced Random Forest Classifier 
* Easy Ensemble Classifier

I generated the balanced accuracy score, confusion matrix and classification report for each.

### Balanced Random Forest

See the Balanced Random Forest Classifier results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/random_forest.png)

### Easy Ensemble Classifier

See the Easy Ensemble Classifier results below:

![](https://github.com/sarahm44/credit-risk-predictor/blob/main/images/easy_ensemble.png)

### Conclusions

#### Best Balanced Accuracy Score

| Model | Balanced Accuracy Score |
| --- | --- |
| Balanced Random Forest Classifier | 0.795829959187949 |
|Easy Ensemble Classifier | 0.9263912558266958 |
   
Easy Ensemble Classifier had the best balanced accuracy score.

#### Best Recall Score

| Model | High Risk | Low Risk | Average |
| --- | --- | --- | --- |
| Balanced Random Forest Classifier | 0.71 | 0.88 | 0.88 |
| Easy Ensemble Classifier | 0.91 | 0.94 | 0.94 |
   
Easy Ensemble Classifier had the best recall score.

#### Best Geometric Mean Score

| Model | High Risk | Low Risk | Average |
| --- | --- | --- | --- |
| Balanced Random Forest Classifier | 0.79 | 0.79 | 0.79 |
| Easy Ensemble Classifier | 0.93 | 0.93 | 0.93 |
   
Easy Ensemble Classifier had the best geometric mean score.

#### Top three features

The top three features are:    
   * total_rec_prncp
   * total_rec_int
   * total_pymnt_in
   
