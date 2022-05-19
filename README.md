# Supervised Machine Learning Homework - Predicting Credit Risk
Build a machine learning model thaat attempts to predict whether a loan from LendingClub will become high risk or not. 
Data Source: 
* LendingClub's API
SCV: 
* [2019loans.csv](https://github.com/cc-christin/Supervised-Machine-Learning/blob/main/Resources/2019loans.csv)
* [2020Q1loans.csv](https://github.com/cc-christin/Supervised-Machine-Learning/blob/main/Resources/2020Q1loans.csv)
Used:
* Random Forest Classifiers 
* Logistic Regression
Task:
* Classify the risk level of given loans
* Comparing the Logistic Regression model and Random Forest Classifier
* Use data (2019) to predict the credit risk of loans for the first quarter of (2020).
* pd.get_dummies() used to convert (2019) loan data to converrt categorical data to numeric creating training set
* Predict, create, fit, score and compare logistic regression, and random forests classifier.
### Predictions 
#### Predictions Of Before Scaling
Predicted Best Model Before Scaling: Random Forest Classifier

* Random Forest Classifier might be the better model to use. The use of many "prediction trees" should result in more accurate data, especially for continuous, categorical, and binary data sets used in credit risk assessment. However, there the concern with overfitting (noise) with the use of Random Forest Classifiers. Logistic regression might have lower accuracy rates than random forest classifiers before the model is appropriately scaled.

## Fit a LogisticRegression model and RandomForestClassifier model
* Create a Random Forest Classifer and LogisticRegression model, fit it to the data, and print the model's score, respectively.
* Choose any starting hyperparameters
* Which model performed better? 
   * Logistic Regression
* How does that compare to your prediction? Write down your results and thoughts.
    * Matched predictions as there were conscerns about logistic regression being over-fitted and not affected by scaling. 

### Before Scaling Results
#### Logistic Regression model
Training Data Score: 0.6977011494252874
Testing Data Score: 0.5642279880901744

#### Random Forest Classifier model
Training Data Score: 1.0
Testing Data Score: 0.5642279880901744

## Revisit the Preprocessing: Scale the data
* Use `StandardScaler` to scale the training and testing sets. 
* Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, make another prediction about how you think scaling will affect the accuracy of the models.
* Write your predictions down and provide justification.
* 
### Predictions Of After Scaling 
Predicted Best Model After Scaling: Logistic Regression
logistic regression is dependent on scaling to make more accurate calculations, while the random forest classifier does not. Therefore, it would be reasonable to predict that logistic regression would be the better model to utilize after scaling.  

### Fit and score the LogisticRegression and RandomForestClassifier models on the scaled data.

### After Scaling Results
#### Logistic Regression model
Training Data Score: 0.712807881773399
Testing Data Score: 0.719906422798809

#### Random Forest Classifier model
Training Data Score: 1.0
Testting Data Score: 0.6371756699276904

#### Questions

* How do the model scores compare to each other, and to the previous results on unscaled data? 
* How does this compare to your prediction? 
* Write down your results and thoughts.

### Results 

As predicted, the random forest classifier model was overfitted even after scaling, since it is not usually dependent on scaling. Prior to scaling the random forest classifier had a testing score of 0.56 with a overfitted accuracy score of 1.0. Yet it was still the better of the two data models. 
After scaling, it was still over fitted with testing score of 0.63 and accuracy score of 1.0. 
The Logistic Regression, contrastingly, improved after scaling from 0.56 and 0.70, testing and training score respectively to a testing score of 0.72 and training score of 0.71. 
In conclusion, logistic regression model, after appropriate scaling, would be the better and preferred model for this credit risk evaluation dataset.   




