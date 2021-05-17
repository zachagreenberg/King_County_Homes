# King of Real Estate
## In King County, Washington

![Cover](https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Other_Images/Cover.png)

by Zachary Greenberg

## Overview
The housing market in King County, Washington is highly diverse. I am seeking to create a predictive model to accurately forecast the prices in the market. Using the detailed factors of a home, including number of bathrooms, zipcode, renovation status, and so on I will analyze the data to be used in a Multiple Linear Regression model. My goal is to come within $200000 for my model estimates. I will use RMSE as an indicator of my model performance. 

## Business Problem
When it comes to buying a house, there are many factors that affect the prices you will pay. If we can create a model to effectively predict the price of homes based on these factors, this will increase our understanding of the housing market and allow us to be more certain in our future pricing estimates and appraisals. 
 

## Data

My dataset is a 2015 Kings County Housing dataset provided by Kaggle. Here is a list of the information I will be using in my model:

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

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/sqftliving.png" width="1000" height="380" /></p>

As the size of the living area increased, the price did as well. 

I also tested the relationship between price and whether or not the property was waterfront. 

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Waterfront.png" width="1000" height="380" /></p>

This turned out to be statistically significant that there was a major difference in price given the home was waterfront or not. 



## Feature Engineering
Because of the predictability of the given features, I decided to go ahead and generate some new features to make my model more unique. 

For example, I used the datetime column to extract the Month and create a price by month feature.

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/month.png" width="1000" height="380" /></p>


## Modeling
For my modeling process, I ran a baseline model with little to no changes and had achieved an RMSE of approximate 151000, which immediately hit my end goal, however I decided to run with and create several other models to improve my RMSE score. Using techniques like non linear transformations and feature selection, I ended up have to choose between three models. Here are there scores: 

<p align="center"><img src="https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Models.png" width="1000" height="380" /></p>


## Results

After trying out various models, I ultimately decided to go my Nonlinear Transformation model. It produced the 2nd lowest RMSE score, however the gap between train and test were also the closest. This made me a little more confident in my choice. I was able to achieve my goal of being under $200000 for the price estimates.  

---------------------------------

## Repo Structure

├── Data  
├── Visualizations  
├── Final_Notebook.ipynb    
├── Predictions_Notebook.ipynb  
├── housing_preds_zachary_greenberg.ipynb  
├── King_County_Homes.pdf    
└── README.me  




