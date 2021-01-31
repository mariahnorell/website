---
title: Visualization
linktitle: Visualization
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

## Data Visualization

Within Python, there is a Matplotlib library that is popular to create plots with. There is also the Seaborn library which uses functions from matplotlib as a foundation and tends to make much more visually appealing plots.

<!-- Seaborn Functions

Scatter Plots
Histograms
Count Plots -->


To use Seaborn, we have to import both seaborn and matplotlib libaries

```
# Library for df
import pandas as pd

# Library for plotting
import matplotlib
%matplotlib inline
import seaborn as sns
```

Function = regplot()
Reg = short for “regression”

Syntax below:

```
# x = horizontal
# y = vertical
plot_name = sns.regplot(x = df_name.col1, y = df_name.col2)
```

#### Scatter plots:

You can include colors and markers into your plots by adding the following arguments: 

Color: 
color = “red” (after y-axis)
Shape: 
marker = “*” (after y-axis)


#### Histograms & Count Plots

Histograms = continuous data
Count Plots = categorical data

Function = distplot()
dist = short for distribution

Syntax below:

```
# x = horizontal
# y = vertical
plot_name = sns.distplot(x = df_name.col1, y = df_name.col2)
```

You can include colors and markers into your plots by adding the following arguments: 

Color: 

color = “red” (after kde)

Number of Bins: 

Seaborn will automatically pick a number that makes sense

You can change this by adding: 

bins = # (after kde)

#### Count Plots

Function = countplot()

Syntax below:

```
# x = horizontal axis & vertical bars
# y = vertical axis & horizontal bars
plot_name = sns.countplot(x = df_name.col1)
plot_name = sns.countplot(y = df_name.col2)
```

Note about data formatting
• Dataframes can be organized in “short/wide” or “long” format
– Wide format is best for:
• Scatter plots, histograms, count plots
– Long format is best for: • Point plots, bar plots

Wide format
• Percentageofpeoplethathaveusedagiven drug in the past year, according to age


Long format (same data)


Converting wide --> long format
• Doing this manually can be painful if you have a large data set
• Can convert with code instead!

Point plot
• Created using the function pointplot(), which takes the following inputs:
– x = df.col_name • In our example: age
– y = df.col_name
• In our example: percentage
– hue = df.col_name
• Column with category names; each category will be
plotted as a different hue (color)

```
# add example here
point = sns.pointplot(x = df_long.age, y = df_long.percentage, hue = df.df))
```


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
```

## More Resources

For more examples of what seaborn can do, click [here](https://seaborn.pydata.org/examples/index.html). You can look up plots by type [here](https://seaborn.pydata.org/api.html).

## For Fun
Word Clouds

One of the most common Python libraries is "wordcloud". 
https://github.com/amueller/word_cloud/blob/master/README.md
http://amueller.github.io/word_cloud/auto_examples/index.html

Doesn’t come pre-installed, but easy to install with pip (Macs) or conda (PCs):
See the README link on the previous slide for installation instructions. For syntax, see next slide – only thing you’ll need to change is one variable name!

```
# import libraries
from wordcloud import WordCloud
import matplotlib
%matplotlib inline
import matplotlib.pyplot as plt

# generate word cloud
wordcloud = WordCloud(background_color = 'black').gernerate()
plt.df(wordcloud, interpolations = 'bilinear')
plt.axis('off')

# save as pdf
wordcloud.to_file('name.pdf')
