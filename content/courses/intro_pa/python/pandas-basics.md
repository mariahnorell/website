---
title: Pandas Basics
linktitle: Pandas Basics
toc: true
type: book
draft: false
menu:
  intro_pa:
    parent: Python
    weight: 6

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 62
---

<!-- In this tutorial, I'll share how to import pandas, read in a file, and verify the data: -->

## Pandas Library

Pandas is a data analysis tool that makes it easy to work with large data sets and do basic, intermediate, and advanced level manipulations. It's a tool used widely by data analysts and data scientists to perform operations commonly done in Excel or SPSS.

## DataFrames

Pandas operates in a rows-to-columns fashion (2D data set) which is called a 'DataFrame'. Think of a Google spreadsheet, SPSS file, or Excel workbook.

## Creating a DataFrame in Pandas

You can create one from scratch or you can read in a data file. We will begin with reading in Excel files to mimic real-world scenarios and use cases.

### Importing Pandas

Whenever you want to add a new library for your code, the `import` command will be used. Open a Jupyter Notebook file (.ipynb) and write the following command in a code cell:

```python
import pandas
```

Often, programmers shorten libraries to a couple letters to make it cleaner and easier to read. Now when we write code, we can use `pd` instead of `pandas`. This shortcut will be more helpful when working with longer library names, but is a good practice to learn and be aware of now. Here's how we can shorten the `pandas` library name:

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

## Tutorial

Now that we know the three steps to read in our data, let's walk through an example. Download the following HR data set from Kaggle: https://www.kaggle.com/rhuebner/human-resources-data-set
### Reviewing the Data

Can you think of some advantages/disadvantages to using one of these three approaches to review your data?

<script src="https://gist.github.com/mariahnorell/5b1c7601bb1b7c801de1422925d1736c.js"></script>

Try it out! Add a number in the parentheses to pull the amount of data you are interested in viewing.