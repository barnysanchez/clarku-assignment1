```python
import pandas as pd
data1 = pd.read_csv("/Users/tinklejain/Desktop/creditcard.csv")
data2=pd.read_csv("/Users/tinklejain/Downloads/healthcare/train_data.csv")
data3=pd.read_csv("/Users/tinklejain/Downloads/Space_Corrected.csv")
data4=pd.read_csv("/Users/tinklejain/Downloads/818027-1400106-bundle-archive/written_name_test_v2.csv")
data5=pd.read_csv("/Users/tinklejain/Desktop/database.csv")
```

# DATA SET 1

CREDIT CARD FRAUD DETECTION

CONTENT: COMPANIES SHOULD BE ABLE TO RECOGNIZE FRAUD TRANSACTION SO CUSTOMERS ARE NOT CHARGED FOR THINGS THEY HAVE NOT PURCHASED


```python
data1.head()

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
      <th>Time</th>
      <th>V1</th>
      <th>V2</th>
      <th>V3</th>
      <th>V4</th>
      <th>V5</th>
      <th>V6</th>
      <th>V7</th>
      <th>V8</th>
      <th>V9</th>
      <th>...</th>
      <th>V21</th>
      <th>V22</th>
      <th>V23</th>
      <th>V24</th>
      <th>V25</th>
      <th>V26</th>
      <th>V27</th>
      <th>V28</th>
      <th>Amount</th>
      <th>Class</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.0</td>
      <td>-1.359807</td>
      <td>-0.072781</td>
      <td>2.536347</td>
      <td>1.378155</td>
      <td>-0.338321</td>
      <td>0.462388</td>
      <td>0.239599</td>
      <td>0.098698</td>
      <td>0.363787</td>
      <td>...</td>
      <td>-0.018307</td>
      <td>0.277838</td>
      <td>-0.110474</td>
      <td>0.066928</td>
      <td>0.128539</td>
      <td>-0.189115</td>
      <td>0.133558</td>
      <td>-0.021053</td>
      <td>149.62</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.0</td>
      <td>1.191857</td>
      <td>0.266151</td>
      <td>0.166480</td>
      <td>0.448154</td>
      <td>0.060018</td>
      <td>-0.082361</td>
      <td>-0.078803</td>
      <td>0.085102</td>
      <td>-0.255425</td>
      <td>...</td>
      <td>-0.225775</td>
      <td>-0.638672</td>
      <td>0.101288</td>
      <td>-0.339846</td>
      <td>0.167170</td>
      <td>0.125895</td>
      <td>-0.008983</td>
      <td>0.014724</td>
      <td>2.69</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1.0</td>
      <td>-1.358354</td>
      <td>-1.340163</td>
      <td>1.773209</td>
      <td>0.379780</td>
      <td>-0.503198</td>
      <td>1.800499</td>
      <td>0.791461</td>
      <td>0.247676</td>
      <td>-1.514654</td>
      <td>...</td>
      <td>0.247998</td>
      <td>0.771679</td>
      <td>0.909412</td>
      <td>-0.689281</td>
      <td>-0.327642</td>
      <td>-0.139097</td>
      <td>-0.055353</td>
      <td>-0.059752</td>
      <td>378.66</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1.0</td>
      <td>-0.966272</td>
      <td>-0.185226</td>
      <td>1.792993</td>
      <td>-0.863291</td>
      <td>-0.010309</td>
      <td>1.247203</td>
      <td>0.237609</td>
      <td>0.377436</td>
      <td>-1.387024</td>
      <td>...</td>
      <td>-0.108300</td>
      <td>0.005274</td>
      <td>-0.190321</td>
      <td>-1.175575</td>
      <td>0.647376</td>
      <td>-0.221929</td>
      <td>0.062723</td>
      <td>0.061458</td>
      <td>123.50</td>
      <td>0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2.0</td>
      <td>-1.158233</td>
      <td>0.877737</td>
      <td>1.548718</td>
      <td>0.403034</td>
      <td>-0.407193</td>
      <td>0.095921</td>
      <td>0.592941</td>
      <td>-0.270533</td>
      <td>0.817739</td>
      <td>...</td>
      <td>-0.009431</td>
      <td>0.798278</td>
      <td>-0.137458</td>
      <td>0.141267</td>
      <td>-0.206010</td>
      <td>0.502292</td>
      <td>0.219422</td>
      <td>0.215153</td>
      <td>69.99</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 31 columns</p>
</div>



# DATA SET 2

HEALTHCARE ANALYSIS

CONTENT:PATIENT LENGTH OF STAY AT HOSPITAL PARAMETER TO IMPROVE EFFICIENCY OF MGMT


```python
data2
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
      <th>case_id</th>
      <th>Hospital_code</th>
      <th>Hospital_type_code</th>
      <th>City_Code_Hospital</th>
      <th>Hospital_region_code</th>
      <th>Available Extra Rooms in Hospital</th>
      <th>Department</th>
      <th>Ward_Type</th>
      <th>Ward_Facility_Code</th>
      <th>Bed Grade</th>
      <th>patientid</th>
      <th>City_Code_Patient</th>
      <th>Type of Admission</th>
      <th>Severity of Illness</th>
      <th>Visitors with Patient</th>
      <th>Age</th>
      <th>Admission_Deposit</th>
      <th>Stay</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>8</td>
      <td>c</td>
      <td>3</td>
      <td>Z</td>
      <td>3</td>
      <td>radiotherapy</td>
      <td>R</td>
      <td>F</td>
      <td>2.0</td>
      <td>31397</td>
      <td>7.0</td>
      <td>Emergency</td>
      <td>Extreme</td>
      <td>2</td>
      <td>51-60</td>
      <td>4911.0</td>
      <td>0-10</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>2</td>
      <td>c</td>
      <td>5</td>
      <td>Z</td>
      <td>2</td>
      <td>radiotherapy</td>
      <td>S</td>
      <td>F</td>
      <td>2.0</td>
      <td>31397</td>
      <td>7.0</td>
      <td>Trauma</td>
      <td>Extreme</td>
      <td>2</td>
      <td>51-60</td>
      <td>5954.0</td>
      <td>41-50</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>10</td>
      <td>e</td>
      <td>1</td>
      <td>X</td>
      <td>2</td>
      <td>anesthesia</td>
      <td>S</td>
      <td>E</td>
      <td>2.0</td>
      <td>31397</td>
      <td>7.0</td>
      <td>Trauma</td>
      <td>Extreme</td>
      <td>2</td>
      <td>51-60</td>
      <td>4745.0</td>
      <td>31-40</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>26</td>
      <td>b</td>
      <td>2</td>
      <td>Y</td>
      <td>2</td>
      <td>radiotherapy</td>
      <td>R</td>
      <td>D</td>
      <td>2.0</td>
      <td>31397</td>
      <td>7.0</td>
      <td>Trauma</td>
      <td>Extreme</td>
      <td>2</td>
      <td>51-60</td>
      <td>7272.0</td>
      <td>41-50</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>26</td>
      <td>b</td>
      <td>2</td>
      <td>Y</td>
      <td>2</td>
      <td>radiotherapy</td>
      <td>S</td>
      <td>D</td>
      <td>2.0</td>
      <td>31397</td>
      <td>7.0</td>
      <td>Trauma</td>
      <td>Extreme</td>
      <td>2</td>
      <td>51-60</td>
      <td>5558.0</td>
      <td>41-50</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>318433</th>
      <td>318434</td>
      <td>6</td>
      <td>a</td>
      <td>6</td>
      <td>X</td>
      <td>3</td>
      <td>radiotherapy</td>
      <td>Q</td>
      <td>F</td>
      <td>4.0</td>
      <td>86499</td>
      <td>23.0</td>
      <td>Emergency</td>
      <td>Moderate</td>
      <td>3</td>
      <td>41-50</td>
      <td>4144.0</td>
      <td>11-20</td>
    </tr>
    <tr>
      <th>318434</th>
      <td>318435</td>
      <td>24</td>
      <td>a</td>
      <td>1</td>
      <td>X</td>
      <td>2</td>
      <td>anesthesia</td>
      <td>Q</td>
      <td>E</td>
      <td>4.0</td>
      <td>325</td>
      <td>8.0</td>
      <td>Urgent</td>
      <td>Moderate</td>
      <td>4</td>
      <td>81-90</td>
      <td>6699.0</td>
      <td>31-40</td>
    </tr>
    <tr>
      <th>318435</th>
      <td>318436</td>
      <td>7</td>
      <td>a</td>
      <td>4</td>
      <td>X</td>
      <td>3</td>
      <td>gynecology</td>
      <td>R</td>
      <td>F</td>
      <td>4.0</td>
      <td>125235</td>
      <td>10.0</td>
      <td>Emergency</td>
      <td>Minor</td>
      <td>3</td>
      <td>71-80</td>
      <td>4235.0</td>
      <td>11-20</td>
    </tr>
    <tr>
      <th>318436</th>
      <td>318437</td>
      <td>11</td>
      <td>b</td>
      <td>2</td>
      <td>Y</td>
      <td>3</td>
      <td>anesthesia</td>
      <td>Q</td>
      <td>D</td>
      <td>3.0</td>
      <td>91081</td>
      <td>8.0</td>
      <td>Trauma</td>
      <td>Minor</td>
      <td>5</td>
      <td>11-20</td>
      <td>3761.0</td>
      <td>11-20</td>
    </tr>
    <tr>
      <th>318437</th>
      <td>318438</td>
      <td>19</td>
      <td>a</td>
      <td>7</td>
      <td>Y</td>
      <td>5</td>
      <td>gynecology</td>
      <td>Q</td>
      <td>C</td>
      <td>2.0</td>
      <td>21641</td>
      <td>8.0</td>
      <td>Emergency</td>
      <td>Minor</td>
      <td>2</td>
      <td>11-20</td>
      <td>4752.0</td>
      <td>0-10</td>
    </tr>
  </tbody>
</table>
<p>318438 rows × 18 columns</p>
</div>



# DATA SET 3

SPACE MISSIONS

CONTENT: MISSIONS SINCE 1957


```python
data3
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
      <th>Unnamed: 0</th>
      <th>Unnamed: 0.1</th>
      <th>Company Name</th>
      <th>Location</th>
      <th>Datum</th>
      <th>Detail</th>
      <th>Status Rocket</th>
      <th>Rocket</th>
      <th>Status Mission</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>SpaceX</td>
      <td>LC-39A, Kennedy Space Center, Florida, USA</td>
      <td>Fri Aug 07, 2020 05:12 UTC</td>
      <td>Falcon 9 Block 5 | Starlink V1 L9 &amp; BlackSky</td>
      <td>StatusActive</td>
      <td>50.0</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>1</td>
      <td>CASC</td>
      <td>Site 9401 (SLS-2), Jiuquan Satellite Launch Ce...</td>
      <td>Thu Aug 06, 2020 04:01 UTC</td>
      <td>Long March 2D | Gaofen-9 04 &amp; Q-SAT</td>
      <td>StatusActive</td>
      <td>29.75</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>2</td>
      <td>SpaceX</td>
      <td>Pad A, Boca Chica, Texas, USA</td>
      <td>Tue Aug 04, 2020 23:57 UTC</td>
      <td>Starship Prototype | 150 Meter Hop</td>
      <td>StatusActive</td>
      <td>NaN</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>3</td>
      <td>Roscosmos</td>
      <td>Site 200/39, Baikonur Cosmodrome, Kazakhstan</td>
      <td>Thu Jul 30, 2020 21:25 UTC</td>
      <td>Proton-M/Briz-M | Ekspress-80 &amp; Ekspress-103</td>
      <td>StatusActive</td>
      <td>65.0</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>4</td>
      <td>ULA</td>
      <td>SLC-41, Cape Canaveral AFS, Florida, USA</td>
      <td>Thu Jul 30, 2020 11:50 UTC</td>
      <td>Atlas V 541 | Perseverance</td>
      <td>StatusActive</td>
      <td>145.0</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>4319</th>
      <td>4319</td>
      <td>4319</td>
      <td>US Navy</td>
      <td>LC-18A, Cape Canaveral AFS, Florida, USA</td>
      <td>Wed Feb 05, 1958 07:33 UTC</td>
      <td>Vanguard | Vanguard TV3BU</td>
      <td>StatusRetired</td>
      <td>NaN</td>
      <td>Failure</td>
    </tr>
    <tr>
      <th>4320</th>
      <td>4320</td>
      <td>4320</td>
      <td>AMBA</td>
      <td>LC-26A, Cape Canaveral AFS, Florida, USA</td>
      <td>Sat Feb 01, 1958 03:48 UTC</td>
      <td>Juno I | Explorer 1</td>
      <td>StatusRetired</td>
      <td>NaN</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>4321</th>
      <td>4321</td>
      <td>4321</td>
      <td>US Navy</td>
      <td>LC-18A, Cape Canaveral AFS, Florida, USA</td>
      <td>Fri Dec 06, 1957 16:44 UTC</td>
      <td>Vanguard | Vanguard TV3</td>
      <td>StatusRetired</td>
      <td>NaN</td>
      <td>Failure</td>
    </tr>
    <tr>
      <th>4322</th>
      <td>4322</td>
      <td>4322</td>
      <td>RVSN USSR</td>
      <td>Site 1/5, Baikonur Cosmodrome, Kazakhstan</td>
      <td>Sun Nov 03, 1957 02:30 UTC</td>
      <td>Sputnik 8K71PS | Sputnik-2</td>
      <td>StatusRetired</td>
      <td>NaN</td>
      <td>Success</td>
    </tr>
    <tr>
      <th>4323</th>
      <td>4323</td>
      <td>4323</td>
      <td>RVSN USSR</td>
      <td>Site 1/5, Baikonur Cosmodrome, Kazakhstan</td>
      <td>Fri Oct 04, 1957 19:28 UTC</td>
      <td>Sputnik 8K71PS | Sputnik-1</td>
      <td>StatusRetired</td>
      <td>NaN</td>
      <td>Success</td>
    </tr>
  </tbody>
</table>
<p>4324 rows × 9 columns</p>
</div>



# DATA SET 4

HANDWRITING RECOGNITION

CONTENT:CHARACTER RECOGNITION


```python
data4
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
      <th>FILENAME</th>
      <th>IDENTITY</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>TEST_0001.jpg</td>
      <td>KEVIN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>TEST_0002.jpg</td>
      <td>CLOTAIRE</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TEST_0003.jpg</td>
      <td>LENA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>TEST_0004.jpg</td>
      <td>JULES</td>
    </tr>
    <tr>
      <th>4</th>
      <td>TEST_0005.jpg</td>
      <td>CHERPIN</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>41365</th>
      <td>TEST_41366.jpg</td>
      <td>ALEXANE</td>
    </tr>
    <tr>
      <th>41366</th>
      <td>TEST_41367.jpg</td>
      <td>PEREIRA-SILVA</td>
    </tr>
    <tr>
      <th>41367</th>
      <td>TEST_41368.jpg</td>
      <td>LAURENT</td>
    </tr>
    <tr>
      <th>41368</th>
      <td>TEST_41369.jpg</td>
      <td>DEFFENSE</td>
    </tr>
    <tr>
      <th>41369</th>
      <td>TEST_41370.jpg</td>
      <td>MELAB</td>
    </tr>
  </tbody>
</table>
<p>41370 rows × 2 columns</p>
</div>



# DATA SET 5

VOLCANO ERUPTION

CONTENT: ACTIVE VOLCANIC ERUPTION


```python
data5
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
      <th>Number</th>
      <th>Name</th>
      <th>Country</th>
      <th>Region</th>
      <th>Type</th>
      <th>Activity Evidence</th>
      <th>Last Known Eruption</th>
      <th>Latitude</th>
      <th>Longitude</th>
      <th>Elevation (Meters)</th>
      <th>Dominant Rock Type</th>
      <th>Tectonic Setting</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>210010</td>
      <td>West Eifel Volcanic Field</td>
      <td>Germany</td>
      <td>Mediterranean and Western Asia</td>
      <td>Maar(s)</td>
      <td>Eruption Dated</td>
      <td>8300 BCE</td>
      <td>50.170</td>
      <td>6.850</td>
      <td>600</td>
      <td>Foidite</td>
      <td>Rift Zone / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>1</th>
      <td>210020</td>
      <td>Chaine des Puys</td>
      <td>France</td>
      <td>Mediterranean and Western Asia</td>
      <td>Lava dome(s)</td>
      <td>Eruption Dated</td>
      <td>4040 BCE</td>
      <td>45.775</td>
      <td>2.970</td>
      <td>1464</td>
      <td>Basalt / Picro-Basalt</td>
      <td>Rift Zone / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>2</th>
      <td>210030</td>
      <td>Olot Volcanic Field</td>
      <td>Spain</td>
      <td>Mediterranean and Western Asia</td>
      <td>Pyroclastic cone(s)</td>
      <td>Evidence Credible</td>
      <td>Unknown</td>
      <td>42.170</td>
      <td>2.530</td>
      <td>893</td>
      <td>Trachybasalt / Tephrite Basanite</td>
      <td>Intraplate / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>3</th>
      <td>210040</td>
      <td>Calatrava Volcanic Field</td>
      <td>Spain</td>
      <td>Mediterranean and Western Asia</td>
      <td>Pyroclastic cone(s)</td>
      <td>Eruption Dated</td>
      <td>3600 BCE</td>
      <td>38.870</td>
      <td>-4.020</td>
      <td>1117</td>
      <td>Basalt / Picro-Basalt</td>
      <td>Intraplate / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>4</th>
      <td>211001</td>
      <td>Larderello</td>
      <td>Italy</td>
      <td>Mediterranean and Western Asia</td>
      <td>Explosion crater(s)</td>
      <td>Eruption Observed</td>
      <td>1282 CE</td>
      <td>43.250</td>
      <td>10.870</td>
      <td>500</td>
      <td>No Data</td>
      <td>Subduction Zone / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>1503</th>
      <td>390130</td>
      <td>Zavodovski</td>
      <td>United Kingdom</td>
      <td>Antarctica</td>
      <td>Stratovolcano</td>
      <td>Eruption Observed</td>
      <td>2016 CE</td>
      <td>-56.300</td>
      <td>-27.570</td>
      <td>551</td>
      <td>Basalt / Picro-Basalt</td>
      <td>Subduction Zone / Oceanic Crust (&lt; 15 km)</td>
    </tr>
    <tr>
      <th>1504</th>
      <td>390140</td>
      <td>Protector Seamounts</td>
      <td>United Kingdom</td>
      <td>Antarctica</td>
      <td>Submarine</td>
      <td>Eruption Observed</td>
      <td>1962 CE</td>
      <td>-55.912</td>
      <td>-28.167</td>
      <td>-55</td>
      <td>Rhyolite</td>
      <td>Subduction Zone / Oceanic Crust (&lt; 15 km)</td>
    </tr>
    <tr>
      <th>1505</th>
      <td>390812</td>
      <td>Rittmann, Mount</td>
      <td>Antarctica</td>
      <td>Antarctica</td>
      <td>Shield</td>
      <td>Unrest / Pleistocene</td>
      <td>Unknown</td>
      <td>-73.450</td>
      <td>165.500</td>
      <td>2600</td>
      <td>NaN</td>
      <td>Intraplate / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>1506</th>
      <td>390829</td>
      <td>James Ross Island</td>
      <td>Antarctica</td>
      <td>Antarctica</td>
      <td>Shield</td>
      <td>Evidence Credible</td>
      <td>Unknown</td>
      <td>-64.150</td>
      <td>-57.750</td>
      <td>1630</td>
      <td>Basalt / Picro-Basalt</td>
      <td>Intraplate / Continental Crust (&gt;25 km)</td>
    </tr>
    <tr>
      <th>1507</th>
      <td>390847</td>
      <td>Melville</td>
      <td>Antarctica</td>
      <td>Antarctica</td>
      <td>Stratovolcano</td>
      <td>Evidence Uncertain</td>
      <td>Unknown</td>
      <td>-62.020</td>
      <td>-57.670</td>
      <td>549</td>
      <td>NaN</td>
      <td>Intraplate / Continental Crust (&gt;25 km)</td>
    </tr>
  </tbody>
</table>
<p>1508 rows × 12 columns</p>
</div>




```python

```
