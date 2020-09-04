```python
import pandas as pd
a = pd.read_csv("C:/Users/zaina/Desktop/MachineLearning/Week2/ProgrammingAssignment1\country_wise_latest.csv")
print(a)
```

             Country/Region  Confirmed  Deaths  Recovered  Active  New cases  \
    0           Afghanistan      36263    1269      25198    9796        106   
    1               Albania       4880     144       2745    1991        117   
    2               Algeria      27973    1163      18837    7973        616   
    3               Andorra        907      52        803      52         10   
    4                Angola        950      41        242     667         18   
    ..                  ...        ...     ...        ...     ...        ...   
    182  West Bank and Gaza      10621      78       3752    6791        152   
    183      Western Sahara         10       1          8       1          0   
    184               Yemen       1691     483        833     375         10   
    185              Zambia       4552     140       2815    1597         71   
    186            Zimbabwe       2704      36        542    2126        192   
    
         New deaths  New recovered  Deaths / 100 Cases  Recovered / 100 Cases  \
    0            10             18                3.50                  69.49   
    1             6             63                2.95                  56.25   
    2             8            749                4.16                  67.34   
    3             0              0                5.73                  88.53   
    4             1              0                4.32                  25.47   
    ..          ...            ...                 ...                    ...   
    182           2              0                0.73                  35.33   
    183           0              0               10.00                  80.00   
    184           4             36               28.56                  49.26   
    185           1            465                3.08                  61.84   
    186           2             24                1.33                  20.04   
    
         Deaths / 100 Recovered  Confirmed last week  1 week change  \
    0                      5.04                35526            737   
    1                      5.25                 4171            709   
    2                      6.17                23691           4282   
    3                      6.48                  884             23   
    4                     16.94                  749            201   
    ..                      ...                  ...            ...   
    182                    2.08                 8916           1705   
    183                   12.50                   10              0   
    184                   57.98                 1619             72   
    185                    4.97                 3326           1226   
    186                    6.64                 1713            991   
    
         1 week % increase             WHO Region  
    0                 2.07  Eastern Mediterranean  
    1                17.00                 Europe  
    2                18.07                 Africa  
    3                 2.60                 Europe  
    4                26.84                 Africa  
    ..                 ...                    ...  
    182              19.12  Eastern Mediterranean  
    183               0.00                 Africa  
    184               4.45  Eastern Mediterranean  
    185              36.86                 Africa  
    186              57.85                 Africa  
    
    [187 rows x 15 columns]
    


```python
import pandas as pd
b = pd.read_csv("C:/Users/zaina/Desktop/MachineLearning/Week2/ProgrammingAssignment1/covid_19_clean_complete.csv")
print(b)
```

          Province/State         Country/Region        Lat       Long        Date  \
    0                NaN            Afghanistan  33.939110  67.709953  2020-01-22   
    1                NaN                Albania  41.153300  20.168300  2020-01-22   
    2                NaN                Algeria  28.033900   1.659600  2020-01-22   
    3                NaN                Andorra  42.506300   1.521800  2020-01-22   
    4                NaN                 Angola -11.202700  17.873900  2020-01-22   
    ...              ...                    ...        ...        ...         ...   
    49063            NaN  Sao Tome and Principe   0.186400   6.613100  2020-07-27   
    49064            NaN                  Yemen  15.552727  48.516388  2020-07-27   
    49065            NaN                Comoros -11.645500  43.333300  2020-07-27   
    49066            NaN             Tajikistan  38.861000  71.276100  2020-07-27   
    49067            NaN                Lesotho -29.610000  28.233600  2020-07-27   
    
           Confirmed  Deaths  Recovered  Active             WHO Region  
    0              0       0          0       0  Eastern Mediterranean  
    1              0       0          0       0                 Europe  
    2              0       0          0       0                 Africa  
    3              0       0          0       0                 Europe  
    4              0       0          0       0                 Africa  
    ...          ...     ...        ...     ...                    ...  
    49063        865      14        734     117                 Africa  
    49064       1691     483        833     375  Eastern Mediterranean  
    49065        354       7        328      19                 Africa  
    49066       7235      60       6028    1147                 Europe  
    49067        505      12        128     365                 Africa  
    
    [49068 rows x 10 columns]
    


```python
import pandas as pd
c = pd.read_csv("C:/Users/zaina/Desktop/MachineLearning/Week2/ProgrammingAssignment1/day_wise.csv")
print(c)
```

               Date  Confirmed  Deaths  Recovered   Active  New cases  New deaths  \
    0    2020-01-22        555      17         28      510          0           0   
    1    2020-01-23        654      18         30      606         99           1   
    2    2020-01-24        941      26         36      879        287           8   
    3    2020-01-25       1434      42         39     1353        493          16   
    4    2020-01-26       2118      56         52     2010        684          14   
    ..          ...        ...     ...        ...      ...        ...         ...   
    183  2020-07-23   15510481  633506    8710969  6166006     282756        9966   
    184  2020-07-24   15791645  639650    8939705  6212290     281164        6144   
    185  2020-07-25   16047190  644517    9158743  6243930     255545        4867   
    186  2020-07-26   16251796  648621    9293464  6309711     204606        4104   
    187  2020-07-27   16480485  654036    9468087  6358362     228693        5415   
    
         New recovered  Deaths / 100 Cases  Recovered / 100 Cases  \
    0                0                3.06                   5.05   
    1                2                2.75                   4.59   
    2                6                2.76                   3.83   
    3                3                2.93                   2.72   
    4               13                2.64                   2.46   
    ..             ...                 ...                    ...   
    183         169714                4.08                  56.16   
    184         228736                4.05                  56.61   
    185         219038                4.02                  57.07   
    186         134721                3.99                  57.18   
    187         174623                3.97                  57.45   
    
         Deaths / 100 Recovered  No. of countries  
    0                     60.71                 6  
    1                     60.00                 8  
    2                     72.22                 9  
    3                    107.69                11  
    4                    107.69                13  
    ..                      ...               ...  
    183                    7.27               187  
    184                    7.16               187  
    185                    7.04               187  
    186                    6.98               187  
    187                    6.91               187  
    
    [188 rows x 12 columns]
    


```python
import pandas as pd
d = pd.read_csv("C:/Users/zaina/Desktop/MachineLearning/Week2/ProgrammingAssignment1/WorldPopulationByAge2020.csv")
print(d)
```

             Location AgeGrp   PopMale  PopFemale  PopTotal
    0     Afghanistan   0-19   10709.0    10197.0   20906.0
    1     Afghanistan  20-39    5994.0     5574.0   11568.0
    2     Afghanistan  40-59    2485.0     2316.0    4801.0
    3     Afghanistan    60+     781.0      858.0    1639.0
    4          Africa   0-19  344109.0   334982.0  679091.0
    ...           ...    ...       ...        ...       ...
    1755       Zambia    60+     258.0      365.0     623.0
    1756     Zimbabwe   0-19    3941.0     3923.0    7864.0
    1757     Zimbabwe  20-39    1993.0     2354.0    4347.0
    1758     Zimbabwe  40-59     892.0     1060.0    1952.0
    1759     Zimbabwe    60+     257.0      424.0     681.0
    
    [1760 rows x 5 columns]
    


```python
import pandas as pd
e = pd.read_csv("C:/Users/zaina/Desktop/MachineLearning/Week2/ProgrammingAssignment1/usa_county_wise.csv")
print(e)

```

                 UID iso2 iso3  code3     FIPS          Admin2  \
    0             16   AS  ASM     16     60.0             NaN   
    1            316   GU  GUM    316     66.0             NaN   
    2            580   MP  MNP    580     69.0             NaN   
    3       63072001   PR  PRI    630  72001.0        Adjuntas   
    4       63072003   PR  PRI    630  72003.0          Aguada   
    ...          ...  ...  ...    ...      ...             ...   
    627915  84070016   US  USA    840      NaN    Central Utah   
    627916  84070017   US  USA    840      NaN  Southeast Utah   
    627917  84070018   US  USA    840      NaN  Southwest Utah   
    627918  84070019   US  USA    840      NaN       TriCounty   
    627919  84070020   US  USA    840      NaN    Weber-Morgan   
    
                      Province_State Country_Region        Lat       Long_  \
    0                 American Samoa             US -14.271000 -170.132000   
    1                           Guam             US  13.444300  144.793700   
    2       Northern Mariana Islands             US  15.097900  145.673900   
    3                    Puerto Rico             US  18.180117  -66.754367   
    4                    Puerto Rico             US  18.360255  -67.175131   
    ...                          ...            ...        ...         ...   
    627915                      Utah             US  39.372319 -111.575868   
    627916                      Utah             US  38.996171 -110.701396   
    627917                      Utah             US  37.854472 -111.441876   
    627918                      Utah             US  40.124915 -109.517442   
    627919                      Utah             US  41.271160 -111.914512   
    
                            Combined_Key     Date  Confirmed  Deaths  
    0                 American Samoa, US  1/22/20          0       0  
    1                           Guam, US  1/22/20          0       0  
    2       Northern Mariana Islands, US  1/22/20          0       0  
    3          Adjuntas, Puerto Rico, US  1/22/20          0       0  
    4            Aguada, Puerto Rico, US  1/22/20          0       0  
    ...                              ...      ...        ...     ...  
    627915        Central Utah, Utah, US  7/27/20        347       1  
    627916      Southeast Utah, Utah, US  7/27/20         70       0  
    627917      Southwest Utah, Utah, US  7/27/20       2781      23  
    627918           TriCounty, Utah, US  7/27/20        142       0  
    627919        Weber-Morgan, Utah, US  7/27/20       2375      24  
    
    [627920 rows x 14 columns]
    


```python

```
