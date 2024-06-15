---
title: Data Slicing
linktitle: Data Slicing
toc: true
type: book
draft: false
menu:
  intro_pa:
    parent: Python
    weight: 40

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 40
---

<!-- In this tutorial, I'll share how to view subsets and sort DataFrames: -->

## DataFrames

Recall that Pandas operates in a rows-to-columns fashion (2D data set) called a 'DataFrame'. Most commonly, this is shortened to `df` when writing code.


## Indexing with Numbers

Indexing means we want to select a specific row/column in a DataFrame. To pull a column of information you can write:

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

#### What is slicing?

Think of slicing like chunking up the data into smaller pieces. For example, you would start the index at 'a' and stop before 'b'.

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

## Indexing with Booleans

We just learned how to sort our data by selecting the appropriate numbers for the rows and columns, but what if you don’t know exactly what to look for? Sometimes we deal with data sets that are so big we don't know what column number to search for. Instead, we can search through something called a 'Boolean expression'.

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

## Sorting Data

Ascending: When you sort your data by a particular column, the default is to sort in ascending order. For example, we could sort our data by the Age column:

```python
Syntax = df_name.sort_values(by=col_name)
example = df_name.sort_values(by='Age')
```

Descending: To sort in descending order, you add one argument to the syntax:

```python
Syntax = df_name.sort_values(by=col_name, ascending = False)
hr_df.sort_values(by = 'column name', ascending = False)
```

<!-- ### Viewing vs. Changing the DF -->
It's important to note that 'sort_values()' does not CHANGE the data. Everything we have learned so far are different ways to VIEW the data and not manipulate it.