# Credit Risk Predictor
 
![Credit Risk](credit-risk.jpg)

## Overview

This task required that I build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. 

Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so I employed different techniques for training and evaluating models with imbalanced classes. 

I used the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques, each contained in their own code file:

1. [Resampling](https://github.com/sarahm44/unit-11-assignment/blob/main/credit_risk_resampling.ipynb)
2. [Ensemble Learning](https://github.com/sarahm44/unit-11-assignment/blob/main/credit_risk_ensemble.ipynb)


- - -

## Final Questions Summary

### Resampling

#### 1. Which model had the best balanced accuracy score?

   The balanced accuracy scores were as follows - 

   * Simple logistic regression: 0.9892813049736127
   * Naive random oversampling: 0.9946414201183431
   * SMOTE oversampling: 0.9946680739911509
   * Undersampling: 0.9932813049736127
   * Combination sampling with SMOTEENN: 0.9946680739911509
   
   SMOTE oversampling and combination sampling with SMOTEENN had the best balanced accuracy scores.

#### 2. Which model had the best recall score?

   The recall scores were as follows - 
   * Simple logistic regression: high risk: 0.98, low risk: 0.99, average: 0.99
   * Naive random oversampling: high risk: 1.00, low risk: 0.99, average: 0.99
   * SMOTE oversampling: high risk: 1.00, low risk: 0.99, average: 0.99
   * Undersampling: high risk: 0.99, low risk: 0.99, average: 0.99
   * Combination sampling with SMOTEENN: high risk: 1.00, low risk: 0.99, average: 0.99
   
   Naive random oversampling, SMOTE oversampling and Combination sampling with SMOTEENN have the best recall scores.

#### 3. Which model had the best geometric mean score?

   The geometric mean scores were as follows - 
   * Simple logistic regression: high risk: 0.99, low risk: 0.99, average: 0.99
   * Naive random oversampling: high risk: 0.99, low risk: 0.99, average: 0.99
   * SMOTE oversampling: high risk: 0.99, low risk: 0.99, average: 0.99
   * Undersampling: high risk: 0.99, low risk: 0.99, average: 0.99
   * Combination sampling with SMOTEENN: 0.99, low risk: 0.99, average: 0.99
   
   Every model had the same geometric mean score.


### Ensemble Learning

#### 1. Which model had the best balanced accuracy score?

   The balanced accuracy scores were as follows - 

   * Balanced Random Forest Classifier: 0.795829959187949
   * Easy Ensemble Classifier: 0.9263912558266958
   
   Easy Ensemble Classifier had the best balanced accuracy score.

#### 2. Which model had the best recall score?

   The recall scores were as follows - 

   * Balanced Random Forest Classifier: high risk: 0.71, low risk: 0.88, average: 0.88
   * Easy Ensemble Classifier: high risk: 0.91, low risk: 0.94, average: 0.94
   
   Easy Ensemble Classifier had the best recall score.

#### 3. Which model had the best geometric mean score?

   The geometric mean scores were as follows - 

   * Balanced Random Forest Classifier: high risk: 0.79, low risk: 0.79, average: 0.79
   * Easy Ensemble Classifier: high risk: 0.93, low risk: 0.93, average: 0.93
   
   Easy Ensemble Classifier had the best geometric mean score.

#### 4. What are the top three features?

   The top three features are: 
   
   * total_rec_prncp
   * total_rec_int
   * total_pymnt_in
   
