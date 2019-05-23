---
layout: posts
title: Facebook Analytics using ggplot in Python
tags: [python ggplot, python in r, data analytics]
date: 2019-05-23 11:15 -0400
---
Project 1 CTW Directed Readings 4999
Using data from Facebook group create data visualization similar to ggplot2 but using Python 3

1.Import data using pandas. Facebook downloads data as a .xls. In order to use the data must me cleaned and merged into a .csv file format.


```python
import pandas as pd
import numpy as np
from plotnine import *
houses = "C:\\Users\\new user\\Downloads\\FB4Project1.csv"
df = pd.read_csv(houses)
df.head()
print(df.dtypes)

```

    Date                              object
    Total Members                      int64
    Pending Members                    int64
    Approved Member Requests           int64
    Declined Member Requests           int64
    Posts                              int64
    Comments                           int64
    Reactions                          int64
    Active Members                     int64
    Popular Days                      object
    Posts, Comments and Reactions    float64
    Popular Times                     object
    12:00 AM                         float64
    1:00 AM                          float64
    2:00 AM                          float64
    3:00 AM                          float64
    4:00 AM                          float64
    5:00 AM                          float64
    6:00 AM                          float64
    7:00 AM                          float64
    8:00 AM                          float64
    9:00 AM                          float64
    10:00 AM                         float64
    11:00 AM                         float64
    12:00 PM                         float64
    1:00 PM                          float64
    2:00 PM                          float64
    3:00 PM                          float64
    4:00 PM                          float64
    5:00 PM                          float64
    6:00 PM                          float64
    7:00 PM                          float64
    8:00 PM                          float64
    9:00 PM                          float64
    10:00 PM                         float64
    11:00 PM                         float64
    Age Range                         object
    Women                            float64
    % Women                           object
    Men                              float64
    % Men                             object
    Custom Gender                    float64
    % Custom Gender                   object
    Top Cities                        object
    Members                          float64
    Countries                         object
    Members.1                        float64
    dtype: object


2.Bar chart

```python
    ggplot(df, aes(x='Posts')) + geom_histogram(bins=10)+  ggtitle("Posts")
```


![png](/images/output_4_0.png)










```python
3.Scatter Chart
```


```python
ggplot(df, aes(x='Posts', y='Reactions')) + geom_point(shape=5, color="blue")
```


![png](/images/output_6_0.png)










```python
4.Line Chart
```


```python
df['Date'] = df.index
myarrow=arrow(angle = 15, ends = "both", type = "closed")
ggplot(aes(x='x'), data=df) +\
    geom_line(aes(y='Total Members'), color='green', linetype = "dashed",arrow=myarrow)
```


![png](/images/output_8_0.png)










```python
5.Histograph
```


```python
ggplot(df, aes(x='Reactions', y='Comments')) +\
        geom_boxplot() + ggtitle("Reactions vs Comments")
```


![png](/images/output_10_0.png)





    




```python

```
