---
title: Complex Statistics
linktitle: Complex Statistics
toc: true
type: book
draft: false
menu:
  intro_pa:
    parent: Python
    weight: 6

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 65

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

Take a look at the output from above. Is there a relationship between *Employee Satisfaction* and *Performance Rating Scores*? If so, what is the strength and direction?

We can see that r = 0.30 and p < .05 which indicates the following:

> There is a weak, positive linear relationship between Employee Satisfaction and Performance Rating Scores, such that, as the employee is more content with their work the higher their performance review score is. Remember though, correlation does not equal causation!

## Linear Regression

John Tukey (an American mathematician and statistician) once said, “An approximate answer to the right problem is worth a good deal more than an exact answer to an approximate problem.” 

### Definition

Ultimately, a linear regression is an attempt to model the relationship between two variables by fitting the linear equation to the observed data (i.e., finding the line of best fit). Statisticians, data scientists, and business professionals use linear regressions often as a means to predict the values of one variable from values of the other variables in question. In a linear regression, one variable is explanatory (i.e., independent variable) and the other is predicted (i.e., dependent variable). Sometimes, there might be more than one explanatory or predicted variable, but more on that later.

### Assumptions

Depending on the model you build, there will be a variety of assumptions/conditions needed to ensure proper model predictions and estimates.

The following are the core assumptions needed for linear regression modeling: 

1. Linear Relationship Exists
2. Independence of Residuals
3. Homoscedasticity
4. Normality

### Formula

Below is the linear regression formula, where *X* is the explanatory variable and *Y* is the predicted variable. The slope of the line is *b* and *a* is the intercept (i.e., the value of *Y* when *X* = 0).

$$Y = a + bX$$

Here's the explanations at a glance:
| Variables  | Interpretation |
| ------------- | ------------- |
| Y | Dependent Variable |
| X | Explanatory Variable |
| b | Slope of the Line |
| a | Intercept |

<!-- ### Finding the Line of Best-Fit

Regressions are all about finding the best-fit line throughout sets of data. Getting the line of best-fit is typically done through a method called the 'least-quares' error solution. This means the regression equation minimizes the differences between data points and the line. 

The least-squares method uses the error of prediction 

The formula for the error of prediction is the distance between the actual (Y) value and the predicted (Ŷ) value.  

$$Y - Ŷ$$


In regression analyses, a prediction error can be used as a measure to determine how well the model does on the predicted variable. 

A line that is the best fit for the actual data that minimizes prediction errors. -->

### Interpretation of Results

Before attempting to fit a linear model to observed data, first determine whether or not there is a relationship between the variables of interest. If a correlation exists, this does not imply that one variable causes the other, but that there is some significant association between the two variables. In other words, correlation does not equal causation. 

When reviewing the data as a scatter plot on a graph, take notice to the outliers/outriders and determine their importance (or deterance) to the data. 

When reviewing the model results, the first number you can focus in on is R Square. R Square explains the goodness of fit - the closer to 1.00 the better!