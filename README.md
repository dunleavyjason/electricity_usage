## Prediciting Electricity Usage

*Using Linear Regression and Web Scraping techniques, created model that predicts monthly electricity usage in the State of Louisiana*

*Utilized web scraping (Selenium and BeautifulSoup) to gather data from dynamically generated web pages. Implemented various modeling techniques such as feature engineering, autoregression, and lasso regularization. Final model predicting monthly electricity usage in the State of Louisiana performed with an r-squared of 90 percent and a mean absolute error of 243 MWh.*

---
### Features and Target Variable
**Target Variable:** Electricity Sales

**Features:**
1. Sales - Same Month, Prior Year
2. Number of Customer Accounts
3. Number of New Construction Permits
4. Average Humidity Percentange
5. Average Wind Speed
6. Average Temperature (absolute deviation from 65 degrees)
7. Average Heating/Cooling Degree Day
8. Personal Income
9. Real GDP
10. Consumer Spending
11. Population
12. Population per account
13. Humidity*Wind
14. Humidity*Temp
15. Wind*Temp

---

### Data Used
U.S. Energy Information Administration:
https://www.eia.gov/

WeatherUnderground:
https://www.wunderground.com/

Population:
https://www.macrotrends.net/states/louisiana/population

Construction Permits:
https://www.census.gov/construction/bps/statemonthly.html

U.S. Department of Commerce - Bureau of Economic Analysis:
https://www.bea.gov/

---

### Tools and Packages
1. Python
2. Pandas
3. NumPy
4. matplotlip
5. seaborn
6. Selenium
7. BeautifulSoup
8. scikit-learn
9. urllib3

---

### Repo Guide

**Data Gathering**
1. Scrape historical weather data - [weather_scrape.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/weather_scrape.ipynb)
2. Average weather info - [weather.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/weather.ipynb)
3. Scrape population data - [population.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/population.ipynb)
4. Import economic data - [economic_data.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/economic_data.ipynb)
5. Import building permit data - [building_permits.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/building_permits.ipynb)
6. Import EIA (electricity) data - [EIA.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/EIA.ipynb)

**Merging Data**

1. Merge data into one dataframe - [merge_eda.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/merge_eda.ipynb)

**Feature Engineering**

1. Perform feature engineering - [feature_engineering.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/feature_engineering.ipynb)

**Linear Regression**

1. Linear Regression: All Features - [linear_regression_all_features.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/linear_regression_all_features.ipynb)
2. Linear Regression: Selected Features - [linear_regression_selected_features.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/linear_regression_selected_features.ipynb)
3. Polynomial Regression: All Features - [poly_regression_all_features.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/poly_regression_all_features.ipynb)
4. Polynomial Regression: Selected Features - [poly_regression_selected_features.ipynb](https://github.com/dunleavyjason/electricity_usage/blob/main/poly_regression_selected_features.ipynb)

