<font size="7">**Publicly Available Dataset**</font>

<font size="5">Dataset 1: COVID-19 dataset</font>
<br>**Link:** https://dj2taa9i652rf.cloudfront.net/
<br>**Description:** This directory has different datasets available on COVID-19. My initial search was to find COVID-19 vaccination dataset to find out the effects of vaccination on individuals; it is too soon to say that but it'll be interesting to see if there are any noticible trends. My next approach was to look at the testing data and COVID deaths and see a correlation between different countries.

<font size="5">Dataset 2: Wine data set</font>
<br>**Link:** https://archive.ics.uci.edu/ml/datasets/wine
<br>**Description:** This dataset includes 13 different attributes associated to the chemical analysis of a wine and have a rating associated with each type of wine. This doesn't solve hige world problem but gives an estimate of the quality of wine given a set of features.

<font size="5">Dataset 3: Volcanoes on Venus</font>
<br>**Link:** https://archive.ics.uci.edu/ml/datasets/Volcanoes+on+Venus+-+JARtool+experiment
<br>**Description:** This data was collected by Magellan spacecraft from 1990-1994 with the objective to procure the global mapping of the surface of Venus. The dataset has labels including 1= definitely Volcano, 2= probably, 3= possibly, 4= only a pit is available. It will be interesting to recognize Volcanoes on Venus given a test image of Venus.

<font size="5">Dataset 4: Database of Genome Variants</font>
<br>**Link:** http://genome.ucsc.edu/cgi-bin/hgTrackUi?db=hg19&g=dgvPlus
<br>**Description:** This is the database of Genome Variants that observed the genomic variations in healthy individuals. My interest was to look into these variation and determine if there is any correlation between different parameters that could help predict disease not necessarily in the present but in the next 10-20 years in future. Diseases like Myloma, sickle cell anemia, etc that has no cure currently but could be prevented if early action can be taken.

<font size="5">Dataset 5: Alternative Fuel Vehicles</font>
<br>**Link:** https://afdc.energy.gov/data/
<br>**Description:** This dataset is downloaded from Alternative Fuels Data Centre. It has data on different attributes relating to Alternative Fuel Vehicles such as Annual Vehicle Credits Earned, average range, efficiency of US Electric Vehicles, AFV and HEV model offerings, etc. It can be used to conduct a financial analysis for an individual institution such as Clark when it's making an investment in fleet electrification. 

**<font size="20">Dataset information</font>**


<font size= '5'>Chosen Datset: Wine Dataset</font>


```python
#import libraries
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt


```

<font size="4">Let's load the datasets</font>


```python
data = pd.read_csv('winequality-red.csv', sep = ';')
data.head(10)
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
      <th>fixed acidity</th>
      <th>volatile acidity</th>
      <th>citric acid</th>
      <th>residual sugar</th>
      <th>chlorides</th>
      <th>free sulfur dioxide</th>
      <th>total sulfur dioxide</th>
      <th>density</th>
      <th>pH</th>
      <th>sulphates</th>
      <th>alcohol</th>
      <th>quality</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7.4</td>
      <td>0.70</td>
      <td>0.00</td>
      <td>1.9</td>
      <td>0.076</td>
      <td>11.0</td>
      <td>34.0</td>
      <td>0.9978</td>
      <td>3.51</td>
      <td>0.56</td>
      <td>9.4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>1</th>
      <td>7.8</td>
      <td>0.88</td>
      <td>0.00</td>
      <td>2.6</td>
      <td>0.098</td>
      <td>25.0</td>
      <td>67.0</td>
      <td>0.9968</td>
      <td>3.20</td>
      <td>0.68</td>
      <td>9.8</td>
      <td>5</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7.8</td>
      <td>0.76</td>
      <td>0.04</td>
      <td>2.3</td>
      <td>0.092</td>
      <td>15.0</td>
      <td>54.0</td>
      <td>0.9970</td>
      <td>3.26</td>
      <td>0.65</td>
      <td>9.8</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>11.2</td>
      <td>0.28</td>
      <td>0.56</td>
      <td>1.9</td>
      <td>0.075</td>
      <td>17.0</td>
      <td>60.0</td>
      <td>0.9980</td>
      <td>3.16</td>
      <td>0.58</td>
      <td>9.8</td>
      <td>6</td>
    </tr>
    <tr>
      <th>4</th>
      <td>7.4</td>
      <td>0.70</td>
      <td>0.00</td>
      <td>1.9</td>
      <td>0.076</td>
      <td>11.0</td>
      <td>34.0</td>
      <td>0.9978</td>
      <td>3.51</td>
      <td>0.56</td>
      <td>9.4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>5</th>
      <td>7.4</td>
      <td>0.66</td>
      <td>0.00</td>
      <td>1.8</td>
      <td>0.075</td>
      <td>13.0</td>
      <td>40.0</td>
      <td>0.9978</td>
      <td>3.51</td>
      <td>0.56</td>
      <td>9.4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>6</th>
      <td>7.9</td>
      <td>0.60</td>
      <td>0.06</td>
      <td>1.6</td>
      <td>0.069</td>
      <td>15.0</td>
      <td>59.0</td>
      <td>0.9964</td>
      <td>3.30</td>
      <td>0.46</td>
      <td>9.4</td>
      <td>5</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7.3</td>
      <td>0.65</td>
      <td>0.00</td>
      <td>1.2</td>
      <td>0.065</td>
      <td>15.0</td>
      <td>21.0</td>
      <td>0.9946</td>
      <td>3.39</td>
      <td>0.47</td>
      <td>10.0</td>
      <td>7</td>
    </tr>
    <tr>
      <th>8</th>
      <td>7.8</td>
      <td>0.58</td>
      <td>0.02</td>
      <td>2.0</td>
      <td>0.073</td>
      <td>9.0</td>
      <td>18.0</td>
      <td>0.9968</td>
      <td>3.36</td>
      <td>0.57</td>
      <td>9.5</td>
      <td>7</td>
    </tr>
    <tr>
      <th>9</th>
      <td>7.5</td>
      <td>0.50</td>
      <td>0.36</td>
      <td>6.1</td>
      <td>0.071</td>
      <td>17.0</td>
      <td>102.0</td>
      <td>0.9978</td>
      <td>3.35</td>
      <td>0.80</td>
      <td>10.5</td>
      <td>5</td>
    </tr>
  </tbody>
</table>
</div>



<font size ="4">Let's look at the number of rows and columns and different data types in the dataset</font>


```python
data.shape
```




    (1599, 12)




```python
data.dtypes
```




    fixed acidity           float64
    volatile acidity        float64
    citric acid             float64
    residual sugar          float64
    chlorides               float64
    free sulfur dioxide     float64
    total sulfur dioxide    float64
    density                 float64
    pH                      float64
    sulphates               float64
    alcohol                 float64
    quality                   int64
    dtype: object




```python
data['Date'] = pd.to_datetime(data['pH'])
```


```python
data.dtypes
```




    fixed acidity                  float64
    volatile acidity               float64
    citric acid                    float64
    residual sugar                 float64
    chlorides                      float64
    free sulfur dioxide            float64
    total sulfur dioxide           float64
    density                        float64
    pH                             float64
    sulphates                      float64
    alcohol                        float64
    quality                          int64
    Date                    datetime64[ns]
    dtype: object




```python
AlcoholLevel = data['alcohol'].value_counts().plot(kind='bar', figsize=(40,8))
```


    
![png](output_16_0.png)
    


<font size='4'>This is not very helpful. We should try something else</font>


```python
top10= data['alcohol'].value_counts()
top10.sort_values(ascending= False)
top10= top10[:10]
top10.plot(kind="bar")
```




    <AxesSubplot:>




    
![png](output_18_1.png)
    



```python

```
