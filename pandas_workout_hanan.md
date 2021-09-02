# Publicly available datasets



# Dataset 1:

- Link: https://www.kaggle.com/emilynallen/top-20-songs-1970s2000s-w-audio-features?select=Top+20+All+Decades.csv 
- Purpose: I would use this dataset of to find top 5 songs that where listen to during the time frame from 70s-80s

# Dataset 2:

- Link: https://www.kaggle.com/stefanoleone992/imdb-extensive-dataset
- Purpose: I would use this dataset of movies to find the a list of Crime movies made in the US.

# Dataset 3:

- Link: https://www.kaggle.com/zynicide/wine-reviews?select=winemag-data-130k-v2.csv 
- Purpose: I would use this data set to find the List of wines that are made in france.

# Dataset 4:

- Link:https://www.kaggle.com/uciml/iris?select=Iris.csv
- Purpose: I would use this dataset to find out which species of the iris have the largest Petal length.

# Dataset 5:

- Link: https://www.kaggle.com/imls/museum-directory?select=museums.csv 
- Purpose: I would use this dataset to find out what type of museums are most frequent in the United States.



```python
import pandas as pd
```

# Dataset information 

## Dataset 1 : Top 20 songs from 1970s - 2000s


```python
dataset1 = pd.read_csv("top_20_music.csv")
```


```python

dataset1.head()
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
      <th>Name</th>
      <th>Artist</th>
      <th>Decade</th>
      <th>Rank</th>
      <th>danceability</th>
      <th>energy</th>
      <th>key</th>
      <th>loudness</th>
      <th>speechiness</th>
      <th>acousticness</th>
      <th>instrumentalness</th>
      <th>liveness</th>
      <th>valence</th>
      <th>tempo</th>
      <th>duration_ms</th>
      <th>time_signature</th>
      <th>Country</th>
      <th>City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Twist</td>
      <td>Chubby Checker</td>
      <td>60</td>
      <td>1</td>
      <td>0.533</td>
      <td>0.638</td>
      <td>4</td>
      <td>-7.130</td>
      <td>0.0341</td>
      <td>0.202</td>
      <td>0.000</td>
      <td>0.0729</td>
      <td>0.937</td>
      <td>156.663</td>
      <td>153760</td>
      <td>4</td>
      <td>United States</td>
      <td>Philadelphia</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Hey Jude</td>
      <td>The Beatles</td>
      <td>60</td>
      <td>2</td>
      <td>0.462</td>
      <td>0.632</td>
      <td>5</td>
      <td>-7.438</td>
      <td>0.0248</td>
      <td>0.091</td>
      <td>0.000</td>
      <td>0.3970</td>
      <td>0.585</td>
      <td>74.268</td>
      <td>238854</td>
      <td>4</td>
      <td>England</td>
      <td>Liverpool</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Theme from “A Summer Place”</td>
      <td>Percy Faith &amp; His Orchestra</td>
      <td>60</td>
      <td>3</td>
      <td>0.466</td>
      <td>0.389</td>
      <td>5</td>
      <td>-12.825</td>
      <td>0.0253</td>
      <td>0.631</td>
      <td>0.843</td>
      <td>0.2950</td>
      <td>0.749</td>
      <td>92.631</td>
      <td>144893</td>
      <td>4</td>
      <td>Canada</td>
      <td>Toronto</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Tossin’ and Turnin’</td>
      <td>Bobby Lewis</td>
      <td>60</td>
      <td>4</td>
      <td>0.569</td>
      <td>0.722</td>
      <td>0</td>
      <td>-8.914</td>
      <td>0.0393</td>
      <td>0.255</td>
      <td>0.000</td>
      <td>0.1080</td>
      <td>0.965</td>
      <td>142.736</td>
      <td>159640</td>
      <td>4</td>
      <td>United States</td>
      <td>Indianapolis</td>
    </tr>
    <tr>
      <th>4</th>
      <td>I Want to Hold Your Hand</td>
      <td>The Beatles</td>
      <td>60</td>
      <td>5</td>
      <td>0.490</td>
      <td>0.715</td>
      <td>7</td>
      <td>-5.549</td>
      <td>0.0476</td>
      <td>0.386</td>
      <td>0.000</td>
      <td>0.3110</td>
      <td>0.866</td>
      <td>130.726</td>
      <td>145747</td>
      <td>4</td>
      <td>England</td>
      <td>Liverpool</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataset1.tail()
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
      <th>Name</th>
      <th>Artist</th>
      <th>Decade</th>
      <th>Rank</th>
      <th>danceability</th>
      <th>energy</th>
      <th>key</th>
      <th>loudness</th>
      <th>speechiness</th>
      <th>acousticness</th>
      <th>instrumentalness</th>
      <th>liveness</th>
      <th>valence</th>
      <th>tempo</th>
      <th>duration_ms</th>
      <th>time_signature</th>
      <th>Country</th>
      <th>City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>94</th>
      <td>Whatever You Like</td>
      <td>T.I.</td>
      <td>2000</td>
      <td>16</td>
      <td>0.680</td>
      <td>0.687</td>
      <td>9</td>
      <td>-6.162</td>
      <td>0.0709</td>
      <td>0.0161</td>
      <td>0.000000</td>
      <td>0.261</td>
      <td>0.467</td>
      <td>150.053</td>
      <td>249533</td>
      <td>4</td>
      <td>United States</td>
      <td>Atlanta</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Bleeding Love</td>
      <td>Leona Lewis</td>
      <td>2000</td>
      <td>17</td>
      <td>0.638</td>
      <td>0.656</td>
      <td>5</td>
      <td>-5.886</td>
      <td>0.0357</td>
      <td>0.1880</td>
      <td>0.000000</td>
      <td>0.146</td>
      <td>0.225</td>
      <td>104.036</td>
      <td>262467</td>
      <td>4</td>
      <td>United Kingdom</td>
      <td>London</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Independent Women, Part I</td>
      <td>Destiny’s Child</td>
      <td>2000</td>
      <td>18</td>
      <td>0.730</td>
      <td>0.602</td>
      <td>6</td>
      <td>-3.782</td>
      <td>0.2060</td>
      <td>0.3620</td>
      <td>0.000004</td>
      <td>0.169</td>
      <td>0.927</td>
      <td>97.954</td>
      <td>221133</td>
      <td>4</td>
      <td>United States</td>
      <td>Houston</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Foolish</td>
      <td>Ashanti</td>
      <td>2000</td>
      <td>19</td>
      <td>0.477</td>
      <td>0.728</td>
      <td>0</td>
      <td>-5.710</td>
      <td>0.0831</td>
      <td>0.3580</td>
      <td>0.000000</td>
      <td>0.110</td>
      <td>0.690</td>
      <td>89.209</td>
      <td>227387</td>
      <td>4</td>
      <td>United States</td>
      <td>Glen Cove</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Hey Ya!</td>
      <td>Outkast</td>
      <td>2000</td>
      <td>20</td>
      <td>0.715</td>
      <td>0.970</td>
      <td>0</td>
      <td>-2.206</td>
      <td>0.0648</td>
      <td>0.0644</td>
      <td>0.000156</td>
      <td>0.205</td>
      <td>0.963</td>
      <td>79.504</td>
      <td>239240</td>
      <td>4</td>
      <td>United States</td>
      <td>East Point</td>
    </tr>
  </tbody>
</table>
</div>



## Dataset 2 : IMDB Movie List


```python
import pandas as pd
```


```python
dataset2 = pd.read_csv("IMDb_movies.csv")
```


```python
dataset2.head()
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
      <th>imdb_title_id</th>
      <th>title</th>
      <th>original_title</th>
      <th>year</th>
      <th>date_published</th>
      <th>genre</th>
      <th>duration</th>
      <th>country</th>
      <th>language</th>
      <th>director</th>
      <th>...</th>
      <th>actors</th>
      <th>description</th>
      <th>avg_vote</th>
      <th>votes</th>
      <th>budget</th>
      <th>usa_gross_income</th>
      <th>worlwide_gross_income</th>
      <th>metascore</th>
      <th>reviews_from_users</th>
      <th>reviews_from_critics</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000009</td>
      <td>Miss Jerry</td>
      <td>Miss Jerry</td>
      <td>1894</td>
      <td>1894-10-09</td>
      <td>Romance</td>
      <td>45</td>
      <td>USA</td>
      <td>None</td>
      <td>Alexander Black</td>
      <td>...</td>
      <td>Blanche Bayliss, William Courtenay, Chauncey D...</td>
      <td>The adventures of a female reporter in the 1890s.</td>
      <td>5.9</td>
      <td>154</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000574</td>
      <td>The Story of the Kelly Gang</td>
      <td>The Story of the Kelly Gang</td>
      <td>1906</td>
      <td>1906-12-26</td>
      <td>Biography, Crime, Drama</td>
      <td>70</td>
      <td>Australia</td>
      <td>None</td>
      <td>Charles Tait</td>
      <td>...</td>
      <td>Elizabeth Tait, John Tait, Norman Campbell, Be...</td>
      <td>True story of notorious Australian outlaw Ned ...</td>
      <td>6.1</td>
      <td>589</td>
      <td>$ 2250</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>7.0</td>
      <td>7.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0001892</td>
      <td>Den sorte drøm</td>
      <td>Den sorte drøm</td>
      <td>1911</td>
      <td>1911-08-19</td>
      <td>Drama</td>
      <td>53</td>
      <td>Germany, Denmark</td>
      <td>NaN</td>
      <td>Urban Gad</td>
      <td>...</td>
      <td>Asta Nielsen, Valdemar Psilander, Gunnar Helse...</td>
      <td>Two men of high rank are both wooing the beaut...</td>
      <td>5.8</td>
      <td>188</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.0</td>
      <td>2.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0002101</td>
      <td>Cleopatra</td>
      <td>Cleopatra</td>
      <td>1912</td>
      <td>1912-11-13</td>
      <td>Drama, History</td>
      <td>100</td>
      <td>USA</td>
      <td>English</td>
      <td>Charles L. Gaskill</td>
      <td>...</td>
      <td>Helen Gardner, Pearl Sindelar, Miss Fielding, ...</td>
      <td>The fabled queen of Egypt's affair with Roman ...</td>
      <td>5.2</td>
      <td>446</td>
      <td>$ 45000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>25.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0002130</td>
      <td>L'Inferno</td>
      <td>L'Inferno</td>
      <td>1911</td>
      <td>1911-03-06</td>
      <td>Adventure, Drama, Fantasy</td>
      <td>68</td>
      <td>Italy</td>
      <td>Italian</td>
      <td>Francesco Bertolini, Adolfo Padovan</td>
      <td>...</td>
      <td>Salvatore Papa, Arturo Pirovano, Giuseppe de L...</td>
      <td>Loosely adapted from Dante's Divine Comedy and...</td>
      <td>7.0</td>
      <td>2237</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>31.0</td>
      <td>14.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 22 columns</p>
</div>




```python
dataset2.tail()
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
      <th>imdb_title_id</th>
      <th>title</th>
      <th>original_title</th>
      <th>year</th>
      <th>date_published</th>
      <th>genre</th>
      <th>duration</th>
      <th>country</th>
      <th>language</th>
      <th>director</th>
      <th>...</th>
      <th>actors</th>
      <th>description</th>
      <th>avg_vote</th>
      <th>votes</th>
      <th>budget</th>
      <th>usa_gross_income</th>
      <th>worlwide_gross_income</th>
      <th>metascore</th>
      <th>reviews_from_users</th>
      <th>reviews_from_critics</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>85850</th>
      <td>tt9908390</td>
      <td>Le lion</td>
      <td>Le lion</td>
      <td>2020</td>
      <td>2020-01-29</td>
      <td>Comedy</td>
      <td>95</td>
      <td>France, Belgium</td>
      <td>French</td>
      <td>Ludovic Colbeau-Justin</td>
      <td>...</td>
      <td>Dany Boon, Philippe Katerine, Anne Serra, Samu...</td>
      <td>A psychiatric hospital patient pretends to be ...</td>
      <td>5.3</td>
      <td>398</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>$ 3507171</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>85851</th>
      <td>tt9911196</td>
      <td>De Beentjes van Sint-Hildegard</td>
      <td>De Beentjes van Sint-Hildegard</td>
      <td>2020</td>
      <td>2020-02-13</td>
      <td>Comedy, Drama</td>
      <td>103</td>
      <td>Netherlands</td>
      <td>German, Dutch</td>
      <td>Johan Nijenhuis</td>
      <td>...</td>
      <td>Herman Finkers, Johanna ter Steege, Leonie ter...</td>
      <td>A middle-aged veterinary surgeon believes his ...</td>
      <td>7.7</td>
      <td>724</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>$ 7299062</td>
      <td>NaN</td>
      <td>6.0</td>
      <td>4.0</td>
    </tr>
    <tr>
      <th>85852</th>
      <td>tt9911774</td>
      <td>Padmavyuhathile Abhimanyu</td>
      <td>Padmavyuhathile Abhimanyu</td>
      <td>2019</td>
      <td>2019-03-08</td>
      <td>Drama</td>
      <td>130</td>
      <td>India</td>
      <td>Malayalam</td>
      <td>Vineesh Aaradya</td>
      <td>...</td>
      <td>Anoop Chandran, Indrans, Sona Nair, Simon Brit...</td>
      <td>NaN</td>
      <td>7.9</td>
      <td>265</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>85853</th>
      <td>tt9914286</td>
      <td>Sokagin Çocuklari</td>
      <td>Sokagin Çocuklari</td>
      <td>2019</td>
      <td>2019-03-15</td>
      <td>Drama, Family</td>
      <td>98</td>
      <td>Turkey</td>
      <td>Turkish</td>
      <td>Ahmet Faik Akinci</td>
      <td>...</td>
      <td>Ahmet Faik Akinci, Belma Mamati, Metin Keçeci,...</td>
      <td>NaN</td>
      <td>6.4</td>
      <td>194</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>$ 2833</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>85854</th>
      <td>tt9914942</td>
      <td>La vida sense la Sara Amat</td>
      <td>La vida sense la Sara Amat</td>
      <td>2019</td>
      <td>2020-02-05</td>
      <td>Drama</td>
      <td>74</td>
      <td>Spain</td>
      <td>Catalan</td>
      <td>Laura Jou</td>
      <td>...</td>
      <td>Maria Morera Colomer, Biel Rossell Pelfort, Is...</td>
      <td>Pep, a 13-year-old boy, is in love with a girl...</td>
      <td>6.7</td>
      <td>102</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>$ 59794</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 22 columns</p>
</div>



## Dataset 3 : Wine Reviews


```python
import pandas as pd
```


```python
dataset3 = pd.read_csv("winemag-data_first150k.csv")
```


```python
dataset3.head()
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
      <th>country</th>
      <th>description</th>
      <th>designation</th>
      <th>points</th>
      <th>price</th>
      <th>province</th>
      <th>region_1</th>
      <th>region_2</th>
      <th>variety</th>
      <th>winery</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>US</td>
      <td>This tremendous 100% varietal wine hails from ...</td>
      <td>Martha's Vineyard</td>
      <td>96</td>
      <td>235.0</td>
      <td>California</td>
      <td>Napa Valley</td>
      <td>Napa</td>
      <td>Cabernet Sauvignon</td>
      <td>Heitz</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1</td>
      <td>Spain</td>
      <td>Ripe aromas of fig, blackberry and cassis are ...</td>
      <td>Carodorum Selección Especial Reserva</td>
      <td>96</td>
      <td>110.0</td>
      <td>Northern Spain</td>
      <td>Toro</td>
      <td>NaN</td>
      <td>Tinta de Toro</td>
      <td>Bodega Carmen Rodríguez</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>US</td>
      <td>Mac Watson honors the memory of a wine once ma...</td>
      <td>Special Selected Late Harvest</td>
      <td>96</td>
      <td>90.0</td>
      <td>California</td>
      <td>Knights Valley</td>
      <td>Sonoma</td>
      <td>Sauvignon Blanc</td>
      <td>Macauley</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>US</td>
      <td>This spent 20 months in 30% new French oak, an...</td>
      <td>Reserve</td>
      <td>96</td>
      <td>65.0</td>
      <td>Oregon</td>
      <td>Willamette Valley</td>
      <td>Willamette Valley</td>
      <td>Pinot Noir</td>
      <td>Ponzi</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4</td>
      <td>France</td>
      <td>This is the top wine from La Bégude, named aft...</td>
      <td>La Brûlade</td>
      <td>95</td>
      <td>66.0</td>
      <td>Provence</td>
      <td>Bandol</td>
      <td>NaN</td>
      <td>Provence red blend</td>
      <td>Domaine de la Bégude</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataset3.tail()
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
      <th>country</th>
      <th>description</th>
      <th>designation</th>
      <th>points</th>
      <th>price</th>
      <th>province</th>
      <th>region_1</th>
      <th>region_2</th>
      <th>variety</th>
      <th>winery</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>150925</th>
      <td>150925</td>
      <td>Italy</td>
      <td>Many people feel Fiano represents southern Ita...</td>
      <td>NaN</td>
      <td>91</td>
      <td>20.0</td>
      <td>Southern Italy</td>
      <td>Fiano di Avellino</td>
      <td>NaN</td>
      <td>White Blend</td>
      <td>Feudi di San Gregorio</td>
    </tr>
    <tr>
      <th>150926</th>
      <td>150926</td>
      <td>France</td>
      <td>Offers an intriguing nose with ginger, lime an...</td>
      <td>Cuvée Prestige</td>
      <td>91</td>
      <td>27.0</td>
      <td>Champagne</td>
      <td>Champagne</td>
      <td>NaN</td>
      <td>Champagne Blend</td>
      <td>H.Germain</td>
    </tr>
    <tr>
      <th>150927</th>
      <td>150927</td>
      <td>Italy</td>
      <td>This classic example comes from a cru vineyard...</td>
      <td>Terre di Dora</td>
      <td>91</td>
      <td>20.0</td>
      <td>Southern Italy</td>
      <td>Fiano di Avellino</td>
      <td>NaN</td>
      <td>White Blend</td>
      <td>Terredora</td>
    </tr>
    <tr>
      <th>150928</th>
      <td>150928</td>
      <td>France</td>
      <td>A perfect salmon shade, with scents of peaches...</td>
      <td>Grand Brut Rosé</td>
      <td>90</td>
      <td>52.0</td>
      <td>Champagne</td>
      <td>Champagne</td>
      <td>NaN</td>
      <td>Champagne Blend</td>
      <td>Gosset</td>
    </tr>
    <tr>
      <th>150929</th>
      <td>150929</td>
      <td>Italy</td>
      <td>More Pinot Grigios should taste like this. A r...</td>
      <td>NaN</td>
      <td>90</td>
      <td>15.0</td>
      <td>Northeastern Italy</td>
      <td>Alto Adige</td>
      <td>NaN</td>
      <td>Pinot Grigio</td>
      <td>Alois Lageder</td>
    </tr>
  </tbody>
</table>
</div>



## Dataset 4 : IRIS


```python
import pandas as pd
```


```python
dataset4 = pd.read_csv("Iris.csv")
```


```python
dataset4.head()
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
      <th>Id</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
      <th>Species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataset4.tail()
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
      <th>Id</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
      <th>Species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>145</th>
      <td>146</td>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>147</td>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>148</td>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>149</td>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>150</td>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
  </tbody>
</table>
</div>



## Dataset 5 : Museums 


```python
import pandas as pd
```


```python
dataset5 = pd.read_csv("museums.csv")
```


```python
dataset5.head()
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
      <th>Museum ID</th>
      <th>Museum Name</th>
      <th>Legal Name</th>
      <th>Alternate Name</th>
      <th>Museum Type</th>
      <th>Institution Name</th>
      <th>Street Address (Administrative Location)</th>
      <th>City (Administrative Location)</th>
      <th>State (Administrative Location)</th>
      <th>Zip Code (Administrative Location)</th>
      <th>...</th>
      <th>Latitude</th>
      <th>Longitude</th>
      <th>Locale Code (NCES)</th>
      <th>County Code (FIPS)</th>
      <th>State Code (FIPS)</th>
      <th>Region Code (AAM)</th>
      <th>Employer ID Number</th>
      <th>Tax Period</th>
      <th>Income</th>
      <th>Revenue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>8400200098</td>
      <td>ALASKA AVIATION HERITAGE MUSEUM</td>
      <td>ALASKA AVIATION HERITAGE MUSEUM</td>
      <td>NaN</td>
      <td>HISTORY MUSEUM</td>
      <td>NaN</td>
      <td>4721 AIRCRAFT DR</td>
      <td>ANCHORAGE</td>
      <td>AK</td>
      <td>99502</td>
      <td>...</td>
      <td>61.17925</td>
      <td>-149.97254</td>
      <td>1.0</td>
      <td>20.0</td>
      <td>2.0</td>
      <td>6</td>
      <td>920071852</td>
      <td>201312.0</td>
      <td>602912.0</td>
      <td>550236.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>8400200117</td>
      <td>ALASKA BOTANICAL GARDEN</td>
      <td>ALASKA BOTANICAL GARDEN INC</td>
      <td>NaN</td>
      <td>ARBORETUM, BOTANICAL GARDEN, OR NATURE CENTER</td>
      <td>NaN</td>
      <td>4601 CAMPBELL AIRSTRIP RD</td>
      <td>ANCHORAGE</td>
      <td>AK</td>
      <td>99507</td>
      <td>...</td>
      <td>61.16890</td>
      <td>-149.76708</td>
      <td>4.0</td>
      <td>20.0</td>
      <td>2.0</td>
      <td>6</td>
      <td>920115504</td>
      <td>201312.0</td>
      <td>1379576.0</td>
      <td>1323742.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>8400200153</td>
      <td>ALASKA CHALLENGER CENTER FOR SPACE SCIENCE TEC...</td>
      <td>ALASKA CHALLENGER CENTER FOR SPACE SCIENCE TEC...</td>
      <td>NaN</td>
      <td>SCIENCE &amp; TECHNOLOGY MUSEUM OR PLANETARIUM</td>
      <td>NaN</td>
      <td>9711 KENAI SPUR HWY</td>
      <td>KENAI</td>
      <td>AK</td>
      <td>99611</td>
      <td>...</td>
      <td>60.56149</td>
      <td>-151.21598</td>
      <td>3.0</td>
      <td>122.0</td>
      <td>2.0</td>
      <td>6</td>
      <td>921761906</td>
      <td>201312.0</td>
      <td>740030.0</td>
      <td>729080.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>8400200143</td>
      <td>ALASKA EDUCATORS HISTORICAL SOCIETY</td>
      <td>ALASKA EDUCATORS HISTORICAL SOCIETY</td>
      <td>NaN</td>
      <td>HISTORIC PRESERVATION</td>
      <td>NaN</td>
      <td>214 BIRCH STREET</td>
      <td>KENAI</td>
      <td>AK</td>
      <td>99611</td>
      <td>...</td>
      <td>60.56280</td>
      <td>-151.26597</td>
      <td>3.0</td>
      <td>122.0</td>
      <td>2.0</td>
      <td>6</td>
      <td>920165178</td>
      <td>201412.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>8400200027</td>
      <td>ALASKA HERITAGE MUSEUM</td>
      <td>ALASKA AVIATION HERITAGE MUSEUM</td>
      <td>NaN</td>
      <td>HISTORY MUSEUM</td>
      <td>NaN</td>
      <td>301 W NORTHERN LIGHTS BLVD</td>
      <td>ANCHORAGE</td>
      <td>AK</td>
      <td>99503</td>
      <td>...</td>
      <td>61.17925</td>
      <td>-149.97254</td>
      <td>1.0</td>
      <td>20.0</td>
      <td>2.0</td>
      <td>6</td>
      <td>920071852</td>
      <td>201312.0</td>
      <td>602912.0</td>
      <td>550236.0</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 25 columns</p>
</div>




```python
dataset.tail()
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    <ipython-input-22-493f4eee143c> in <module>
    ----> 1 dataset.tail()
    

    NameError: name 'dataset' is not defined



```python

```
