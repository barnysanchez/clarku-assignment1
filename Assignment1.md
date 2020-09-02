```python
import pandas as pd
```

# 1
NAME OF THE DATASET: COVID19 TWEETS
DOWNLOAD LOCATION: KAGGLE
PURPOSE: We can dive into the subjects that use this hashtag on tweeter, look into their geographical distribution, evaluate sentiments.


```python
data_covid=pd.read_csv(r"C:\Users\vinit\OneDrive\Desktop\ML\Assignment1\covid19_tweets.csv")
data_covid.tail()
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
      <th>user_name</th>
      <th>user_location</th>
      <th>user_description</th>
      <th>user_created</th>
      <th>user_followers</th>
      <th>user_friends</th>
      <th>user_favourites</th>
      <th>user_verified</th>
      <th>date</th>
      <th>text</th>
      <th>hashtags</th>
      <th>source</th>
      <th>is_retweet</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>179103</th>
      <td>AJIMATI AbdulRahman O.</td>
      <td>Ilorin, Nigeria</td>
      <td>Animal Scientist|| Muslim|| Real Madrid/Chelsea</td>
      <td>2013-12-30 18:59:19</td>
      <td>412</td>
      <td>1609</td>
      <td>1062</td>
      <td>False</td>
      <td>2020-08-29 19:44:21</td>
      <td>Thanks @IamOhmai for nominating me for the @WH...</td>
      <td>['WearAMask']</td>
      <td>Twitter for Android</td>
      <td>False</td>
    </tr>
    <tr>
      <th>179104</th>
      <td>Jason</td>
      <td>Ontario</td>
      <td>When your cat has more baking soda than Ninja ...</td>
      <td>2011-12-21 04:41:30</td>
      <td>150</td>
      <td>182</td>
      <td>7295</td>
      <td>False</td>
      <td>2020-08-29 19:44:16</td>
      <td>2020! The year of insanity! Lol! #COVID19 http...</td>
      <td>['COVID19']</td>
      <td>Twitter for Android</td>
      <td>False</td>
    </tr>
    <tr>
      <th>179105</th>
      <td>BEEHEMOTH ⏳</td>
      <td>🇨🇦 Canada</td>
      <td>⚒️ The Architects of Free Trade ⚒️ Really Did ...</td>
      <td>2016-07-13 17:21:59</td>
      <td>1623</td>
      <td>2160</td>
      <td>98000</td>
      <td>False</td>
      <td>2020-08-29 19:44:15</td>
      <td>@CTVNews A powerful painting by Juan Lucena. I...</td>
      <td>NaN</td>
      <td>Twitter Web App</td>
      <td>False</td>
    </tr>
    <tr>
      <th>179106</th>
      <td>Gary DelPonte</td>
      <td>New York City</td>
      <td>Global UX UI Visual Designer. StoryTeller, Mus...</td>
      <td>2009-10-27 17:43:13</td>
      <td>1338</td>
      <td>1111</td>
      <td>0</td>
      <td>False</td>
      <td>2020-08-29 19:44:14</td>
      <td>More than 1,200 students test positive for #CO...</td>
      <td>['COVID19']</td>
      <td>Twitter for iPhone</td>
      <td>False</td>
    </tr>
    <tr>
      <th>179107</th>
      <td>TUKY II</td>
      <td>Aliwal North, South Africa</td>
      <td>TOKELO SEKHOPA | TUKY II | LAST BORN | EISH TU...</td>
      <td>2018-04-14 17:30:07</td>
      <td>97</td>
      <td>1697</td>
      <td>566</td>
      <td>False</td>
      <td>2020-08-29 19:44:08</td>
      <td>I stop when I see a Stop\n\n@SABCNews\n@Izinda...</td>
      <td>NaN</td>
      <td>Twitter for Android</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
data_covid.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 179108 entries, 0 to 179107
    Data columns (total 13 columns):
     #   Column            Non-Null Count   Dtype 
    ---  ------            --------------   ----- 
     0   user_name         179108 non-null  object
     1   user_location     142337 non-null  object
     2   user_description  168822 non-null  object
     3   user_created      179108 non-null  object
     4   user_followers    179108 non-null  int64 
     5   user_friends      179108 non-null  int64 
     6   user_favourites   179108 non-null  int64 
     7   user_verified     179108 non-null  bool  
     8   date              179108 non-null  object
     9   text              179108 non-null  object
     10  hashtags          127774 non-null  object
     11  source            179031 non-null  object
     12  is_retweet        179108 non-null  bool  
    dtypes: bool(2), int64(3), object(8)
    memory usage: 15.4+ MB
    

# 2
NAME OF THE DATASET: NETFLIX MOVIES AND TV SHOWS
DOWNLOAD LOCATION: KAGGLE
PURPOSE: Understanding the content in different countries, network analysis of Actors/Directors, focus on movies or TV shows in recent years.


```python
data_netflix=pd.read_csv(r"C:\Users\vinit\OneDrive\Desktop\ML\Assignment1\netflix_titles.csv")
data_netflix.head()
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
      <th>show_id</th>
      <th>type</th>
      <th>title</th>
      <th>director</th>
      <th>cast</th>
      <th>country</th>
      <th>date_added</th>
      <th>release_year</th>
      <th>rating</th>
      <th>duration</th>
      <th>listed_in</th>
      <th>description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>81145628</td>
      <td>Movie</td>
      <td>Norm of the North: King Sized Adventure</td>
      <td>Richard Finn, Tim Maltby</td>
      <td>Alan Marriott, Andrew Toth, Brian Dobson, Cole...</td>
      <td>United States, India, South Korea, China</td>
      <td>September 9, 2019</td>
      <td>2019</td>
      <td>TV-PG</td>
      <td>90 min</td>
      <td>Children &amp; Family Movies, Comedies</td>
      <td>Before planning an awesome wedding for his gra...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>80117401</td>
      <td>Movie</td>
      <td>Jandino: Whatever it Takes</td>
      <td>NaN</td>
      <td>Jandino Asporaat</td>
      <td>United Kingdom</td>
      <td>September 9, 2016</td>
      <td>2016</td>
      <td>TV-MA</td>
      <td>94 min</td>
      <td>Stand-Up Comedy</td>
      <td>Jandino Asporaat riffs on the challenges of ra...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>70234439</td>
      <td>TV Show</td>
      <td>Transformers Prime</td>
      <td>NaN</td>
      <td>Peter Cullen, Sumalee Montano, Frank Welker, J...</td>
      <td>United States</td>
      <td>September 8, 2018</td>
      <td>2013</td>
      <td>TV-Y7-FV</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>With the help of three human allies, the Autob...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>80058654</td>
      <td>TV Show</td>
      <td>Transformers: Robots in Disguise</td>
      <td>NaN</td>
      <td>Will Friedle, Darren Criss, Constance Zimmer, ...</td>
      <td>United States</td>
      <td>September 8, 2018</td>
      <td>2016</td>
      <td>TV-Y7</td>
      <td>1 Season</td>
      <td>Kids' TV</td>
      <td>When a prison ship crash unleashes hundreds of...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>80125979</td>
      <td>Movie</td>
      <td>#realityhigh</td>
      <td>Fernando Lebrija</td>
      <td>Nesta Cooper, Kate Walsh, John Michael Higgins...</td>
      <td>United States</td>
      <td>September 8, 2017</td>
      <td>2017</td>
      <td>TV-14</td>
      <td>99 min</td>
      <td>Comedies</td>
      <td>When nerdy high schooler Dani finally attracts...</td>
    </tr>
  </tbody>
</table>
</div>




```python
data_netflix.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 6234 entries, 0 to 6233
    Data columns (total 12 columns):
     #   Column        Non-Null Count  Dtype 
    ---  ------        --------------  ----- 
     0   show_id       6234 non-null   int64 
     1   type          6234 non-null   object
     2   title         6234 non-null   object
     3   director      4265 non-null   object
     4   cast          5664 non-null   object
     5   country       5758 non-null   object
     6   date_added    6223 non-null   object
     7   release_year  6234 non-null   int64 
     8   rating        6224 non-null   object
     9   duration      6234 non-null   object
     10  listed_in     6234 non-null   object
     11  description   6234 non-null   object
    dtypes: int64(2), object(10)
    memory usage: 584.6+ KB
    

# 3
NAME OF THE DATASET: FIFA 2019 PLAYER DATASET
DOWNLOAD LOCATION: KAGGLE
PURPOSE: detailed attributes for every player who was registered in the latest edition of FIFA 19 database.


```python
data_fifa=pd.read_csv(r"C:\Users\vinit\OneDrive\Desktop\ML\Assignment1\fifa19_dataset.csv")
data_fifa.head()
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
      <th>ID</th>
      <th>Name</th>
      <th>Age</th>
      <th>Photo</th>
      <th>Nationality</th>
      <th>Flag</th>
      <th>Overall</th>
      <th>Potential</th>
      <th>Club</th>
      <th>...</th>
      <th>Composure</th>
      <th>Marking</th>
      <th>StandingTackle</th>
      <th>SlidingTackle</th>
      <th>GKDiving</th>
      <th>GKHandling</th>
      <th>GKKicking</th>
      <th>GKPositioning</th>
      <th>GKReflexes</th>
      <th>Release Clause</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>158023</td>
      <td>L. Messi</td>
      <td>31</td>
      <td>https://cdn.sofifa.org/players/4/19/158023.png</td>
      <td>Argentina</td>
      <td>https://cdn.sofifa.org/flags/52.png</td>
      <td>94</td>
      <td>94</td>
      <td>FC Barcelona</td>
      <td>...</td>
      <td>96.0</td>
      <td>33.0</td>
      <td>28.0</td>
      <td>26.0</td>
      <td>6.0</td>
      <td>11.0</td>
      <td>15.0</td>
      <td>14.0</td>
      <td>8.0</td>
      <td>€226.5M</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>20801</td>
      <td>Cristiano Ronaldo</td>
      <td>33</td>
      <td>https://cdn.sofifa.org/players/4/19/20801.png</td>
      <td>Portugal</td>
      <td>https://cdn.sofifa.org/flags/38.png</td>
      <td>94</td>
      <td>94</td>
      <td>Juventus</td>
      <td>...</td>
      <td>95.0</td>
      <td>28.0</td>
      <td>31.0</td>
      <td>23.0</td>
      <td>7.0</td>
      <td>11.0</td>
      <td>15.0</td>
      <td>14.0</td>
      <td>11.0</td>
      <td>€127.1M</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>190871</td>
      <td>Neymar Jr</td>
      <td>26</td>
      <td>https://cdn.sofifa.org/players/4/19/190871.png</td>
      <td>Brazil</td>
      <td>https://cdn.sofifa.org/flags/54.png</td>
      <td>92</td>
      <td>93</td>
      <td>Paris Saint-Germain</td>
      <td>...</td>
      <td>94.0</td>
      <td>27.0</td>
      <td>24.0</td>
      <td>33.0</td>
      <td>9.0</td>
      <td>9.0</td>
      <td>15.0</td>
      <td>15.0</td>
      <td>11.0</td>
      <td>€228.1M</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>193080</td>
      <td>De Gea</td>
      <td>27</td>
      <td>https://cdn.sofifa.org/players/4/19/193080.png</td>
      <td>Spain</td>
      <td>https://cdn.sofifa.org/flags/45.png</td>
      <td>91</td>
      <td>93</td>
      <td>Manchester United</td>
      <td>...</td>
      <td>68.0</td>
      <td>15.0</td>
      <td>21.0</td>
      <td>13.0</td>
      <td>90.0</td>
      <td>85.0</td>
      <td>87.0</td>
      <td>88.0</td>
      <td>94.0</td>
      <td>€138.6M</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>192985</td>
      <td>K. De Bruyne</td>
      <td>27</td>
      <td>https://cdn.sofifa.org/players/4/19/192985.png</td>
      <td>Belgium</td>
      <td>https://cdn.sofifa.org/flags/7.png</td>
      <td>91</td>
      <td>92</td>
      <td>Manchester City</td>
      <td>...</td>
      <td>88.0</td>
      <td>68.0</td>
      <td>58.0</td>
      <td>51.0</td>
      <td>15.0</td>
      <td>13.0</td>
      <td>5.0</td>
      <td>10.0</td>
      <td>13.0</td>
      <td>€196.4M</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 89 columns</p>
</div>




```python
data_fifa.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 18207 entries, 0 to 18206
    Data columns (total 89 columns):
     #   Column                    Non-Null Count  Dtype  
    ---  ------                    --------------  -----  
     0   Unnamed: 0                18207 non-null  int64  
     1   ID                        18207 non-null  int64  
     2   Name                      18207 non-null  object 
     3   Age                       18207 non-null  int64  
     4   Photo                     18207 non-null  object 
     5   Nationality               18207 non-null  object 
     6   Flag                      18207 non-null  object 
     7   Overall                   18207 non-null  int64  
     8   Potential                 18207 non-null  int64  
     9   Club                      17966 non-null  object 
     10  Club Logo                 18207 non-null  object 
     11  Value                     18207 non-null  object 
     12  Wage                      18207 non-null  object 
     13  Special                   18207 non-null  int64  
     14  Preferred Foot            18159 non-null  object 
     15  International Reputation  18159 non-null  float64
     16  Weak Foot                 18159 non-null  float64
     17  Skill Moves               18159 non-null  float64
     18  Work Rate                 18159 non-null  object 
     19  Body Type                 18159 non-null  object 
     20  Real Face                 18159 non-null  object 
     21  Position                  18147 non-null  object 
     22  Jersey Number             18147 non-null  float64
     23  Joined                    16654 non-null  object 
     24  Loaned From               1264 non-null   object 
     25  Contract Valid Until      17918 non-null  object 
     26  Height                    18159 non-null  object 
     27  Weight                    18159 non-null  object 
     28  LS                        16122 non-null  object 
     29  ST                        16122 non-null  object 
     30  RS                        16122 non-null  object 
     31  LW                        16122 non-null  object 
     32  LF                        16122 non-null  object 
     33  CF                        16122 non-null  object 
     34  RF                        16122 non-null  object 
     35  RW                        16122 non-null  object 
     36  LAM                       16122 non-null  object 
     37  CAM                       16122 non-null  object 
     38  RAM                       16122 non-null  object 
     39  LM                        16122 non-null  object 
     40  LCM                       16122 non-null  object 
     41  CM                        16122 non-null  object 
     42  RCM                       16122 non-null  object 
     43  RM                        16122 non-null  object 
     44  LWB                       16122 non-null  object 
     45  LDM                       16122 non-null  object 
     46  CDM                       16122 non-null  object 
     47  RDM                       16122 non-null  object 
     48  RWB                       16122 non-null  object 
     49  LB                        16122 non-null  object 
     50  LCB                       16122 non-null  object 
     51  CB                        16122 non-null  object 
     52  RCB                       16122 non-null  object 
     53  RB                        16122 non-null  object 
     54  Crossing                  18159 non-null  float64
     55  Finishing                 18159 non-null  float64
     56  HeadingAccuracy           18159 non-null  float64
     57  ShortPassing              18159 non-null  float64
     58  Volleys                   18159 non-null  float64
     59  Dribbling                 18159 non-null  float64
     60  Curve                     18159 non-null  float64
     61  FKAccuracy                18159 non-null  float64
     62  LongPassing               18159 non-null  float64
     63  BallControl               18159 non-null  float64
     64  Acceleration              18159 non-null  float64
     65  SprintSpeed               18159 non-null  float64
     66  Agility                   18159 non-null  float64
     67  Reactions                 18159 non-null  float64
     68  Balance                   18159 non-null  float64
     69  ShotPower                 18159 non-null  float64
     70  Jumping                   18159 non-null  float64
     71  Stamina                   18159 non-null  float64
     72  Strength                  18159 non-null  float64
     73  LongShots                 18159 non-null  float64
     74  Aggression                18159 non-null  float64
     75  Interceptions             18159 non-null  float64
     76  Positioning               18159 non-null  float64
     77  Vision                    18159 non-null  float64
     78  Penalties                 18159 non-null  float64
     79  Composure                 18159 non-null  float64
     80  Marking                   18159 non-null  float64
     81  StandingTackle            18159 non-null  float64
     82  SlidingTackle             18159 non-null  float64
     83  GKDiving                  18159 non-null  float64
     84  GKHandling                18159 non-null  float64
     85  GKKicking                 18159 non-null  float64
     86  GKPositioning             18159 non-null  float64
     87  GKReflexes                18159 non-null  float64
     88  Release Clause            16643 non-null  object 
    dtypes: float64(38), int64(6), object(45)
    memory usage: 12.4+ MB
    

# 4
NAME OF THE DATASET: DATA POLICE SHOOTINGS
DOWNLOAD LOCATION: KAGGLE
PURPOSE: The dataset documented more than two times more fatal shootings by police than that recorded by FBI.


```python
data_police=pd.read_csv(r"C:\Users\vinit\OneDrive\Desktop\ML\Assignment1\fatal_police_shooting.csv")
data_police.head()
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
      <th>id</th>
      <th>name</th>
      <th>date</th>
      <th>manner_of_death</th>
      <th>armed</th>
      <th>age</th>
      <th>gender</th>
      <th>race</th>
      <th>city</th>
      <th>state</th>
      <th>signs_of_mental_illness</th>
      <th>threat_level</th>
      <th>flee</th>
      <th>body_camera</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3</td>
      <td>Tim Elliot</td>
      <td>2015-01-02</td>
      <td>shot</td>
      <td>gun</td>
      <td>53.0</td>
      <td>M</td>
      <td>A</td>
      <td>Shelton</td>
      <td>WA</td>
      <td>True</td>
      <td>attack</td>
      <td>Not fleeing</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4</td>
      <td>Lewis Lee Lembke</td>
      <td>2015-01-02</td>
      <td>shot</td>
      <td>gun</td>
      <td>47.0</td>
      <td>M</td>
      <td>W</td>
      <td>Aloha</td>
      <td>OR</td>
      <td>False</td>
      <td>attack</td>
      <td>Not fleeing</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5</td>
      <td>John Paul Quintero</td>
      <td>2015-01-03</td>
      <td>shot and Tasered</td>
      <td>unarmed</td>
      <td>23.0</td>
      <td>M</td>
      <td>H</td>
      <td>Wichita</td>
      <td>KS</td>
      <td>False</td>
      <td>other</td>
      <td>Not fleeing</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>8</td>
      <td>Matthew Hoffman</td>
      <td>2015-01-04</td>
      <td>shot</td>
      <td>toy weapon</td>
      <td>32.0</td>
      <td>M</td>
      <td>W</td>
      <td>San Francisco</td>
      <td>CA</td>
      <td>True</td>
      <td>attack</td>
      <td>Not fleeing</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>9</td>
      <td>Michael Rodriguez</td>
      <td>2015-01-04</td>
      <td>shot</td>
      <td>nail gun</td>
      <td>39.0</td>
      <td>M</td>
      <td>H</td>
      <td>Evans</td>
      <td>CO</td>
      <td>False</td>
      <td>attack</td>
      <td>Not fleeing</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
</div>




```python
data_police.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 5416 entries, 0 to 5415
    Data columns (total 14 columns):
     #   Column                   Non-Null Count  Dtype  
    ---  ------                   --------------  -----  
     0   id                       5416 non-null   int64  
     1   name                     5416 non-null   object 
     2   date                     5416 non-null   object 
     3   manner_of_death          5416 non-null   object 
     4   armed                    5189 non-null   object 
     5   age                      5181 non-null   float64
     6   gender                   5414 non-null   object 
     7   race                     4895 non-null   object 
     8   city                     5416 non-null   object 
     9   state                    5416 non-null   object 
     10  signs_of_mental_illness  5416 non-null   bool   
     11  threat_level             5416 non-null   object 
     12  flee                     5167 non-null   object 
     13  body_camera              5416 non-null   bool   
    dtypes: bool(2), float64(1), int64(1), object(10)
    memory usage: 518.5+ KB
    

# 5
NAME OF THE DATASET: TITANIC DATASET
DOWNLOAD LOCATION: KAGGLE
PURPOSE: This is the dataset which most interests me as the training set can be used to build machine learning models. In this set, the outcome for each passenger is provided.  


```python
data=pd.read_csv(r"C:\Users\vinit\OneDrive\Desktop\MLAssignments\titanic\train.csv")
data.head()
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
      <th>PassengerId</th>
      <th>Survived</th>
      <th>Pclass</th>
      <th>Name</th>
      <th>Sex</th>
      <th>Age</th>
      <th>SibSp</th>
      <th>Parch</th>
      <th>Ticket</th>
      <th>Fare</th>
      <th>Cabin</th>
      <th>Embarked</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>Braund, Mr. Owen Harris</td>
      <td>male</td>
      <td>22.0</td>
      <td>1</td>
      <td>0</td>
      <td>A/5 21171</td>
      <td>7.2500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>Cumings, Mrs. John Bradley (Florence Briggs Th...</td>
      <td>female</td>
      <td>38.0</td>
      <td>1</td>
      <td>0</td>
      <td>PC 17599</td>
      <td>71.2833</td>
      <td>C85</td>
      <td>C</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Heikkinen, Miss. Laina</td>
      <td>female</td>
      <td>26.0</td>
      <td>0</td>
      <td>0</td>
      <td>STON/O2. 3101282</td>
      <td>7.9250</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>1</td>
      <td>1</td>
      <td>Futrelle, Mrs. Jacques Heath (Lily May Peel)</td>
      <td>female</td>
      <td>35.0</td>
      <td>1</td>
      <td>0</td>
      <td>113803</td>
      <td>53.1000</td>
      <td>C123</td>
      <td>S</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>0</td>
      <td>3</td>
      <td>Allen, Mr. William Henry</td>
      <td>male</td>
      <td>35.0</td>
      <td>0</td>
      <td>0</td>
      <td>373450</td>
      <td>8.0500</td>
      <td>NaN</td>
      <td>S</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 891 entries, 0 to 890
    Data columns (total 12 columns):
     #   Column       Non-Null Count  Dtype  
    ---  ------       --------------  -----  
     0   PassengerId  891 non-null    int64  
     1   Survived     891 non-null    int64  
     2   Pclass       891 non-null    int64  
     3   Name         891 non-null    object 
     4   Sex          891 non-null    object 
     5   Age          714 non-null    float64
     6   SibSp        891 non-null    int64  
     7   Parch        891 non-null    int64  
     8   Ticket       891 non-null    object 
     9   Fare         891 non-null    float64
     10  Cabin        204 non-null    object 
     11  Embarked     889 non-null    object 
    dtypes: float64(2), int64(5), object(5)
    memory usage: 83.7+ KB
    


