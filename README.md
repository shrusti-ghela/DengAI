# DengAI - Predicting the disease spread

### Challenge Summary

Can you predict local epidemics of dengue fever?

Dengue fever is a mosquito-borne disease that occurs in tropical and sub-tropical parts of the world. In mild cases, symptoms are similar to the flu: fever, rash, and muscle and joint pain. In severe cases, dengue fever can cause severe bleeding, low blood pressure, and even death.

Because it is carried by mosquitoes, the transmission dynamics of dengue are related to climate variables such as temperature and precipitation. Although the relationship to climate is complex, a growing number of scientists argue that climate change is likely to produce distributional shifts that will have significant public health implications worldwide.

In recent years dengue fever has been spreading. Historically, the disease has been most prevalent in Southeast Asia and the Pacific islands. These days many of the nearly half billion cases per year are occurring in Latin America


Your goal is to predict the total_cases label for each (city, year, weekofyear) in the test set. There are two cities, San Juan and Iquitos, with test data for each city spanning 5 and 3 years respectively. You will make one submission that contains predictions for both cities. The data for each city have been concatenated along with a city column indicating the source: sj for San Juan and iq for Iquitos. The test set is a pure future hold-out, meaning the test data are sequential and non-overlapping with any of the training data. Throughout, missing values have been filled as NaNs.


### My Approach

#### Preprocessing

- Exploratory Data Analysis
- Data Cleaning 
  - Handling missing values
  - Data integration
- Data Normalization

#### Data Modelling

- Correlation between features
- Feature Selection
- Engineering new features

#### Comparing models

| Model  | MAE for SJ  | MAE for IQ  |
|---|---|---|
|Linear Regression   | 27.826  | 6.334  |
|K-Nearest Neighbour Regression | 25.240  | 6.033  |
|Support Vector Regression (linear kernel)   |  23.035 | 5.585 |
|Support Vector Regression (rbf kernel) | 21.931 | 5.551 |
|Gradient Boosting | 20.644 | 5.523 |
|Random Forest Regression |18.984 | 5.441 |

#### Further Processing of selected models and final model selection

