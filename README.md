# King of Real Estate
## In King County, Washington

![Cover](https://github.com/zachagreenberg/King_County_Homes/blob/main/Visualizations/Other_Images/Cover.png)

## Overview

The project aims to predict housing prices within the King County area of Washington state. In doing so, certain variables are taken into consideration when it comes to what greatly affects the housing market. 
 

## Data

2015 Housing Data provided information ideal for predicting housing prices. To name a few of the most useful ones:

Zipcode

Number of Bedrooms / Bathrooms

Year of Renovation

Squarefoot of the Nearest 15 Neighbors


## EDA
During the data exploration process, certain features seemed to be highlighted more than others indicating their influences. With following common sense, location showed perhaps the greatest variance in home prices indicating their affects. Other variables were certainly worth the deeper exploration. 


## Methods

To create the best model possible, features were carefully sifted through and analyzed for their overall relationship with price. The features that showed the most promise were the ones that made it into the final modeling process. Through trial and error with feature selection techniques, these selected columns helped to give insight on estimating pricing.

## Results

After trying out various models, I ultimately decided to go with the model where I had adjusted for the log of price. This seemed logical because the housing market in nature can be positively skewed.

## Repo Structure

├── Data  
├── Visualizations  
├── Final_Notebook.ipynb  
├── Predictions_Notebook.ipynb  
├── King_County_Homes.pdf  
└── README.me  




