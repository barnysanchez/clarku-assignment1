# Publicly available datasets 

## Dataset example:

- Link: [Google Dataset](https://www.google.com)

- Purpose (what would you use this dataset for, explain, a short paragraph): 
I would use this "dataset" (not really a dataset) to search for more details of extratestrial life. 

## Dataset 1:

- Link: [Kaggle Dataset](https://www.kaggle.com/jboysen/mri-and-alzheimers)
- Purpose : I would suggest to predict the alzheimer's disease using cross-sectional data

## Dataset 2:

- Link: [Kaggle Dataset](https://www.kaggle.com/crawford/noaa-storm-events-database)
- Purpose: This dataset can be really helpful in identifying the most affected areas and where the damage has been the most. This can help an insurance company decide where to send their representatives first.

## Dataset 3:

- Link: [DBarchive](ftp://ftp.biosciencedbc.jp/archive/open-tggates/LATEST/open_tggates_biochemistry.zip)
- Purpose: This is a dataset on chemical experiments on rats. This can help identify and understand the affect of certain chemicals and their doses.

## Dataset 4:

- Link: [Canada open database](https://open.canada.ca/data/en/dataset/e319d795-50c8-4c7e-96b5-c821ac235395)
- Purpose : This dataset contains the amounts of fats consumed by proportions and dietry regulations to predict and regulate the fat consumption.

## Dataset 5:

- Link: [3D High Density mmWave Interconnects, Phase I](https://catalog.data.gov/dataset/3d-high-density-mmwave-interconnects-phase-i)
- Purpose: This dataset can be used to monitor and detect the density of mmwave 5G spectrum network. This model can further be used to predict the usage to identify the areas of high and low useage.

# Dataset information


## Chosen dataset: Dataset 1


```import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline

sns.set()

df = pd.read_csv('/Users/akshaykasera/Desktop/oasis_longitudinal.csv')
df.head()
```


```python
# You will now proceed with a serious of commands in the next cell(s) that demonstrate some level of manipulation of the dataset that you are interested, in my case dataset1

# As you enter and execute commands leave the outputs so that I can read the manipulation that you did. Use all of your python skills here that you wish

# As an example I am providing some commands that have absolutly nothing to do with a dataset but just to illustrate the capture in my Jupyter notebook

# Once done, you can save this Jupyter notebook as a markdown and this is what I want you to commit to your private repo. Once you have your assignment ready, invite me to your private repo
```


```python
list1 = range(1,11)
```


```python
    1) Are we having fun yet? YES!
    2) Are we having fun yet? YES!
    3) Are we having fun yet? YES!
    4) Are we having fun yet? YES!
    5) Are we having fun yet? YES!
    6) Are we having fun yet? YES!
    7) Are we having fun yet? YES!
    8) Are we having fun yet? YES!
    9) Are we having fun yet? YES!
    10) Are we having fun yet? YES!



```python
list1[3:-6]
```




    range(4, 5)




```python

```
