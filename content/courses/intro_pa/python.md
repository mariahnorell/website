---
title: Python & Data Analysis
toc: true
type: book
date: "2024-06-15T00:00:00+01:00"
draft: false
params: 
  math: true
menu:
  intro_pa:
    name: Python & Data Analysis
    weight: 60

weight: 60
---

# Introduction

## What is Python?

Python is a programming language that was written by Guido van Rossum in the 1990s. Programming is the process of designing and building a computer program to accomplish many tasks. Some examples include analyzing data, generating algorithms, implementing rules and validations, and much more! This language initially became so popular because it was free and open-sourced, meaning anyone can use it. Python is now one of the most on-demand languages to learn as it is very readable to the user. By 2018, over 8 million people started programming in Python and there's been a steady 8-10% increase in usership year-over-year. This language is great for beginners and is widely used by many professionals in both research and industry, so it will be powerful to have in your analytics tool belt.

Learning Python will give you superpowers in the workplace, especially in the People Analytics field, and the best way to learn this language is to dive right into a project. The following sections contain People Analytics and Human Resources related examples and walkthroughs on how to use this powerful programming language to your advantage.

## Choosing an IDE

You can write Python code in numerous IDEs (integrated development environments). The Python language stays the same regardless of the IDE you choose to use, but each IDE may look different or have different features. Think of it this way: your Gmail or Outlook account still functions as an e-mail account, but can be accessed through many different browsers like Chrome, Firefox, or Safari that have their own characteristics.

Examples of IDEs include:
- [Virtual Studio Code](https://code.visualstudio.com/)
- [Spyder](https://www.spyder-ide.org/)
- [PyCharm](https://www.jetbrains.com/pycharm/)
- [Jupyter Notebook](https://jupyter.org/)

### Installing Anaconda
Anaconda is an open-source (i.e., free) environment for individuals to write code and is helpful to all data analysts. Go to [anaconda.com](https://www.anaconda.com/products/individual) to download Python 3.7 for your computer and follow all instruction prompts.

### Jupyter Notebook Basics

Jupyter Notebook is a very user-friendly IDE that allows you to chunk out your code and write in text in a clear way. The way we add in this text is through something called *Markdown*. It is helpful to alternate between writing in Markdown and writing code because it will visually organize the project you set out to accomplish. In addition, organizing your Notebook will help others (i.e., colleagues, interview committees, friends) understand your thought process.

Open up this [tutorial](https://www.dataquest.io/blog/jupyter-notebook-tutorial/) to understand all necessary steps for running Jupyter and getting your first notebook ready.

While getting everything set up, locate a place on your computer that will be easy to access all notebooks for this class. It's recommended to utilize cloud-based storage tools like iCloud, OneDrive, Dropbox, Google Drive, rather than your desktop to ensure you do not lose any work.

### What is Markdown?

```md
### Hello, this is Markdown.
#### This font is a little smaller.
###### This font is even smaller. We can also write in *italic* and create numbered lists:
- Header
    - Second Level
        - Third Level

We can also write in **bold** and add links like [this one](https://youtu.be/dQw4w9WgXcQ).

> Blockquotes look like this and help highlight a key point you're trying to make.

Markdown is particularly helpful when we want to include notes about our code.
```

*Here's how that output looks:*

---

### Hello, this is Markdown.
#### This font is a little smaller.
###### This font is even smaller. We can also write in *italic* and create numbered lists:
- Header
    - Second Level
        - Third Level

We can also write in **bold** and add links like [this one](https://youtu.be/dQw4w9WgXcQ).

> Blockquotes look like this and help highlight a key point you're trying to make.

Markdown is particularly helpful when we want to include notes about our code.

---

Now that we have installed Anaconda and have Jupyter Notebook, we can begin coding!


## Pandas Library

Programming languages have libraries that act as a collection of code that has been stored together in one single file. Using the designated code 'unlocks' your access to that library, which in turn allows you to do some pretty powerful computing. To start writing Python code, you will need to do your research on which libraries you need for your analysis. For now, we will begin with the Pandas library.

Pandas is a library within Python that makes data analysis with large data sets easy. It allows anyone to do basic, intermediate, and advanced level manipulations. It is widely used by data analysts and data scientists to perform operations commonly done in Excel, SPSS, or R. Pandas operates in a rows-to-columns fashion (2D data set) which is called a 'DataFrame'. Think of a Google spreadsheet, SPSS file, or Excel workbook. You can create a DataFrame from scratch or you can read in a data file. Most commonly, this is shortened to `df` when writing code. We will begin with reading in Excel files to mimic real-world scenarios and use cases. 

Whenever you want to add a new library for your code, the `import` command will be used. Open up a Jupyter Notebook file (.ipynb) and write the following command in a code cell:

```python
import pandas
```

Often, programmers shorten libraries to a couple letters to make it cleaner and easier to read. Now when we write code, we can use `pd` instead of `pandas`. This shortcut will be more helpful when working with longer library names, but is a good practice to learn and be aware of now. Here's how we can shorten the Pandas library name:

```python
import pandas as pd
```

### Reading in a File

It's good practice to assign the line of code you are trying to run to a variable. To read in a .csv file for example, first assign it a variable name. Doing so will help later when we want to reference the file because we won't have to re-write the command, we will be able to reference the variable name used.

The syntax, or order in which the code should be written so that Python can understand what you're trying to accomplish, for reading in Excel (.xlsx) files look like this:

```python
my_variable = pandas.read_excel('filename.xlsx')
```

And for .csv files:

```python
my_variable = pandas.read_csv('filename.csv')
```

Sometimes writing notes in your code can help organize what is being called. See below for an example on writing a comment:

```python
# This is an example of a comment, which can be used as a note for you to keep your code organized.
# When writing '#' followed by your notes, Python ignores what is written and does not try to compute anything.
```

Here is an example of how you can structure your comments and code so far:

```python
# Import Pandas library
import pandas as pd

# Read in .csv file
my_variable = pd.read_csv('filename.csv')
```

### Verifying the Data

After reading in the .csv file, it is important to verify that it loaded in properly. To do this, we can use three different methods:

1. my_variable
2. my_variable.head()
3. my_variable.tail()

Let's take a look at some examples:

#### my_variable

Returns entire data set

```python
import pandas as pd
my_variable = pd.read_csv('filename.csv')
my_variable
```

#### my_variable.head()

Returns the top 5 rows of data

```python
import pandas as pd
my_variable = pd.read_csv('filename.csv')
my_variable.head()
```

#### my_variable.tail()

Returns the bottom 5 rows of data

```python
import pandas as pd
my_variable = pd.read_csv('filename.csv')
my_variable.tail()
```

Writing .head() or .tail(), it will automatically return 5 variables. To return a specific number, place that desired number within the parentheses. For example, `.head(3)` will return the top three rows of data and `.tail(7)` will return the bottom seven rows of data.

## Tutorial 1

Now that we know the three steps to read in our data, let's walk through an example. Download the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set. Take a moment to download this file and navigate where you just set up your Jupyter notebook files. Create a folder to store all practice files and materials. Then open up the Anaconda app, navigate to the Jupyter notebook section, and find the folder you just created to begin a new project. 

### Reviewing the Data

Can you think of some advantages/disadvantages to using one of these three approaches to review your data?

<script src="https://gist.github.com/mariahnorell/5b1c7601bb1b7c801de1422925d1736c.js"></script>

Try it out! Add a number in the parentheses to pull the amount of data you are interested in viewing.

## Ways to Filter and View Data

### Indexing with Numbers

From the above section, we pulled all data to look at and in all one view. Often, the sheer volume of data you will work with will require you to filter down to only the relevant variables. In other words, instead of looking at a file with all rows and columns, you may really only be interested in some rows and/or some columns. One way we can select (or filter) our variables is to do something called indexing. Here's an example of how to pull a column of information you can write:

```python
hr_df['Age']
```

To pull the nth value in the 'Education' column you can write the following:

```python
df.column_name[n]
```

Here's another example:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.Education[3]
```

Here's another example where we can slice the data even more. For example, you would start the index at 'a' and stop before 'b'.

```python
# : = all rows
# 0:1 = one column slice
df_name.iloc[:, 0:1]
```

```python
# 0:1 = one row slice
# : = all rows
df_name.iloc[:, 0:1]
```

<!-- How does it look with some data?
We are interested in looking at
Employee ID
Age
Attrition

For Employee IDs:
 #2, 3, 4, 5, 6, 7, 8, & 9

How do we start going about this?

What row/column #s are of interest?

Let's practice! -->

Let’s try with whole rows or columns. The syntax here is `iloc` and is followed by two sets of values in brackets like this `[a:b, c:d]`. In this example, `a:b` represents a row slice and `c:d` represents a column slice. These represent upper and lower bounds. Here is how we would write this:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.iloc[0:1, 1:2]
```

This would return rows 0 and column 1. The upper bounds in the syntax act as a stopper, so if you wanted to capture two rows and two columns, you would modify your code like this:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.iloc[0:2, 1:3]
```

To see all the rows or all the columns, place the colon in the brackets without any numbers:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.iloc[:, :]
```

### Indexing with Booleans

We just learned how to slice our data by selecting the appropriate numbers for the rows and columns, but what if you don’t know exactly what to look for? Sometimes we deal with data sets that are so big we don't know what column number to search for. Instead, we can search through something called a 'Boolean expression'.

We can search within a specific column to return a specific row.

<!-- Let's search the "MaritalStatus" column and return data for the row(s) containing "Divorced". -->

An example of the syntax structure:

```python
df_name[df_name.col_name[operator][value]]
```

We can use the same general syntax to find data that meets some criteria. Essentially just need to choose:
  * An operator (e.g., <, <=, >, >=, ==, !=)
  * A value (a string or number)

<!-- Return data from the df that:
- matches a string like "female"

Obtain greater than or less than a value:
- Job Satisfaction score over 3

Represents a minimum or maximum age value:
- Lowest age in the data set -->

### Sorting Data

Often, it is easier to look at data once it has been sorted from largest to smallest or the reverse, for any given column. In the Pandas library, the default syntax is to sort in ascending order. For example, we could sort our data by the Age column, this is what we would write:

```python
Syntax = df_name.sort_values(by=col_name)
example = df_name.sort_values(by='Age')
```

To sort in descending order, you add one argument to the syntax exactly as follows:

```python
Syntax = df_name.sort_values(by=col_name, ascending = False)
hr_df.sort_values(by = 'column name', ascending = False)
```

<!-- ### Viewing vs. Changing the DF -->
It's important to note that 'sort_values()' does not **change** the data. Everything we have learned so far are different ways to **view** the data and not manipulate it.

<!-- Consider adding tutorial here!!! -->

## Descriptive Statistics

Just like in Excel, there are some quick ways to pull basic (and even some complex) statistics in Python. Within the Pandas library, there is one shortcut command that pulls:

* Total number of observations
* Mean, median, mode
* Standard deviation
* Min and max

To write it out, use the syntax `.describe()`:

```python
# Combined syntax:
df.describe()
```

To obtain the high-level statistics of the entire data set:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.describe()
```

To obtain the high-level statistics of one column in the data set:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.column_name.describe()
```

Alternatively, we could pull the descriptive statistics with the following commands:

| Descriptive Statistics | Code |
| ------------- | ------------- |
| Mean | `df_name.column_name.mean()` |
| Median | `df_name.column_name.median()` |
| Mode | `df_name.column_name.mode()` |
| Maximum Value | `df_name.column_name.max()` |
| Minimum Value | `df_name.column_name.min()` |
| Standard Deviation | `df_name.column_name.std()` |
| Count Instances | `df_name.column_name.count()` |

For example, to obtain the max value of one column in the data set we would use this command:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df.column_name.max()
```

Or, to obtain the counts of one column in the data set we would use this command:

```python
import pandas as pd
df = pd.read_csv('filename.csv')
df_name.column_name.count()
```

## Tutorial 2

We just learned how to obtain high level descriptive statistics data. To practice what we just learned, let's use the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set. 

### Part One: Describe Command

Take a look at the following code and analyze the output. What observations can you make from this initial pull of the data?

<script src="https://gist.github.com/mariahnorell/b3ca4768999f51c5064a3376a1c5051f.js"></script>

### Part Two: Alternative Commands

What insights can you gather from looking at the data using these commands?

<script src="https://gist.github.com/mariahnorell/d5b9b1f21dd876307698900bcafbb8a5.js"></script>

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

## Tutorial 3

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

A linear regression is an attempt to model the relationship between two variables by fitting the linear equation to the observed data (i.e., finding the line of best fit). Statisticians, data scientists, and business professionals use linear regressions often as a means to predict the values of one variable from values of the other variables in question. One variable is explanatory (i.e., independent variable) and the other is predicted (i.e., dependent variable). Sometimes, there might be more than one explanatory or predicted variable, but more on that later.

### Assumptions

Depending on the question you are trying to answer, there will be a variety of assumptions/conditions needed to ensure proper model predictions and estimates.

The following are the core assumptions needed for linear regression modeling: 

1. Linear Relationship Exists
2. Independence of Residuals
3. Homoscedasticity
4. Normality

### Formula

Below is the linear regression formula, where *X* is the explanatory variable and *Y* is the predicted variable. The slope of the line is *b* and *a* is the intercept (i.e., the value of *Y* when *X* = 0).

$Y = a + bX$

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

## Data Visualizations

Within Python, the `matplotlib` library is popular for plotting data. There is also the `seaborn` library which uses functions from `matplotlib` as a foundation and tends to make much more visually appealing plots. Scatter plots, histograms, and count plots are all examples of found in `seaborn`.

All of these plots are customizable through size, shape, color, markers, and more. For now, we will explore colors and markers. For more information on choosing color palettes, check out the seaborn documentation [here](https://seaborn.pydata.org/tutorial/color_palettes.html). For more examples of what `seaborn` can do, click [here](https://seaborn.pydata.org/examples/index.html). You can look up additional plot types [here](https://seaborn.pydata.org/api.html).

To get started, import both `seaborn` and `matplotlib` libraries:

```python
# Library for df (remember df = dataframe)
import pandas as pd

# Library for plotting - we need all of these commands
import matplotlib
%matplotlib inline
import seaborn as sns
```

### Scatter Plots

To visually see the relationship between two variables, scatter plots can be very helpful. To view a scatter plot of the data, `seaborn` has a function called `regplot()` (short for regression) which will graph the desired data points on both the x and y axis.

The way you would format your code looks like this:

```python
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2)
```

Enhance the graph by including colors and markers into your plots by adding the following arguments:

* Color of plot points = 'purple' (after y-axis)
* Shape of marker = '+' (after y-axis)

Now your code should look something like this:

```python
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2, color = 'purple', marker = '+')
```

For more on scatter plots, check out the seaborn documentation [here]('https://seaborn.pydata.org/generated/seaborn.scatterplot.html').

### Histograms

Rather than viewing the relationship of two variables through a scatter plot, we can create plots that show a continuous variable individually. Doing so will display a distribution of the data. Therefore, when continuous variables are present in the data, a histogram can be created through the `distplot()` (short for distribution) function. The `seaborn` library will automatically pick a number for the amount of bins that makes sense based on the data, but to customize you would follow the same format of adding `bins = #` in the argument. For now, we will use `kde = False` to override a default we don't need. Colors can be added to these plots as well.

To plot your data, write your code like this:

```python
plot_name = sns.distplot(df_name.col1, kde = False, bins = 5, color = 'orange')
```

### Count Plots

To view a standard bar chart, the `countplot()` function can be used. This type of plot will graph the amount of times a categorical variable appears in the data. To get vertical bars, use `x = df_name.col1` and to get horizontal bars use `y = df_name.col1`.

For vertical bars, your code would look like this:

```python
# x = horizontal axis & vertical bars
plot_name = sns.countplot(x = df_name.col1)
```

For horizontal bars, your code would look like this:

```python
# y = vertical axis & horizontal bars
plot_name = sns.countplot(y = df_name.col2)
```

### Word Clouds

To visualize text data, one of the most common Python libraries is *wordcloud*. It does not come pre-installed when you downloaded Jupyter Notebook through Anaconda, however, it is easy to install. To install `wordcloud`, go to your preferred IDE (integrated development environment) and enter the following command: `pip install wordcloud`. After it is installed, you can import it just like the any other library and read in your `df` to generate a variety of images.

Begin by installing `wordcloud` and importing the library as shown below:

```python
pip install wordcloud

# import libraries
from wordcloud import WordCloud
import matplotlib
%matplotlib inline
import matplotlib.pyplot as plt
```

Next, use the following command and replace 'enter_variable_name_here' with a column from your `df` that you're interested in viewing:

```python
# generate wordcloud
wordcloud = WordCloud(background_color = 'black').generate('enter_variable_name_here')
plt.df(wordcloud, interpolations = 'bilinear')
plt.axis('off')
```

For additional resources, click [here]('https://github.com/amueller/word_cloud/blob/master/README.md') for instructions and [here]('http://amueller.github.io/word_cloud/auto_examples/index.html') for examples.