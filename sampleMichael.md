# Publicly available datasets 

## Dataset 1:
- Link:https://databank.worldbank.org/reports.aspx?source=world-development-indicators
- Purpose: This a publicly available dataset from the World Bank, officially known as World Development Indicators (WDI). It is a compilation of relevant, high-quality, and comparable indicators. The database contains 1,400 time series indicators for 217 economies and more than 40 country groups, with data for many indicators going back more than 50 years. I am planning to use some of the indicators in this data set (GDP percapita as my label variable) and lots of other training variables (like infrastructure and the like) to explain the contribution of each variable to predict GDP percapita and model the future contribution of infrastructure development to the development of countries specifically in Africa.

## Dataset 2:
- Link https://covidtracking.com/data/download 
- Purpose: This dataset is a CSV file that contains daily data on the COVID-19 pandemic for US and individual states. All dates and times are in US eastern time (ET). Each state has its own set of caveats, which we have documented on our data page. I intend to use these data to track for specific patterns (anomalies) in COVID-19 infections and by merging it to other datasets analyze the relationships between other indicators and COVID-infections. Potentially provide a good insight for policy makers in their fight to put this pandemic under control.  

## Dataset 3:
- Link: https://ourworldindata.org/coronavirus-source-data
- Purpose: This dataset linked multiple data sources with the Complete COVID-19 dataset on confirmed cases and deaths from Johns Hopkins University (JHU).  JHU updates its data multiple times each day. This data is sourced from governments, national and subnational agencies across the world. Here I intend to link up multiple indicators with the label variable (COVID-19) and conduct worldwide analysis on what determines the spread and explain the geographic variations.

## Dataset 4:
- Link: https://comtrade.un.org/data/
- Purpose: This a detailed global trade data. UNCOMTRADE is a repository of official international trade statistics and relevant analytical tables. I have already downloaded, cleaned, and merged this data with multiple datasets (Used in my first paper of the dissertation). The label variable (Bilateral import by year) and lots of other variables are used to explain the within and between variations in the label variable. Most importantly, infrastructure (LPI Index), landlockedness(binary variable (1 =  Landlocked, 0 = Coastal)) and geography (Elevation and distance from the centroid of a country to the nearest sea) 

## Dataset 5:
- Link: http://www.cepii.fr/CEPII/en/bdd_modele/bdd.asp
- Purpose: The Gravity database contains variables to estimate what is known as “gravity equations” in international trade. This dataset contains large set of; Bilateral trade flows, from three distinct sources: IMF (DOTS), the UN (Comtrade) and the BACI database from CEPII. Geographical distance, including distances that reflect the within-country spatial distribution of activity. Trade facilitation measures: GATT/WTO membership, existence of trade agreements and nature of these agreements. Proxies for cultural proximity: language, religion, origins of the legal system, colonial ties, etc. Macroeconomic indicators: GDP, population, etc. For any country pair existing between 1948 and 2019.  


```python
print("Importing important liberaries")
print('The chosen dataset for this assignment is "****DATASET3****"')
print("This program analyzes Covid-19 spread around the world")
import pandas as pd
import os
import csv
from datetime import datetime as dt
import random as rand
import matplotlib.pyplot as plt
import matplotlib.ticker as mtick
import numpy as np

```

    Importing important liberaries
    This program analyzes Covid-19 spread around the world
    


```python
variables = pd.read_csv(r"C:\Users\micha\Desktop\finalpython\owid-covid-data.csv")
variables.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>iso_code</th>
      <th>continent</th>
      <th>location</th>
      <th>date</th>
      <th>total_cases</th>
      <th>new_cases</th>
      <th>new_cases_smoothed</th>
      <th>total_deaths</th>
      <th>new_deaths</th>
      <th>new_deaths_smoothed</th>
      <th>...</th>
      <th>gdp_per_capita</th>
      <th>extreme_poverty</th>
      <th>cardiovasc_death_rate</th>
      <th>diabetes_prevalence</th>
      <th>female_smokers</th>
      <th>male_smokers</th>
      <th>handwashing_facilities</th>
      <th>hospital_beds_per_thousand</th>
      <th>life_expectancy</th>
      <th>human_development_index</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Afghanistan</td>
      <td>2020-02-24</td>
      <td>1.0</td>
      <td>1.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>1803.987</td>
      <td>NaN</td>
      <td>597.029</td>
      <td>9.59</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>37.746</td>
      <td>0.5</td>
      <td>64.83</td>
      <td>0.511</td>
    </tr>
    <tr>
      <th>1</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Afghanistan</td>
      <td>2020-02-25</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>1803.987</td>
      <td>NaN</td>
      <td>597.029</td>
      <td>9.59</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>37.746</td>
      <td>0.5</td>
      <td>64.83</td>
      <td>0.511</td>
    </tr>
    <tr>
      <th>2</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Afghanistan</td>
      <td>2020-02-26</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>1803.987</td>
      <td>NaN</td>
      <td>597.029</td>
      <td>9.59</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>37.746</td>
      <td>0.5</td>
      <td>64.83</td>
      <td>0.511</td>
    </tr>
    <tr>
      <th>3</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Afghanistan</td>
      <td>2020-02-27</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>1803.987</td>
      <td>NaN</td>
      <td>597.029</td>
      <td>9.59</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>37.746</td>
      <td>0.5</td>
      <td>64.83</td>
      <td>0.511</td>
    </tr>
    <tr>
      <th>4</th>
      <td>AFG</td>
      <td>Asia</td>
      <td>Afghanistan</td>
      <td>2020-02-28</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>...</td>
      <td>1803.987</td>
      <td>NaN</td>
      <td>597.029</td>
      <td>9.59</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>37.746</td>
      <td>0.5</td>
      <td>64.83</td>
      <td>0.511</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 59 columns</p>
</div>




```python
covid = [row for row in variables]
# Poping indices 
## <0> iso_code <2> location
headings = covid.pop(0)
locations = list(set([x[1] for x in covid]))

```


```python

# Visualize the data  
for item in covid:
    print(item)
        

```

    continent
    location
    date
    total_cases
    new_cases
    new_cases_smoothed
    total_deaths
    new_deaths
    new_deaths_smoothed
    total_cases_per_million
    new_cases_per_million
    new_cases_smoothed_per_million
    total_deaths_per_million
    new_deaths_per_million
    new_deaths_smoothed_per_million
    reproduction_rate
    icu_patients
    icu_patients_per_million
    hosp_patients
    hosp_patients_per_million
    weekly_icu_admissions
    weekly_icu_admissions_per_million
    weekly_hosp_admissions
    weekly_hosp_admissions_per_million
    new_tests
    total_tests
    total_tests_per_thousand
    new_tests_per_thousand
    new_tests_smoothed
    new_tests_smoothed_per_thousand
    positive_rate
    tests_per_case
    tests_units
    total_vaccinations
    people_vaccinated
    people_fully_vaccinated
    new_vaccinations
    new_vaccinations_smoothed
    total_vaccinations_per_hundred
    people_vaccinated_per_hundred
    people_fully_vaccinated_per_hundred
    new_vaccinations_smoothed_per_million
    stringency_index
    population
    population_density
    median_age
    aged_65_older
    aged_70_older
    gdp_per_capita
    extreme_poverty
    cardiovasc_death_rate
    diabetes_prevalence
    female_smokers
    male_smokers
    handwashing_facilities
    hospital_beds_per_thousand
    life_expectancy
    human_development_index
    


```python
## Picking United states as an example
country= "United States" 
date=[covid[2] for x in covid if x[1]==country]
newVaccinations=[item[37] for item in covid if covid[1]==country]
```
