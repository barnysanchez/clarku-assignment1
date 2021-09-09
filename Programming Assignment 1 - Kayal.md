# Dataset 1:
- Link: https://www.kaggle.com/fivethirtyeight/uber-pickups-in-new-york-city- Purpose: This dataset can be used to find the peak Uber ride hours for each day in NYC.
# Dataset 2:
- Link: https://www.kaggle.com/terenceshin/covid19s-impact-on-airport-traffic- Purpose: This dataset can be used to find the impact of covid-19 on airport traffic for the given countries.
# Dataset 3:
- Link: https://www.kaggle.com/kingabzpro/singapore-waste-management- Purpose: This dataset can be used to find the proportions of the type of waste that contributes to the total waste generated in Singapore.
# Dataset 4: 
- Link: https://www.kaggle.com/gpreda/covid-world-vaccination-progress- Purpose: This dataset can be used to find the top 5 countries which has the maximum vaccination rate.
# Dataset 5: 
- Link: https://www.kaggle.com/shivamb/netflix-shows- Purpose: This dataset can be used to identify the ratio of Movies to TV shows in each available countries. 
# Chosen Dataset:  Dataset 2


```python
import pandas as pd  
import numpy as np
import matplotlib.pyplot as plt
covidimpact_on_air = pd.read_csv(r'C:\Users\kayal\Desktop\ML\covid_impact_on_airport_traffic.csv')
covidimpact_on_air.head() 
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
      <th>AggregationMethod</th>
      <th>Date</th>
      <th>Version</th>
      <th>AirportName</th>
      <th>PercentOfBaseline</th>
      <th>Centroid</th>
      <th>City</th>
      <th>State</th>
      <th>ISO_3166_2</th>
      <th>Country</th>
      <th>Geography</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Daily</td>
      <td>2020-04-03</td>
      <td>1.0</td>
      <td>Kingsford Smith</td>
      <td>64</td>
      <td>POINT(151.180087713813 -33.9459774986125)</td>
      <td>Sydney</td>
      <td>New South Wales</td>
      <td>AU</td>
      <td>Australia</td>
      <td>POLYGON((151.164354085922 -33.9301772341877, 1...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Daily</td>
      <td>2020-04-13</td>
      <td>1.0</td>
      <td>Kingsford Smith</td>
      <td>29</td>
      <td>POINT(151.180087713813 -33.9459774986125)</td>
      <td>Sydney</td>
      <td>New South Wales</td>
      <td>AU</td>
      <td>Australia</td>
      <td>POLYGON((151.164354085922 -33.9301772341877, 1...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Daily</td>
      <td>2020-07-10</td>
      <td>1.0</td>
      <td>Kingsford Smith</td>
      <td>54</td>
      <td>POINT(151.180087713813 -33.9459774986125)</td>
      <td>Sydney</td>
      <td>New South Wales</td>
      <td>AU</td>
      <td>Australia</td>
      <td>POLYGON((151.164354085922 -33.9301772341877, 1...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Daily</td>
      <td>2020-09-02</td>
      <td>1.0</td>
      <td>Kingsford Smith</td>
      <td>18</td>
      <td>POINT(151.180087713813 -33.9459774986125)</td>
      <td>Sydney</td>
      <td>New South Wales</td>
      <td>AU</td>
      <td>Australia</td>
      <td>POLYGON((151.164354085922 -33.9301772341877, 1...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Daily</td>
      <td>2020-10-31</td>
      <td>1.0</td>
      <td>Kingsford Smith</td>
      <td>22</td>
      <td>POINT(151.180087713813 -33.9459774986125)</td>
      <td>Sydney</td>
      <td>New South Wales</td>
      <td>AU</td>
      <td>Australia</td>
      <td>POLYGON((151.164354085922 -33.9301772341877, 1...</td>
    </tr>
  </tbody>
</table>
</div>




```python
Country_count = pd.DataFrame(covidimpact_on_air["Country"].value_counts())
g = Country_count.plot.bar(figsize=(7, 7), color = 'green')
plt.title('EACH COUNTRIES AIRPORT TRAFFIC DURING COVID-19')
plt.xlabel('Country')
plt.ylabel('No.of. Record')
```




    Text(0, 0.5, 'No.of. Record')




    
![png](output_17_1.png)
    



```python
Mass_Data = covidimpact_on_air[(covidimpact_on_air.State == 'Massachusetts')]
Mass_Data.plot(x = 'Date', y = 'PercentOfBaseline', title = 'Massachusetts Baseline data from March 2020 to December 2020')
plt.xticks(rotation=45)
```




    (array([-50.,   0.,  50., 100., 150., 200., 250., 300.]),
     [Text(-50.0, 0, '2020-09-01'),
      Text(0.0, 0, '2020-04-03'),
      Text(50.0, 0, '2020-07-03'),
      Text(100.0, 0, '2020-11-01'),
      Text(150.0, 0, '2020-11-25'),
      Text(200.0, 0, '2020-09-25'),
      Text(250.0, 0, '2020-04-27'),
      Text(300.0, 0, '')])




    
![png](output_18_1.png)
    



```python
US_only = covidimpact_on_air.loc[covidimpact_on_air.Country == "United States of America (the)"]
State_baseline = (US_only.groupby('State').PercentOfBaseline.sum())
State_baseline.plot.pie(y="State", autopct='%1.0f%%', pctdistance=0.9, labeldistance=1.2, title = "Percent of baseline for each U.S. state")
plt.ylabel("")
```




    Text(0, 0.5, '')




    
![png](output_19_1.png)
    

