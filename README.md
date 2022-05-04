# Unit 11 - Risky Business
 
![Credit Risk](credit-risk.jpg)

## Background

Mortgages, student and auto loans, and debt consolidation are just a few examples of credit and loans that people seek online. Peer-to-peer lending services such as Loans Canada and Mogo let investors loan people money without using a bank. However, because investors always want to mitigate risk, a client has asked that you help them predict credit risk with machine learning techniques.

In this assignment you will build and evaluate several machine learning models to predict credit risk using data you'd typically see from peer-to-peer lending services. Credit risk is an inherently imbalanced classification problem (the number of good loans is much larger than the number of at-risk loans), so you will need to employ different techniques for training and evaluating models with imbalanced classes. You will use the imbalanced-learn and Scikit-learn libraries to build and evaluate models using the two following techniques:

1. [Resampling](#Resampling)
2. [Ensemble Learning](#Ensemble-Learning)

- - -

## Completed Code Files

The completed code files are as follows:

[Resampling Notebook](https://github.com/sarahm44/unit-11-assignment/blob/main/credit_risk_resampling.ipynb)

[Ensemble Notebook](https://github.com/sarahm44/unit-11-assignment/blob/main/credit_risk_ensemble.ipynb)

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
   
