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

You can create one from scratch or you can read in a data file. In this class we will begin with reading in Excel files to mimic real-world scenarios and use cases.

### Step One: Importing Pandas

Whenever you want to add a new library for your code, the 'import' command will be used. Open a Jupyter Notebook file (.ipynb) and write the following command in a code cell: 

```
import pandas
```

Often, programmers shorten the library to a couple letters to make it cleaner and easier to read. Here's how we can shorten our library name: 

```
import pandas as pd
```

Now when we write code, we can use `pd` instead of writing out the whole word, `pandas`. This shortcut will be more helpful when working with longer library names, but is a good practice to learn and be aware of now.

### Step Two: Reading in a File

To read in a ".csv" file, we will use a command, "read_csv()" to view the file. First, we must assign it to a variable name and then we can read in the file. Sometimes writing notes in your code can help organize what is being called. See below for an example on writing a comment:

```
# This is an example of a comment, which can be used as a note for you to keep your code organized. When writing '#' followed by your notes, Python ignores what is written and does not try to compute anything.
```

The syntax, or order in which the code should be written so that Python can understand what you're trying to accomplish, for reading in Excel (.xlsx) files look like this:

```
variable = pandas.read_excel('filename.xlsx')
```

And for .csv files: 

```
variable = pandas.read_csv('filename.csv')


For this first example, let's define our variable as `my_df` which stands for 'my dataframe'. We will cover dataframes in more detail in the next section, but for now let's just see what it does: 

```
# my_df = variable name
# pd = pandas library to convert data into dataframe
# read_csv = command
# 'filename.csv' = replace with appropriate data source
my_df = pandas.read_csv('filename.csv')
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