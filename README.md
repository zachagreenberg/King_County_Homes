# King of Real Estate
## Effectively Predicting Prices of Homes in King County, Washington

![Cover](https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Other_Images/Cover.png)

by Zachary Greenberg

## Overview
The housing market in King County, Washington is highly diverse. I am seeking to create a predictive model to accurately forecast the prices in the market. Using the detailed factors of a home, including number of bathrooms, zipcode, renovation status, and so on I will analyze and clean the data to be used in a Multiple Linear Regression model. My goal is to come within $200000 for my model estimates. I will use RMSE as an indicator of my model's performance. 

## Business Problem
When it comes to buying a house, there are many factors that affect the prices you will pay. If we can create a model to effectively predict the price of homes based on these factors, this will increase our understanding of the housing market and allow us to be more certain in our future pricing estimates and appraisals. 
 

## Data

My dataset is a [2015 Kings County Housing dataset](https://www.kaggle.com/harlfoxem/housesalesprediction) provided by Kaggle. Here is a list of the information I will be using in my model:

* **price** - Price is prediction TARGET  


* **id** - unique ID for a house
* **date** - Date day house was sold
* **bedrooms** - Number of bedrooms
* **bathrooms** - Number of bathrooms
* **sqft_living** - square footage of the home
* **sqft_lot** - square footage of the lot
* **floors** - Total floors (levels) in house
* **waterfront** - Whether house has a view to a waterfront
* **view** - Number of times house has been viewed
* **condition** - How good the condition is (overall)
* **grade** - overall grade given to the housing unit, based on King County grading system
* **sqft_above** - square footage of house (apart from basement)
* **sqft_basement** - square footage of the basement
* **yr_built** - Year when house was built
* **yr_renovated** - Year when house was renovated
* **zipcode** - zip code in which house is located
* **lat** - Latitude coordinate
* **long** - Longitude coordinate
* **sqft_living15** - The square footage of interior housing living space for the nearest 15 neighbors
* **sqft_lot15** - The square footage of the land lots of the nearest 15 neighbors




## EDA
During the data exploration process, there seemed to be a predictability in certain factors affecting the overall price. 

I looked at the relationship between price and square foot.

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/sqftliving.png" width="700" height="280" /></p>

As the size of the living area increased, the price did as well. 

I also tested the relationship between price and whether or not the property was waterfront. 

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Waterfront.png" width="300" height="180" /></p>

This turned out to be statistically significant that there was a major difference in price given the home was waterfront or not. 



## Feature Engineering
Because of the predictability of the given features, I decided to go ahead and generate some new features to make my model more unique. 

For example, I used the datetime column to extract the Month and create a price by month feature.

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/month.png" width="500" height="280" /></p>

This also proved to be statistically significant. 

## Modeling
For my modeling process, I ran a baseline model with little to no changes and had achieved an RMSE of approximate 151000, which immediately hit my end goal, however I decided to run with it and create several other models to improve my RMSE score. Using techniques like non linear transformations and feature selection, I ended up have to choose between three models. Here are there scores: 

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Models.png" width="300" height="180" /></p>

**As an addition to all of this** I decided to come up with a neural network model. Please see the 'NeuralNet_Addition.ipynb' notebook. It is still a work in progress at the moment, the RMSE achieved cannot compete with the other models at this time, therefore the results remain the same.  

## Results

After trying out various models, I ultimately decided to go my Nonlinear Transformation model. It produced the 2nd lowest RMSE score, however the gap between train and test were also the closest. This made me a little more confident in my choice. I was able to achieve my goal of being under $200000 for the price estimates.  

## Next Steps

I believe the model could possibly show continuous improvement through the further tuning of the neural net model. I would be curious to see if it can be comparable to the linear models created. 

---------------------------------

## Repository Structure

|_ Data          
|_ Visualizations      
|_ .gitignore      
|_ EDA-Modeling-Eval.ipynb  
|_ EDA_Presentation.pdf     
|_ NeuralNet_Addition.ipynb    
|_ Predictions_Preparation.ipynb           
|_ housing_preds_zachary_greenberg.csv    
|_ README.md      





