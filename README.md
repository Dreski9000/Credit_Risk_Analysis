# Credit_Risk_Analysis
Module 17 of UCB Data Science Bootcamp - Supervised Learning

### Analysis Overview
The goal of this project is to test different supervised machine learning models to analyze and predict credit risk for potential bank loan applicants.

An accuracy score, confusion matrix and other metrics are computed for each model to evalute accuracy and viability

Note: Random State was not selected apart from ensemble learning models.

### Results

**Logistic Regression w/ Naive Random Oversampling**
* Balanced Accuracy Score: 0.64
* Precision : 0.99
* Recall: 0.67

**Logistic Regression w/ SMOTE**
* Balanced Accuracy Score: 0.65
* Precision : 0.99
* Recall: 0.70

**Logistic Regression w/ Cluster Centroids (undersampling)**
* Balanced Accuracy Score: 0.56
* Precision: 0.99
* Recall: 0.48

**Logistic Regression w/ SMOTEENN**
* Balanced Accuracy Score: 0.63
* Precision: 0.99
* Recall: 0.60

**Balanced Random Forest Classifier**
* Balanced Accuracy Score : 0.75
* Precision: 0.99
* Recall: 0.75

**Easy Ensemble AdaBoost Classifier**
* Balanced Accuracy Score: 0.90
* Precision: 0.99
* Recall: 0.94

### Summary

All models appear to have a very high precision rate of 99% or greater, however, the logistic regression classifiers all have a worse recall scores than the tree classifiers. Since recall is very important when it comes to credit risk, to make sure that the classifier is casting a wide enough net to catch as many high-risk accounts as possible, * *AdaBoost* * is probably the best classifier to use if the data gets frequently re-trained with more recent, prescient data, otherwise the model might risk overfitting and dropping in accuracy over time. If the classifier data set is not frequently re-trained, then * *Balanced Random Forest* * might be the better choice, with the second-highest balanced accuracy score, it may be more resilient to overfitting.