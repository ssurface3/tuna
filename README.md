# Bank's classifier
## Table of contents
* [General info](#general-info)
* [Features](#features)
* [Process](#process)
* [Stack](#stack)
* [Conclusion](#conclusion)

## General info
This project is made for classification of ouflow of clients.
Saving current clients is better than attracting new ones? This needs to be tested
## Features
* CustomerId — unique users' id
* Surname 
* CreditScore
* Geography — country of living
* Gender 
* Age 
* Tenure — years of being a bank's client
* Balance — money on card
* NumOfProducts — number of products that a person uses currently
* HasCrCard — 1 if has a card , 0 if doesn't
* IsActiveMember — 1 if is an active client, 0 not
* EstimatedSalary
* Exited - target 
## Process
|Stage | Description|
|--------|--------|
|First stage| Data preprocessing: removing Nans and giving data a good (and right) look|
|Second stage|Model training without classes balancement|
|Third stage| Classes Balancing(upscaling and downsampling), Trained three model and chose the best one|
|Fourth stage| Tested best model on test sample|
## Stack
Project is created with:
* Pandas
* Sklearn
  1. Sklearn.preprocessing
    1. StandardScaler
    2. OneHotEnocder
  2. Model_selection.train_test_split
  3. sklearn.metrics
     1. accuracy_score
     2. f1_score
     3. precision_score, recall_score
  4. sklearn.ensemble.RandomForestClassifier
  5. sklaern.tree.DecisionTreeClassifier
  6. sklearn.utils.shuffle
  7. sklearn.metrics
     1. roc_auc_score
     2. roc_curve
     3. auc
* Numpy
* Matplotlib.pyplot
	
## Conclusion
* It's better to upsample in this occasion as models yield better results with it
* Testing resulted aur_roc score of 0.6 and f1 is 0.6 whick is better than throwing a coin ;)





