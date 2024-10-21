# Final Project: Statistical Modelling with Python

## Project Goals
Build a model to predict the rating of bike-sharing stations based on their features. The process involves:
- Gathering data from APIs
- Data cleaning and exploration
- Data visualization
- Model building and prediction

## Process

### 1. Data Collection
- Use Request library to fetch data from api.citybik.es
- Transform JSON to pandas DataFrame and save as CSV
- Collect data from Foursquare and Yelp APIs
- Transform API data to pandas DataFrames and save as CSVs

### 2. Data Joining
- Join DataFrames based on location (latitude and longitude)
- Implement function to calculate distance between points
- Join based on distance < 1000 meters

### 3. Data Cleaning
- Remove duplicate data and rows with missing values
- Drop irrelevant columns (e.g., id, url, single-value columns)
- Convert appropriate columns to numeric data types

### 4. Exploratory Data Analysis
- Create visualizations to explore relationships between rating and other variables

### 5. Model Building
- Implement linear regression model to predict ratings

### 6. Model Evaluation
- Assess model using R-squared and p-value

## Results
- Yelp provided more comprehensive data compared to Foursquare
- Initial model using bike count to predict rating:
  - Statistically significant
  - Low R-squared (0.018)
- Adding features (price, review count, distance):
  - Remained statistically significant
  - R-squared still low
- Conclusion: Selected features not strong predictors of rating

## Challenges
1. API request limitations
   - Careful management of daily request limits
   - Initial single request test before implementing loops

2. Data joining complexities
   - Inexact latitude/longitude matches
   - Distance calculation function implementation
   - Post-model realization: Keeping station IDs could improve join accuracy

3. Model improvement difficulties
   - Easy model building, challenging to enhance performance
   - Low R-squared persisted despite adding features

## Future Goals
1. Enhance data detail
   - Include bike station pricing
   - Incorporate review content

2. Explore alternative models
   - Test different modelling approaches for potential performance improvements