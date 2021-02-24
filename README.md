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

* Used `GridSearch` to tune model parameters.

  

### Reporting



- - -

## Resources

* [Exoplanet Data Source](https://www.kaggle.com/nasa/kepler-exoplanet-search-results)

* [Scikit-Learn Tutorial Part 1](https://www.youtube.com/watch?v=4PXAztQtoTg)

* [Scikit-Learn Tutorial Part 2](https://www.youtube.com/watch?v=gK43gtGh49o&t=5858s)

* [Grid Search](https://scikit-learn.org/stable/modules/grid_search.html)

- - -



##### © 2021 Fereshteh Aghaei | University of Denver Data Analysis Bootcamp. All Rights Reserved.
