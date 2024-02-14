# pricePrediction

# Overview

This repo explores the used cars dataset from Kaggle. The original dataset contained information on 3 million used cars. The dataset in this repo contains information on 426K cars to ensure speed of processing.  The goal is to understand what factors make a car more or less expensive.  As a result of the analysis, this repo provides clear recommendations to a client -- a used car dealership -- as to what consumers value in a used car.

# Business Understanding

This task aims to develop a Machine-learning model to predict the prices of used cars based on the data provided. In this task, linear regression models will be developed to identify key features influencing the price of used cars. The models developed will provide insights into the patterns and relationships in the data. The insights derived from the data will eventually help estimate used car prices.

# Data Understanding & Preparation

- Many columns were missing more than 30% of the data
- There were too many unique values for features VIN and model
- Features 'condition,' 'cylinders,' 'VIN,' 'drive,' 'size,' 'type,' and 'paint_color' had too many missing values, so the columns were dropped
- Features 'region' and 'state' are not useful data to build the model, so they were dropped
- Features 'id' and 'model' had too many unique values, so they were dropped too
- Outliers in 'price,' 'year,' and 'odometer' were dropped

  # Modeling

  Built the following  linear regression models.
  - Simple Linear Regression with numerical features
  - Linear Regression model with all features
  - Huber Regression model with all features
  - Lasso Regression
  - Ridge Regression
  - Ridge regression after dimensionality reduction using PCA
 
  # Evaluation
  Based on the different models developed, the ridge regression model, after performing dimensionality reduction, gave the best results. The MSE for training data and test data were almost the same.
  The Lasso model suggested the latest model cars, car titles with a lien, and cars with manual transmissions are expensive. Cars with higher odometer readings, Cars with all fuel types, cars with missing titles, and cars that are salvaged, rebuilt and missing parts are inexpensive. The best hyperparameter was 0.001, but the MSE was on the higher side. Hence, it was decided to build a ridge regression model.

  ![image](https://github.com/manikrajan/pricePrediction/assets/6862254/b49926a5-6887-4100-936c-d78e8d211760)

  # Deployment
  - Used electric cars and diesel-fueled cars are cheaper compared to other fuel types
  - Used Aston-Martin, Buick, Chrysler, and Audi are cheaper
  - Cars with clean titles, and rebuilt cars are cheaper
  - Recommend the client add more inventory of latest Hybrid and manual transmission cars

  


  
 
    
