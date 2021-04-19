---
title: Visualizations
linktitle: Visualizations
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 60

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 60
---

<!-- In this tutorial, I'll share how to visualize data: -->

## Data Visualizations

Within Python, the `matplotlib` library is popular for plotting data. There is also the `seaborn` library which uses functions from `matplotlib` as a foundation and tends to make much more visually appealing plots. Scatter plots, histograms, and count plots are all examples of found in `seaborn`.

All of these plots are customizable through size, shape, color, markers, and more. For now, we will explore colors and markers. For more information on choosing color palettes, check out the seaborn documentation [here](https://seaborn.pydata.org/tutorial/color_palettes.html). For more examples of what `seaborn` can do, click [here](https://seaborn.pydata.org/examples/index.html). You can look up additional plot types [here](https://seaborn.pydata.org/api.html).

To get started, import both `seaborn` and `matplotlib` libraries:

```
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

```
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2)
```


Enhance the graph by including colors and markers into your plots by adding the following arguments:

* Color of plot points = 'purple' (after y-axis)
* Shape of marker = '+' (after y-axis)

Now your code should look something like this:

```
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2, color = 'purple', marker = '+')
```

For more on scatter plots, check out the seaborn documentation [here]('https://seaborn.pydata.org/generated/seaborn.scatterplot.html').

### Histograms

Rather than viewing the relationship of two variables through a scatter plot, we can create plots that show a continuous variable individually. Doing so will display a distribution of the data. Therefore, when continuous variables are present in the data, a histogram can be created through the `distplot()` (short for distribution) function. The `seaborn` library will automatically pick a number for the amount of bins that makes sense based on the data, but to customize you would follow the same format of adding `bins = #` in the argument. For now, we will use `kde = False` to override a default we don't need. Colors can be added to these plots as well.

To plot your data, write your code like this:

```
plot_name = sns.distplot(df_name.col1, kde = False, bins = 5, color = 'orange')
```


### Count Plots

To view a standard bar chart, the `countplot()` function can be used. This type of plot will graph the amount of times a categorical variable appears in the data. To get vertical bars, use `x = df_name.col1` and to get horizontal bars use `y = df_name.col1`.

For vertical bars, your code would look like this:

```
# x = horizontal axis & vertical bars
plot_name = sns.countplot(x = df_name.col1)
```

For horizontal bars, your code would look like this:

```
# y = vertical axis & horizontal bars
plot_name = sns.countplot(y = df_name.col2)
```


## Word Clouds

To visualize text data, one of the most common Python libraries is *wordcloud*. It does not come pre-installed when you downloaded Jupyter Notebook through Anaconda, however, it is easy to install. To install `wordcloud`, go to your preferred IDE (integrated development environment) and enter the following command: `pip install wordcloud`. After it is installed, you can import it just like the any other library and read in your `df` to generate a variety of images.

Begin by installing `wordcloud` and importing the library as shown below:

```
pip install wordcloud

# import libraries
from wordcloud import WordCloud
import matplotlib
%matplotlib inline
import matplotlib.pyplot as plt
```

Next, use the following command and replace 'enter_variable_name_here' with a column from your `df` that you're interested in viewing:

```
# generate wordcloud
wordcloud = WordCloud(background_color = 'black').generate('enter_variable_name_here')
plt.df(wordcloud, interpolations = 'bilinear')
plt.axis('off')
```

For additional resources, click [here]('https://github.com/amueller/word_cloud/blob/master/README.md') for instructions and [here]('http://amueller.github.io/word_cloud/auto_examples/index.html') for examples.