---
title: DataFrames
linktitle: DataFrames
toc: true
type: docs
draft: false
menu:
  hr_analytics:
    parent: Python
    weight: 20

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 5
---

In this tutorial, I'll share how to view subsets and sort DataFrames:

## Indexing with Numbers

Indexing means we want to select a specific row/column in a dataframe
```
hr_df[“Age”]
```

Let’s say we want to see the 4th value in the “Education” column

To do that, use the following syntax: 
```
df.column_name[n]
```
Remember how we talked about the data starting at “0” instead of “1”? Keep that in mind when we say we want a value! 
For example, if we want the “4th” value, that means we use “3” in our code

How does that look with our data?

```
In_[1]: hr_df.Education[3]
Out[1]: 'Master'
```


Let’s try with whole rows or columns
Syntax = iloc

```
# a:b = row slice
# c:d = column slice
Syntax: df_name.iloc[a:b, c:d]
```

#### What is slicing?

Think of it like chunking up the data into smaller pieces

We start the index at “a” and stop before “b”

Viewing Rows and Columns
Want to see all the rows or all the columns? Simply place the colon in the brackets without any numbers!

```
# : = all rows
# 0:1 = one column slice
df_name.iloc[:, 0:1]
```

```
# 0:1 = one row slice
# : = all rows
df_name.iloc[:, 0:1]
```


How does it look with some data?
We are interested in looking at
Employee ID
Age
Attrition

For Employee IDs:
 #2, 3, 4, 5, 6, 7, 8, & 9

How do we start going about this?

What row/column #s are of interest?

Let's practice!


## Indexing with Booleans

We just learned how to sort our data by selecting the appropriate numbers for the rows and columns 

But what if you don’t know exactly what to look for? 

Large DataFrame

The dataframe could be so large we don’t know what column to search for

Instead we can search through something called a “Boolean expression”


We can search within a specific column to return a specific row

Example: 
Let's serach the "MaritalStatus" column

Let's return data for the row(s) containing "Divorced"

#### Boolean Expression Indexing
An example of the syntax structure: 

```
# df_name[df_name.col_name[operator][value]]
example = df_name[df_name.MaritalStatus == 1]
```

We can use the same general syntax to find data that meets some criteria. Essentially just need to choose:- An operator (e.g., <, <=, >, >=, ==, !=) – A value (a string or number).

Return data from the df that: 
- matches a string like "female"

Obtain greater than or less than a value:
- Job Satisfaction score over 3

Represents a minimum or maximum age value:
- Lowest age in the dataset

## Sorting Data

Ascending:
When you sort your data by a particular column, the default is to sort in ascending order

For example, we could sort our data by the Age column

```
Syntax = df_name.sort_values(by=col_name)
example = df_name.sort_values(by="Age")
```

Descending:
To sort in descending order, you add one argument to the syntax 

```
Syntax = df_name.sort_values(by=col_name, ascending = False)
hr_df.sort_values(by = “column name”, ascending = False)
```

Viewing vs. Changing the DF
It's very important to note that "sort_values()" does not CHANGE the data. Everything we have learned so far are different ways to VIEW the data and not manipulate it.