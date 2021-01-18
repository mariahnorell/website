---
title: Statistics in Python
linktitle: Statistics in Python
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 30

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6
---

In this tutorial, I'll share how to pull basic and complex statistics from a dataset:

## Descriptives
Total number of observations
Mean, median, mode
Standard deviation
Min and max

```
# Combined syntax: 
df_name.describe()
```


Descriptives –Separated Out

Instead of using the .describe() method, we could ask for the descriptive statistics individuals
df_name.col_name.mean()
df_name.col_name.median()
df_name.col_name.max()
df_name.col_name.std()


Complex Statistics

Pandas can do much more complex statistics than the mean or the sum

For more complex work though, we need to make sure we have the “scipy” library – therefore, when we begin our code we need to add: 

```
from scipy import stats
```

scipy and stats

There’s a long list of functions you could use to get the statistics you need, but the syntax looks like this:

```
# replace 'func_name' with actual function name
stats.func_name()
```

*Notice how you don’t actually have to write ”scipy” here

Basic statistics using scipy
Today we will learn about 
Correlations (Pearson)

#### Pearson’s Correlation

Used to evaluate linear relationship between two sets of continuous values

The function, “pearnsonr()” uses the below syntax and returns 2 values of r and p like so: (0.23, 0.03)

```
stats.pearsonr(df_name.col1, df_name.col2)
```

