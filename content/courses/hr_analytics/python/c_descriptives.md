---
title: Descriptive Statistics
linktitle: Descriptive Statistics
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 10

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 6
---

In this tutorial, I'll share my top 10 tips for getting started with Academic:

## Descriptive Statistics
Total number of observations
Mean, median, mode
Standard deviation
Min and max

```
# Combined syntax: 
df_name.describe()
```


Descriptive Stats –Separated Out

Instead of using the .describe() method, we could ask for the descriptive statistics individuals
df_name.col_name.mean()
df_name.col_name.median()
df_name.col_name.max()
df_name.col_name.std()


