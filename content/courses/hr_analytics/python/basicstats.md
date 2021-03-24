---
title: Basic Statistics
linktitle: Basic Statistics
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

<!-- In this tutorial, I'll share how to pull basic and complex statistics from a data set: -->

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
df.describe()
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

Alternatively, we could pull the descriptive statistics with the following commands:

* df_name.column_name.mean()
* df_name.column_name.median()
* df_name.column_name.mode()
* df_name.column_name.max()
* df_name.column_name.min()
* df_name.column_name.std()
* df_name.column_name.count()

For example, to obtain the max value of one column in the data set: 

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df.column_name.max()
```

Or, to obtain the counts of one column in the data set:

``` 
import pandas as pd
df = pd.read_csv('filename.csv')
df_name.column_name.count()
```

## Tutorials

To practice what we just learned, let's use sample data to pull these statistics. Download the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set

### Tutorial One: Describe Command
Take a look at the following code and analyze the output. What observations can you make from this initial pull of the data?

<script src="https://gist.github.com/mariahnorell/b3ca4768999f51c5064a3376a1c5051f.js"></script>

### Tutorial Two: Alternative Commands
Identify what the output indicates from the following code. What insights can you gather from looking at the data using these commands?

<script src="https://gist.github.com/mariahnorell/d5b9b1f21dd876307698900bcafbb8a5.js"></script>