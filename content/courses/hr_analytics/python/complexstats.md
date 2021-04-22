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

```python
from scipy import stats
```

There’s a long list of functions you could use to get the statistics you need, but the syntax looks like this:

```python
# replace 'func_name' with actual function name

stats.func_name()
```

<!-- >> *Notice how you don’t actually have to write ”scipy” here. More on that later.* -->

## Correlations

Correlations measure the strength of a linear relationship between measurement variables and the purpose is to predict and understand the constructs. One useful function in the Pandas library is `.corr()`, which will find all relationships for each column that is a continuous variable in your data. It places these values in a tabular format and also automatically excludes blank values from the analysis.

To get the correlations with this method, write it out using the syntax `.corr()`:

```python
hr_df.corr()
```

Pearson's Correlation is the most popular method to observe relationships. Pearson's Correlation evaluates the linear relationship between two sets of continuous values and can be computed in a relatively simple way.

The function `pearsonr()` reads in two column names to determine the strength and direction of the relationship of those constructs. It also returns two values of r and p-value like so: (0.23, 0.03). Recall that the correlation coefficient is represented by r and the p-value helps us determine whether that relationship is statistically significant or not.

To get the correlation with this method, use the `stats` function like so:

```python
stats.pearsonr(df_name.column1, df_name.column2)
```

## Tutorial

We can obtain the correlation coefficient of two continuous variables from a data set. To get started, download the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set
### Part One: Writing the Code
For this example, let's determine whether there is a relationship between *Employee Satisfaction* and *Performance Rating Scores*.

<script src="https://gist.github.com/mariahnorell/b21b82919f46b1faf06a4d6349f6486a.js"></script>

### Part Two: Interpreting the Results

Pearson's Correlation values ranges from -1 to 1, where 0 would indicate no relationship while -1 or +1 would indicate a perfect relationship.

Here's a guide on interpreting the strength and direction of the correlation output:

* -1 = Perfect negative linear relationship
* -0.75 = Strong negative linear relationship
* -0.50 = Moderate negative linear relationship
* -0.25 = Weak negative linear relationship
* 0 = No linear relationship
* +0.25 = Weak positive linear relationship
* +0.50 = Moderate positive linear relationship
* +0.75 = Strong positive linear relationship
* +1 = Perfect positive linear relationship

```markdown
| Correlational Coefficient (r)  | Interpretation |
| ------------- | ------------- |
| -1.00  | Perfect negative linear relationship  |
| -0.75  | Strong negative linear relationship  |
| -0.50  | Moderate negative linear relationship  |
| -0.25  | Weak negative linear relationship  |
| -0.00  | No linear relationship  |
| +0.25  | Weak positive linear relationship  |
| +0.50  | Moderate positive linear relationship  |
| +0.75  | Strong positive linear relationship  |
| +1.00  | Perfect positive linear relationship  |
```

Take a look at the output from above. Is there a relationship between *Employee Satisfaction* and *Performance Rating Scores*? If so, what is the strength and direction?

We can see that r = 0.30 and p < .05 which indicates the following:

> There is a weak, positive linear relationship between Employee Satisfaction and Performance Rating Scores, such that, as the employee is more content with their work the higher their performance review score is. Remember though, correlation does not equal causation!
