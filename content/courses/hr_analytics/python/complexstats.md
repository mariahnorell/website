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


## Complex Statistics

Pandas can do much more complex statistics than the mean or the sum. For more complex work though, we need to make sure we have the `scipy` library – therefore, when we begin our code we need to add: 

```
from scipy import stats
```

There’s a long list of functions you could use to get the statistics you need, but the syntax looks like this:

```
# replace 'func_name' with actual function name

stats.func_name()
```

> *Notice how you don’t actually have to write ”scipy” here. More on that later.*

### Pearson’s Correlation

Used to evaluate linear relationship between two sets of continuous values. The function, “pearnsonr()” uses the below syntax and returns 2 values of r and p like so: (0.23, 0.03).

```
stats.pearsonr(df_name.col1, df_name.col2)
```