# HCMUS---Statistical-Data-Processing

Team K:

| Fullname    | ID student |
|---------------------|-----------------|
|Lâm Gia Phú |21280104|
| Trần Ngọc Khánh Như | 21280040|
| Trần Minh Hiển | 21280016|
| Nguyễn Đăng Khôi| 21280023|



## Seoul Bike Sharing Demand Prediction

### Table of Contents
1. [Abstract](#abstract)
2. [Introduction](#introduction)
3. [Data Exploration and Preprocessing](#data-exploration-and-preprocessing)
   1. [Data Description](#data-description)
   2. [Data Preprocessing](#data-preprocessing)
4. [Model Building and Evaluation](#model-building-and-evaluation)
   1. [Poisson Regression](#poisson-regression)
   2. [Weighted Regression](#weighted-regression)
   3. [Polynomial Regression](#polynomial-regression)
   4. [Bsplines](#bsplines)
   5. [Generalized Additive Models (GAM)](#generalized-additive-models-gam)
   6. [Random Forest](#random-forest)
5. [Results and Business Strategy](#results-and-business-strategy)
   1. [Prediction Results](#prediction-results)
   2. [Business Strategy](#business-strategy)
6. [Conclusion](#conclusion)
7. [References](#references)

### Abstract
The goal of this project is to forecast Seoul's demand for hourly rental bikes using a variety of regression models. Poisson, Weighted, Polynomial, Bsplines, Random Forest, and Generalized Additive Models (GAM) are some of the models that were assessed. Finding the best model to predict bike rentals, guarantee consistent bike availability, and shorten customer wait times is the main objective.

### Introduce
The goal of Seoul's bike-sharing program is to offer practical and environmentally friendly modes of transportation. Accurately forecasting bike demand is essential for preserving the ideal fleet size, cutting down on wait times, and guaranteeing client satisfaction. In order to determine which model performs the best at forecasting the demand for hourly bike rentals, this study investigates a number of regression techniques.
### Data Exploration and Preprocessing

#### Data Description
The dataset used in this study is the Seoul Bike Data, which includes various features such as:
- **Rented Bike Count:** The number of bikes rented each hour.
- **Temperature (°C):** The temperature in degrees Celsius.
- **Humidity (%):** The humidity percentage.
- **Wind speed (m/s):** The wind speed in meters per second.
- **Dew point temperature (°C):** The dew point temperature in degrees Celsius.
- **Solar Radiation (MJ/m²):** The solar radiation in megajoules per square meter.
- **Rainfall (mm):** The amount of rainfall in millimeters.
- **Snowfall (cm):** The amount of snowfall in centimeters.
- **Hour:** The hour of the day.
- **Seasons:** The season of the year.
- **Holiday:** Indicates whether the day is a holiday.
- **Functional Day:** Indicates whether the day is a working day.

#### Data Preprocessing
- **Date Conversion:** Convert date columns to appropriate date formats.
- **Categorical Variables:** Create categorical variables for hour, seasons, holiday, and functional day.
- **Missing Values:** Handle missing values through imputation or removal.
- **Normalization:** Normalize continuous variables to ensure consistency in scale.

### Model Building and Evaluation
Six regression models were built and evaluated for their effectiveness in predicting bike rentals.

#### Poisson Regression
- **R-squared:** 0.79
- **Description:** Suitable for count data, explaining 79% of the variance.

#### Weighted Regression
- **R-squared:** 0.66
- **Description:** Addresses heteroscedasticity, explaining 66% of the variance.

#### Polynomial Regression
- **R-squared:** 0.66
- **Description:** Handles simple nonlinear relationships, explaining 66% of the variance.

#### Bsplines
- **R-squared:** 0.69
- **Description:** Uses piecewise polynomials for smooth curves, explaining 69% of the variance.

#### Generalized Additive Models (GAM)
- **R-squared:** 0.72
- **Description:** Captures complex nonlinear relationships, explaining 72% of the variance.

#### Random Forest
- **R-squared:** 0.97
- **Description:** Utilizes multiple decision trees, explaining 97% of the variance and providing the best performance.

### Results and Business Strategy

#### Prediction Results
- The **Random Forest** model showed the highest R-squared value (0.97), indicating superior predictive power.
- **Poisson Regression** (R-squared: 0.79) and **GAM** (R-squared: 0.72) were also effective for simpler and more interpretable models.

#### Business Strategy
- **Time-Based Planning:** Ensure adequate bike availability during peak hours.
- **Seasonal Adjustment:** Increase bike fleet during spring and summer.
- **Holiday Management:** Prepare for higher demand on holidays and weekends.
- **Weather Considerations:** Adjust bike supply based on weather forecasts.

### Conclusion
The Random Forest model demonstrated exceptional performance in predicting bike rental demand, making it the most suitable choice for this application. By leveraging these predictive insights, the bike-sharing program can optimize bike availability, enhance customer experience, and ensure efficient resource allocation.

### References
- Waleed Ejaz. Seoul Bike Sharing - EDA & XGBRegressor. Kaggle. Retrieved from [Kaggle](https://www.kaggle.com/code/waleedejaz/seoul-bike-sharing-eda-xgbregressor).
- Nayana CK. Seoul Bike Data Analysis. Kaggle. Retrieved from [Kaggle](https://www.kaggle.com/code/nayanack/seoul-bike-data-analysis).
- Syed Sharin. Seoul Bike Sharing Demand Prediction. GitHub. Retrieved from [GitHub](https://github.com/syedsharin/Seoul-Bike-Sharing-Demand-Prediction).
- ResearchGate. Seoul Bike data variables and description. Retrieved from [ResearchGate](https://www.researchgate.net/figure/Seoul-Bike-data-variables-and-description_tbl1_339266153).
- Dancer World. Project Title: Seoul Bike Sharing Demand Prediction. Medium. Retrieved from [Medium](https://medium.com/@dancerworld60/project-title-seoul-bike-sharing-demand-prediction-e1be18f23cbe).

By using these models, the bike-sharing service can strategically plan and execute business strategies to ensure a stable and efficient bike rental system, ultimately improving customer satisfaction.
