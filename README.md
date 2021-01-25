## Prediciting Electricity Usage

*Using Linear Regression and Web Scraping techniques, created model that predicts monthly electricity usage in the State of Louisiana*

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

---
**Data Gathering**

weather_scrape.ipynb
	
	- Notable packages: Selenium, BeautifulSoup
	- Data source: https://www.wunderground.com/
	- Exports:
		○ kenner_scrape.pkl
		○ baton_rouge_scrape.pkl
		○ lake_charles_scrape.pkl
		○ alexandria_scrape.pkl
		○ shreveport_scrape.pkl

weather.ipynb

	- Imports:
		○ Kenner_scrape.pkl
		○ Baton_rouge_scrape.pkl
		○ Lake_charles_scrape.pkl
		○ Alexandria_scrape.pkl
		○ Shreveport_scrape.pkl
	- Exports:
		○ Average_weather.pkl

population.ipynb
	
	- Notable packages: BeautifulSoup
	- Data Source: https://www.macrotrends.net/states/louisiana/population
		○ Compared with US Census data - scraped from site for purposes of using BeautifulSoup
	- Export:
		○ State_pop.pkl

economic_data.ipynb
	
	- Data source: https://www.bea.gov/
	- Imports: 
		○ Personal Income Summary Personal Income, Population, Per Capita Personal Income.csv
		○ Gross Domestic Product (GDP) summary, quarterly by state.csv
		○ Total personal consumption expenditures (PCE).csv
	- Export:
		○ econcomic_data.pkl

building_permits.ipynb
	
	- Notable packages: urllib3
	- Data Source: https://www.census.gov/construction/bps/
	- Import:
		○ permits_2019_11_2020_11.xlsx
	- Export:
		○ Permits.pkl

EIA.ipynb
	
	- Data Source: https://www.eia.gov/
	- Imports:
		○ Retail_sales_of_electricity.csv
		○ Average_retail_price_of_electricity.csv
		○ Number_of_customer_accounts.csv
		○ sales_smpy.xlsx
	- Exports:
		○ sales_price.csv
		○ eia_data.pkl

---
**Merging Data**

Merge_eda.ipynb
	
	- Imports:
		○ eia_data.pkl
		○ permits.pkl
		○ economic_data.pkl
		○ average_weather.pkl
		○ state_pop.pkl
	- Export:
		○ df.pkl

---
**Feature Engineering**

Feature_engineering.ipynb
	
	- Import:
		○ df.pkl
	- Export:
		○ df_all_features.pkl

---
**Linear Regression**

linear_regression_all_features.ipynb
	
	- Notable packages:
		○ Sci-kit learn
		○ Seaborn
	- Import:
		○ df_all_features.pkl

linear_regression_selected_features.ipynb
	
	- Notable packages:
		○ Sci-kit learn
		○ Seaborn
	- Import:
		○ df_all_features.pkl

poly_regression_all_features.ipynb
	
	- Notable packages:
		○ Sci-kit learn
		○ Seaborn
	- Import:
		○ df_all_features.pkl

poly_regression_selected_features.ipynb
	
	- Notable packages:
		○ Sci-kit learn
		○ Seaborn
	- Import:
            ○ df_all_features.pkl





