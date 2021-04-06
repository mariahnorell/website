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

Within Python, there is a `matplotlib` library that is popular to create plots with. There is also the `seaborn` library which uses functions from `matplotlib` as a foundation and tends to make much more visually appealing plots. Scatter plots, histograms, and count plots are examples found in `seaborn`.

To get started, import both `seaborn` and `matplotlib` libaries:

```
# Library for df
import pandas as pd

# Library for plotting
import matplotlib
%matplotlib inline
import seaborn as sns
```

### Scatter Plots

To view a scatter plot of the data, `seaborn` has a function called, `regplot()` (short for regression) which will graph the desired data points on the x and y axis.


The way you would format your code looks like this:

```
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2)
```


Additionally, you can enhance the graph by including colors and markers into your plots by adding the following arguments:

* Color of plot points = 'purple' (after y-axis)
* Shape of marker = '+' (after y-axis)

Therefore, your code would look like this:

```
# x = horizontal axis variable
# y = vertical axis variable
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2, color = 'purple', marker = '+')
```

### Histograms

Rather than viewing the relationship of two variables through a scatter plot, we can create plots that show a continuous variable individually. Doing so will display a distribution of the data. Therefore, when continuous variables are present in the data, a histogram can be created through the `distplot()` (short for distribution) function. The `seaborn` library will automatically pick a number for the amount of bins that makes sense based on the data, but to customize you would follow the same format of adding `bins = #` in the argument. For now, we will use `kde = False` to override a default we don't need. Colors can be added to these plots as well.

To plot your data, write your code like this:

```
plot_name = sns.distplot(df_name.col1, kde = False, bins = 5, 'color = 'orange')
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

<!-- Note about data formatting
• Dataframes can be organized in “short/wide” or “long” format
– Wide format is best for:
• Scatter plots, histograms, count plots
– Long format is best for: • Point plots, bar plots

Wide format
• Percentageofpeoplethathaveusedagiven drug in the past year, according to age


Long format (same data)


Converting wide to long format
• Doing this manually can be painful if you have a large data set
• Can convert with code instead!

Point plot
• Created using the function pointplot(), which takes the following inputs:
– x = df.col_name • In our example: age
– y = df.col_name
• In our example: percentage
– hue = df.col_name
• Column with category names; each category will be
plotted as a different hue (color) -->

<!-- ```
# add example here
point = sns.pointplot(x = df_long.age, y = df_long.percentage, hue = df.df))
``` -->

<!--
Bar plot
• Created using the function barplot(), which takes the following inputs:
– x = df.col_name • In our example: age
– y = df.col_name
• In our example: percentage
– hue = df.col_name
• Column with category names; each category will be
plotted as a different hue (color)

```
# add example here
point = sns.barplot(x = df_long.age, y = df_long.percentage, hue = df.df))
```

Need to use the following two commands:
1. fig = my_plot.get_figure()
2. fig.savefig(‘my_plot.pdf’)

```
# add example here
point = sns.barplot(x = df_long.age, y = df_long.percentage, hue = df.df))
fig = my_plot.get_figure()
fig.savefig(‘my_plot.pdf’)
``` -->

## For Fun: Word Clouds

One of the most common Python libraries is "wordcloud". For additional resources, click [here]('https://github.com/amueller/word_cloud/blob/master/README.md') for instructions and [here]('http://amueller.github.io/word_cloud/auto_examples/index.html') for examples.

`Wordcloud` does not come pre-installed, but is easy to install with pip (Macs) or conda (PCs). To install `wordcloud`, navigate to your IDE and enter the command: `pip install wordcloud`. Once installed, you can import to begin reading in a `df` to generate a variety of examples through boundary maps, emojis, single word and frequency images.

```
pip install wordcloud

# import libraries
from wordcloud import WordCloud
import matplotlib
%matplotlib inline
import matplotlib.pyplot as plt

# generate word cloud
wordcloud = WordCloud(background_color = 'black').generate()
plt.df(wordcloud, interpolations = 'bilinear')
plt.axis('off')

# save as pdf
wordcloud.to_file('name.pdf')
```

## More Resources

For more examples of what `seaborn` can do, click [here](https://seaborn.pydata.org/examples/index.html). You can look up additional plot types [here](https://seaborn.pydata.org/api.html).