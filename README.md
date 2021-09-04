# Purpose 
The Purpose of this project was to evaluate the effectiveness of ML models in determining credit card risk using a dataset from LendingClub. 
This project consists of 4 deliverables:

* Deliverable 1: Use Resampling Models to Predict Credit Risk
* Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
* Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
* Deliverable 4: A Written Report on the Credit Risk Analysis (README.md)

## Results

Describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. 
* Accuracy is the percentage of correct predictions for the test data. (Accuracy = Correct Predictions / Total Predictions) 
* Precision is a measure of how reliable a positive classification is. Precision = True Positives / (True Positives + False Positives).
* Sensitivity (Recall) is a measure of how accurate the model is in predicting the percentage of true positives that were correctly identified.         Sensitivity = True Positives / (True Positives + False Negatives)

### Naive RandomOverSampling Model

<img width="721" alt="Screen Shot 2021-09-04 at 4 14 18 PM" src="https://user-images.githubusercontent.com/83051034/132109222-9d073c2f-eb09-40ef-a4de-1ac11ee1a2dd.png">

* Accuracy is 64%.
* Precision is 99%, however the precision score for high-risk is very low (1%). 
* Sensitivity (Recall) is 62%. 

### SMOTE Oversampling Model 

<img width="718" alt="Screen Shot 2021-09-04 at 4 17 50 PM" src="https://user-images.githubusercontent.com/83051034/132109260-4caf79cc-969d-4bff-bbfc-06917b1a6e24.png">

* Accuracy is 65%. 
* Precision is 99%, however the precision score for high-risk is very low (1%). 
* Sensitivity (Recall) is 69%. 

### Cluster Centroids Model 

<img width="715" alt="Screen Shot 2021-09-04 at 4 18 30 PM" src="https://user-images.githubusercontent.com/83051034/132109273-6cb67423-4031-4f1f-943f-3a5583fe0d2f.png">

* Accuracy is 57%.
* Precision is 99%, however the precision score for high-risk is very low (1%). 
* Sensitivity (Recall) is 53%. 

### SMOTEENN Model 

<img width="711" alt="Screen Shot 2021-09-04 at 4 20 57 PM" src="https://user-images.githubusercontent.com/83051034/132109305-d9557c49-e64e-45df-a03a-c2824a4611f5.png">

* Accuracy is 65%.
* Precision is 99%, however the precision score for high-risk is very low (1%).
* Sensitivity (Recall) is 56%. 

### Balanced Random Forest Classifier

<img width="731" alt="Screen Shot 2021-09-04 at 4 22 38 PM" src="https://user-images.githubusercontent.com/83051034/132109334-840e29da-6aaf-43c6-a049-d9d20d09d451.png">

* Accuracy is 79%.
* Precision is 99%, however the precision score for high-risk is very low (3%).
* Sensitivity (Recall) is 88%. 

### Easy Ensemble AdaBoost Classifier

<img width="722" alt="Screen Shot 2021-09-04 at 4 23 27 PM" src="https://user-images.githubusercontent.com/83051034/132109345-d6db0bcc-06d1-4dd6-8f17-4b4d1339482c.png">

* Accuracy is 93%.
* Precision is 99%, however the precision score for high-risk is low (9%).
* Sensitivity (Recall) is 94%. 

## Summarize 

All the models used here to predict credit card risk have weak precision scores, meaning that the number of false positives is high. I.e. There is a high number of applications that were classified as high-risk despite actually being low-risk. Sensitivity (Recall) for the Easy Ensemble AdaBoost Model is the highest, meaning that that model is the most reliable in predicting all of the high-risk applications. Accuracy is also highest for the Easy Ensemble AdaBoost Model meaning that overall, the model was accurate in predicting 99% of all applications correctly, however it was only accurate in predicting high-risk applications 9% of the time. The F1 score, which is characterized as a single summary statistic of precision and sensitivity, is highest for the Easy Ensemble AdaBoost Model as well. 

I would not recommend any of these models be used by a bank because the low precision would be detrimental to a bank's ability to make profits by falsly classifying low-risk applications as high-risk. However, if one model must be used, it should be the Easy Ensemble AdaBoost Model. 





















