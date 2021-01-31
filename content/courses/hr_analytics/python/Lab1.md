---
title: Lab 1
linktitle: Lab 1
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  hr_analytics:
    parent: Getting Started
    weight: 21

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

# Jupyter Tutorial
Mariah Norell  
Last updated: 4/6/2020  

Purpose: To provide a tutorial for new users to learn how to format text, add cells, write simple code and view outputs.

## 1. Overview
Jupyter allows you to combine both text elements and Python code elements. With Jupyter, you can have both nicely formatted text for things like notes and instructions, as well as Python code itself. What you're reading right now is an example of a text element. In Jupyter, we call these text elements **markdown**. 

It is often helpful to alternate between writing markdown and writing code. For example, you might use markdown to write some notes about the code you're about to include, and then write the code itself. Below that, you might use markdown again to make notes, followed by more code. Each of these different bits of markdown or code is called a **cell**. Whenever you want to add a new cell, you'll need to tell Jupyter whether it should be a markdown cell or a code cell. 

In this tutorial, you'll learn how to create new cells of each type, and you'll also gain practice writing markdown and code.

## 2. Creating new cells
Let's practice creating a new cell. First, single click on the text in this cell. Then, using the menu choices above, select `Insert -> Insert cell below`. This will insert a new cell below this one.

Once the new cell is created, make sure it is "editable" by clicking on it -- you should see that it's now highlighted by a green rectangle. Then, use the dropdown menu above that currently says `Code`, and change it to `Markdown`. Type a short sentence of your choosing into the cell. Once you've typed your sentence, continue on to the next section below. 

Hi, this is Mariah!

### Shortcuts
Now, let's try creating a new cell below the sentence that you just typed, except we'll use a keyboard shortcut this time. The cell in which you just typed your equation should be highlighted with a green box. This means that the cell is editable. Click outside of the cell, and now you should see that it's blue. That means that it's "active" (i.e., selected), but not in edit mode, and that you're ready to use some keyboard shortcuts.

Thankfully, this is really easy! Simply hit the "b" key. This is short for "below", and means that you'll insert a new cell below the one that is currently active (outlined in blue). Click on the new cell so that it's in "edit" mode (green), and type a simple math equation, like 2 + 2.

Now let's learn the short cut for inserting a cell above the currently active cell. First, we'll need to click outside of the cell with our simple math equation so that it turns blue. Hit the "a" key, which stands for "above". Click the cell so that it's editable, and then change the cell type to markdown and type another simple sentence of your choosing.

Now, continue on to section 3 below.


```python
2+2
```




    4



## 3. Practice with markdown cells
In this section, we'll learn how to change font size, make things bold or italic, create bulleted lists, and include links.

### 3a. Changing font size (headings)
In markdown, instead of talking about font size like we would in Word (e.g., font size 10 or 12), we talk about headings. Heading 1 would have the largest font size, heading 2 would be smaller, and so on. The number of `#` symbols indicates the heading number. So, a single `#` symbol means heading 1, two `#` symbols means heading 2, and so on.  

In the cell below, I've written some text formatted as heading 1 and heading 2; your job is to create new text formatted as heading 3 and heading 4. To edit the cell below, simply double click on it. You'll see the text change blue, and you'll also be able to see the `#` symbols. Once you're done writing your text, use the following keyboard shortcut to "run" the cell, so that you can see the nice formatting: `Shift + Enter`

# Hello, this is heading 1
## And this is heading 2 

You can also write in "regular" sized font, like in this cell, simply by *not* including any `#` symbols. In the cell below, practice creating some text formatted as heading 2, followed by a new line of "regular" sized font. To edit the cell below, first click on it, and then change the cell type to markdown. Once you're done typing your practice text, run the cell using the `Shift + Enter` keyboard shortcut.


```python

```

### 3b. Bold and italic
To make a word **bold**, surround it on both sides with two asterisks. To make a word *italic*, surround it on both sides with a single asterisk. To understand what this formatting looks like, double click on this cell. Once you understand, run this cell to return to the nicely formatted view.

Next, use the empty cell below to practice making words bold and italic. Remember to change the cell type to markdown! Once you're done typing, run the cell.



## 4. Practice with code cells
In this portion of this tutorial, we'll learn how to write code by using Python as a calculator. No need to know how to program in Python just yet! In the cell below, I've included a simple calculation. Click on the cell, and run it -- you should see the output immediately below it.


```python
2 + 2
```




    4



In the empty cell below, try writing your own simple calculation, and then run the cell to ensure that you get the expected answer. If you're curious, you can use the `*` symbol for multiplication and the `/` symbol for division.


```python
34567890 * 34567
```




    1194908253630



Next, it's important to note that code cells can also contain something called **comments**, which are lines of text that are *not* evaluated as code. Comments are used to write brief notes about specific lines of code, and are precded by the `#` symbol. In the example below I've included a comment and some code. Run the cell to see what happens.


```python
# This is a comment: Subtract 5 from 10
10 - 5
```




    5



As you can see, the calculation in the *comment* wasn't actually run -- only the calculation in the code itself. In the empty cell below, try writing a comment and a simple calculation underneath it.


```python

```

Finally, you might be wondering when to write notes using markdown, and when to write notes using comments within a code cell. A good rule of thumb is that if you want to write longer, nicely formatted notes, you should use markdown. If you want to write a very brief note (i.e., less than a sentence) that refers to a specific line of code, use a comment. As you start to learn how to program in Python, this distinction will become more clear.

## 5. Documenting your notebooks
You'll note that, at the top of this notebook, I've included the following information:

* Title of the notebook
* My name 
* The date that I last updated the notebook
* The purpose of the notebook

It is standard practice, both in the classroom and in the work place, to include this documentation in all of your notebooks!
