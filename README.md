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

In the photo, it is shown that the logistic regression model is showing a 60.8% accuracy for precision and recall scores for each classification.

![image](https://user-images.githubusercontent.com/99559096/180677049-b2420ef9-e4e4-43a3-8c00-45150b09cd18.png)

Pictured above is a classification report. 

For the HIGH RISK CLASS:
- The precision is 1%
- The recall is 57%

For the LOW RISK CLASS:
- The precision is 100%
- The recall is 64%

## SMOTE Oversampling
Using the Synthetic Minority Oversampling Technique (SMOTE) we show the logistic regression model using this method is 65.8%

![image](https://user-images.githubusercontent.com/99559096/182045043-c27db1a4-0b35-4e6b-82c1-e143a371807e.png)

In the classification report we can see for each classification :
![image](https://user-images.githubusercontent.com/99559096/182045062-af94f7f5-9503-4874-8fed-b736f8dd2736.png)

For High Risk :
- The precision is 1%
- The recall is 64%
For Low Risk : 
- The precision is 100%
- The recall is 67%

## Undersampling Using the ClusterCentroids Method
Cluster Centroid undersampling shows grouping for the majority class then generates synthetic datapoints also known as 'Centroids' that are representative of the groupings

The accuracy score for the logistic regression model using ClusterCentroids Method shows 52.4% accuracy :

![image](https://user-images.githubusercontent.com/99559096/182045154-01c64efb-3218-490b-8a78-98b6209e81c9.png)

In the classification report we can see for each classification :

![image](https://user-images.githubusercontent.com/99559096/182045164-c2679c0d-6f0f-49fa-88ea-30665bada4d5.png)

For High Risk : 
- The precision is 1%
- The Recall is 62%

For Low Risk : 
- The precision is 100%
- The recall is 42%

## Combination Sampling with SMOTEENN
SMOTEENN is a two step process
1. Use SMOTE to oversample the data
2. Clean the results from SMOTE if the two closest neighbors to a datapoint belong to different classes, drop the data point.

The accuracy score for the logistic regression model using SMOTEENN is 61.9% : 

![image](https://user-images.githubusercontent.com/99559096/182045321-b80405b3-95f1-4a33-849e-347f8b3987d5.png)

In the classification report we can see for each classification :

![image](https://user-images.githubusercontent.com/99559096/182045339-8701d380-e037-443a-a000-9a938e985ae1.png)

For High Risk : 
- The precision is 1%
- The Recall is 69%

For Low Risk : 
- The precision is 100%
- The Recall is 55%

## The Balanced Random Forest Classifier
The accuracy score of this randomforest classifier is 79.4% : 

![image](https://user-images.githubusercontent.com/99559096/182045456-9b334e14-af7d-4686-8f14-28f20e4ac384.png)

In the classification report we can see for each classification :

![image](https://user-images.githubusercontent.com/99559096/182045470-8625c9f0-ef20-447c-957e-1de5d4697749.png)

For High Risk : 
- The precision is 3%
- The recall is 71%

For Low Risk : 
- The precision is 100%
- The Recall is 88%

## The Easy Ensemble Classifier
The accuracy score of the easy ensemble classifier is 91.0% :

![image](https://user-images.githubusercontent.com/99559096/182045527-bcf3cba3-2cf8-4b82-b77d-a4f1ac430eea.png)

In the classification report we can see for each classification :
![image](https://user-images.githubusercontent.com/99559096/182045532-87ef93a4-dc66-4db8-af8d-296a5803fd79.png)

For High Risk :
-The precision is 0.7%
-The recall is 89%
For Low Risk :
-The precision is 100%
-The Recall is 94%

# Summary
We used 4 different resampling methods before using them on our logistic model. There is little difference between each resampling method, making the method used negligible. The precision and recall scores are all within a minimal margin. 

Going towards the Easy Ensemble Classifier, the diffrerence is shown that it is more accurate for prediction due to the accuracy scores being 89/94%

To recommend a model, the easy pick is the final test with the Easy Ensemble Classifier, as it is the most accurate of all testing shown with this dataset. This model will correctly classify a high risk application 89% of the time, and 94% likely to classify a low risk application.
