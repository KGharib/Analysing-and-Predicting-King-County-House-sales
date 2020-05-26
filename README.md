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

