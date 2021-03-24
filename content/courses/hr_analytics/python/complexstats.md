---
title: Complex Statistics
linktitle: Complex Statistics
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 52

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 52
---


## Analyzing Data

Pandas can do much more complex statistics than just the mean or the sum. For more complex work though, we need to make sure we have the `scipy` library – therefore, when we begin our code we need to add:

```
from scipy import stats
```

There’s a long list of functions you could use to get the statistics you need, but the syntax looks like this:

```
# replace 'func_name' with actual function name

stats.func_name()
```

>> *Notice how you don’t actually have to write ”scipy” here. More on that later.*


## Correlations

Correlations measure the strength of a linear relationship between measurement variables and the purpose is to predict and understand the constructs. One useful function in the Pandas library is `corr()`, which will find all relationships for each column that is a continuous variable in your data.

The Result of the corr() method is a table with a lot of numbers that represents how well the relationship is between two columns.

To get the correlations with this method, you do not need to call the `stats` function. Instead, you would write it out using the syntax `corr()`:

```
hr_df.corr()
```

Pearson's Correlation is the most popular method to observe relationships. Pearson's Correlation evaluates the linear relationship between two sets of continuous values and can be computed using Python in a relatively simple way.

The function, `pearsonr()` two column names to determine the strength and direction of the relationship. It also returns 2 values of r and p like so: (0.23, 0.03). To get the correlation with this method, use the `stats` function like so:

```
stats.pearsonr(df_name.col1, df_name.col2)
```

## Tutorial

### Part Three: Correlations

Using the above data, we can obtain the correlation coefficient of two continuous variables. For this example, let's determine whether


The number varies from -1 to 1.

1 means that there is a 1 to 1 relationship (a perfect correlation), and for this data set, each time a value went up in the first column, the other one went up as well.

0.9 is also a good relationship, and if you increase one value, the other will probably increase as well.

-0.9 would be just as good relationship as 0.9, but if you increase one value, the other will probably go down.

0.2 means NOT a good relationship, meaning that if one value goes up does not mean that the other will.
