---
title: Statistics in Python
linktitle: Statistics in Python
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 50

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 50
---

<!-- In this tutorial, I'll share how to pull basic and complex statistics from a dataset: -->

<!-- ## NumPy Library

NumPy supports processing large sets of data as well as complex mathematical functions. -->

## Describing Data

Just like in Excel, there are some quick ways to pull basic (and even some complex) statistics in Python. Within the `pandas` library, there is one shortcut command that pulls: 

* Total number of observations
* Mean, median, mode
* Standard deviation
* Min and max

To write it out, use the syntax `.describe()`:

```
# Combined syntax: 
df_name.describe()
```

To obtain the high-level statistics of the entire data set: 

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df.describe()
```

To obtain the high-level statistics of one column in the data set:

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df.column_name.describe()
```

Alternatively, we could pull the descriptive statistics with the following four commands:

* df_name.column_name.mean()
* df_name.column_name.median()
* df_name.column_name.max()
* df_name.column_name.std()
* df_name.column_name.mode()
* df_name.column_name.count()

For example, to obtain the max value of one column in the data set: 

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df.column_name.max()
```

Or, to obtain the standard deviation of one column in the data set:

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df_name.column_name.std()
```

## Tutorial

To practice what we just learned, let's use sample data to pull these statistics. Download the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set

After saving the file to your preferred directory, assign it to a variable and review the first five rows:

``` 
import pandas as pd
hrdata = pd.read_csv('HRDataset_v14.csv')
hrdata.head()
```

![First five rows of the HR dataset in a DataFrame](hr_df.head.jpg)

Next, let's review the high-level statistics of the entire data set: 

``` 
hrdata.describe()
```

Add in the column name of interest to view the high-level statistics there:

``` 
hrdata.PerfScoreID.describe()
```

