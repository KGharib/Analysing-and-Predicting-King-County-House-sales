# Predicting-Sentiment-on-Amazon-Reviews
### Executive Summary
The Data used is from: https://www.kaggle.com/harlfoxem/housesalesprediction
<br><br>
- We will be using the King County Dataset in this project, we will perform EDA, and then answer a few questions based on the data, finally we will predict the House Sale price based on a number of features using Supervised Learning Methods
- The point of view we will be taking is that we have been approached by a real estate agency who is looking to start buying and selling in the King County Area and we have been hired to help them answer questions in order to make informed decesions as well as help them make profit through the effecient use of their funds and resources
<br><br>
### Pre-Processing Steps
- replaced Null values from waterfront and yr_renovated with the median, the reason being is i wanted to preserve the Median value for that column for future statistical anaylsis.
- removed Null/Missing values from view columns as it was only 63 missing points, and our dataset was fairly large enough that removing them would not have a negative effect
- changed Date column into a dtype format from integer to be able to do date time anaylsis
- removed "?" values in sqft_basement
<br><br>
### Statistical Anaylsis
- Correlation Heatmap
- Grouped Houses into prices bands depending on their sale price 
- used a heatmap to find most expensive and cheapeast locations
- used a duplicate counter to count how many houses are being sold in each zipcode by counting the number of times a unique houses is shown in a zipcode
<br><br>
### Questions:
- Which price are the most houses being sold and bought at and which price range has most activity and demand
- which location/zipcode has most demand?
- How accuratly can we predict the prices of houses based on certain features using different Machine Learning Techniques
<br><br>
### Methodology
1. **Business Understanding** 
- Based on the Data we want to be able to advise a Real Estate Agency Company which price range and locations are most profitable 
- find the factors which affect prices most and be able to buy houses which are being undersold and resell them.
- find location with most demand so that our business can focus our time and money on those locations with highest probability for profit 
<br> <br>
2. **Data Understanding**  
Column Names and descriptions for Kings County Data Set
- id - unique identified for a house
- date - house was sold
- price -  is prediction target
- bedroomsNumber -  of Bedrooms/House
- bathroomsNumber -  of bathrooms/bedrooms
- sqft_livingsquare -  footage of the home
- sqft_lotsquare -  footage of the lot
- floorsTotal -  floors (levels) in house
- waterfront - House which has a view to a waterfront
- view - Has been viewed
- condition - How good the condition is ( Overall )
- grade - overall grade given to the housing unit, based on King County grading system
- sqft_above - square footage of house apart from basement
- sqft_basement - square footage of the basement
- yr_built - Built Year
- yr_renovated - Year when house was renovated
- zipcode - zip
- lat - Latitude coordinate
- long - Longitude coordinate
- sqft_living15 - The square footage of interior housing living space for the nearest 15 neighbors
- sqft_lot15 - The square footage of the land lots of the nearest 15 neighbors
    <br><br>
3. **Modelling**
 For the 3rd question we used 3 differeent Machine Learning Techniques
- Linear Regression Model: this only gave us a score of around 56% which is only slightly better then randomly guessing
- KNN: for this we firstly scaled the data using a StandardScaler which is imperative as with KNN models we are measuring the distances of points using Uclidean distance and it is nesscessary to level the playing field between all the features in order to make sure that one doesnt out weight another just based on its scale, we got a score of 61% which is an improvement from a Linear Regression Model but still not good enough
- RandomForest: finally i used a RandomForest which performed the best with a score of 74% we then used a GridSearchCV in order to optimise the parameters and see if we could improve that score and after tuning n_estimators, max_depth ,min_samples_leaf ,min_samples_split, max_features we were able to improve our score to 78%
<br><br>
4. **Findings**
We cleaned the Dataset, and answered the 3 questions which are meant to have direct and immediate effects on deceision making of our client(Real Estate agency)
We were able to explain and show through analysis the price range that is most suitable for them through both the prices and activity, We then showed them the exact locations that met those conditions and even gave them a list of suggested zipcodes that are within the price bands and the number of corrosponding houses being bought and sold in that zipcode.
We finally used different machine learning methods in order to be able to predict the prices of houses based on ceratain prominent features that are most important, This allows us to be able help the real estate agency do two important tasks.
- Be able to predict if a house is worth buying based on the price compared to its features, i.e will the real estate agnecy make a profit by buying/flipping this house?
- as well as be able to make accurate estimations when selling a house to maximize profits for the features the house has, i.e what is a reasonable price to sell a house with these features while making maximum profits
<br><br>
5.  **Future Tasks**
there are a few things i have in mind to do for future works
- Add more features that can effect the prices, a main feature i would like to add more features such as details on geographical locations this would mean collecting more data on specific details on each zipcode or lat/long location such as schools in that area, shopping malls,public transportation, etc. these factors may have a direct negative or positive influence on the price of a house(External factors that affect the price of a house)
- I want to build a pipeline for the whole process, do the Imputation, Transformation and Machine Learning all at once


