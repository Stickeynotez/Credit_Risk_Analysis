# Credit_Risk_Analysis

## Overview

In this project, we were provided with a large dataset on loan applications with all available information included in the dataset. The task at hand is to transfrom the imbalanced dataset and feed it into a machine learning program to predict if a loan application is low or high risk.

### Resamping Techniques

We are using 4 resampling techniques to make the dataset more balanced in our credit risk resampling program.
- Oversampling with Naive Random OverSampler
- SMOTE Oversampling
- Undersampling using ClusterCentroids
- Combination of oversampling and undersampling with SMOTEENN
To show the risk factor, a logistic regression model is used to predict and assess the performance of the model.

### Ensemble Learning Techniques
There are 2 techniques used with our credit risk ensemble file.
- The Balance RandomForestClassifier
- The Easy Ensemble Classifier
Each model was processed in the same manner as the previous resampling file.

# Results
## Oversampling with Naive RandomOverSampler
![image](https://user-images.githubusercontent.com/99559096/180676955-c71f85a4-9e62-4d5a-88d4-51ab8e616b80.png)

In the photo, it is shown that the logistic regression model is showing a 60.7% accuracy for precision and recall scores for each classification.

![image](https://user-images.githubusercontent.com/99559096/180677049-b2420ef9-e4e4-43a3-8c00-45150b09cd18.png)

Pictured above is a classification report. 

For the HIGH RISK CLASS:
- The precision is 1%
- The recall is 57%

For the LOW RISK CLASS:
- The precision is 100%
- The recall is 64%

## SMOTE Oversampling
