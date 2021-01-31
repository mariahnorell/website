---
title: Pandas Basics
linktitle: Pandas Basics
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 30

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 30
---

<!-- In this tutorial, I'll share how to import pandas, read in a file, and verify the data: -->

## Pandas Library

Pandas is a data analysis tool that makes it easy to work with large data sets and do basic, intermediate, and advanced level manipulations. It's a tool used widely by data analysts and data scientists to perform operations commonly done in Excel or SPSS. Pandas operates in a rows-to-columns fashion (2D dataset) which is called a "dataframe". Think of a Google spreadsheet, SPSS file, or Excel workbook.

## Creating a DataFrame in Pandas

You can create one from scratch or you can read in a data file. In this class we will be reading in csv and excel files to mimic real-world scenarios. 

### Step One: Importing Pandas

Open a Jupyter Notebook file (.ipynb) and write the following command in a code cell: 

```
import pandas as pd
```

### Step Two: Reading in a File

To read in a ".csv" file, we will use a command, "read_csv()" to view the file. First, we must assign a variable and then we can reference our file. See below for some notes on how to do this.

```
# my_df = variable name
# pd = pandas library to convert data into dataframe
# read_csv = command
# 'filename.csv' = replace with appropriate data source
my_df = pd.read_csv('filename.csv')
```

### Step Three: Verifying the Data 

After you read in the csv file, you'll want to verify that it loaded in properly. To do this, we can use three different methods:

> 1. df
> 2. df.head()
> 3. df.tail()

Let's take a look at some examples:

#### df

Returns entire dataset

#### df.head()

Returns the top 5 rows of data

#### df.tail()

Returns the bottom 5 rows of data

If you simply write .head() or .tail(), it will automatically return 5 variables. If you want to return a specific number, simply place that number within the parentheses. For example, .head(3) will return the top three rows of data and .tail(7) will return the bottom seven rows of data.