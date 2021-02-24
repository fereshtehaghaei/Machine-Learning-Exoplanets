# Machine Learning Homework - Exoplanet Exploration

![exoplanets.jpg](Images/exoplanets.jpg)



## Background

Over a period of nine years in deep space, the NASA Kepler space telescope has been out on a planet-hunting mission to discover hidden planets outside of our solar system.

To help process this data, I created machine learning models capable of classifying candidate exoplanets from the raw dataset.

### Preprocessed & Cleaned the Data

* Data was first read in from a csv file, and null columns and null rolls were dropped. 
* Performed feature selection and remove unnecessary features.
* Used `ExtraTreesClassifier()` and stored those top ten features as a series to be used as my `X` values. 
* The `koi_disposition` column contained the classification values of each exoplanet candidate and would be used as my `y` values.
* Used `MinMaxScaler` to scale the numerical data.
* Separated the data into training and testing data.`train_test_split` 
* This process and method was used for all four models.

### Tuned Model Parameters

* Used `GridSearch` to tune model parameters for all four methods

  

### Reporting

- **KNN**
  - Used K-Nearest Neighbors to find the best K value. Created a loop to run through a set of possible k values after Comparing the training and testing scores, I found that k=15 was the best value as it had the lowest difference between training and testing scores.
  - Used classification report to analyze key metrics and it showed the precision (confirmed 0.73, False Positive 0.74 and Candidate 0.98) classified correctly among the class. The score for f1 showing the harmonic mean between precision & recall. The classification report also showed the support number of  (confirmed 411, False Positive 484 and Candidate 853)  which it shows dataset is not very well balanced.
  - Saved the model using joblib

- **Logistic Regression**

  - Used LogisticRegression() model and used training data to for model fitting. After using the scored the model using training and testing scores, both sets scored well, with training data 82% and testing data 81.9%

  - Used **Hyperparameter Tuning** by using `GridSearchCV` to tune the parameters further more. Changed 'C' and 'max_iter' values and found that 65 is the best value for 'C' and 100 is the best for 'max_iter' and got the score model of 85% 

  - Saved the model using joblib

    

  **Random Forest**

  - Used RandomForest() model and used training data to for model fitting and set the number of trees to 200 (n_estimators =200), both sets scored well, with training data 100% and testing data 89%
  - Used **Hyperparameter Tuning** by using `GridSearchCV` to tune the parameters further more. Changed number of tress ('n_estimators') and 'max_depth' values and found that 15 is the best value for 'max_depth' and 700 is the best for 'n_estimator' and got the score model of 89% which there was no significant improvement from the original model.
  - Saved the model using joblib



- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -



##### © 2021 Fereshteh Aghaei | University of Denver Data Analysis Bootcamp. All Rights Reserved.
