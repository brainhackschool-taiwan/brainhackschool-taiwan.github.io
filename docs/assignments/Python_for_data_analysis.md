---
layout: default
title: Python for data analysis - Exercise
parent: Modules
nav_exclude: true
---

# Python for data analysis - Exercise

## Description:

- Most of this exercise is identical to that of [BrainHack School 2022](https://school.brainhackmtl.org/modules/python_data_analysis/). The purpose of this assignment is to ensure that you're equipped with the basic skills to analyze data in Python.

## Instructions:

- Open a Jupyter notebook, and import the following
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.datasets import load_iris
# optional magic command
%matplotlib inline
```
- Load the dataset with `iris = load_iris()`
- Explore the dataset using `.keys()`
- Print the shape and type of the `'data'`
- Declare two variables that store `'data'` and `'feature_names'` 
- Create a pandas dataframe with `'data'` and use `'feature_names'` for the column names
- Get the summary statistics of this dataframe using `.describe()`
- Subset the dataframe to keep only the first 50 rows
- Check if there are any extreme sepal length values (extreme value criterion: less or greater than 3.9 standard diviations away from the mean)
- What about the other three features? Define a function that checks for extreme values for each of the features.
- *Optional: Usually boxplots (see below) treat as "outliers" those values that are outside of 1.5 times the interquartile range. You can try to define a function that checks for boxplot outliers too.*
- Check out how to plot boxplots at [matplotlib](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.boxplot.html)
- Boxplot the distribution of the features. **Please do add labels for the axes**
- Save the dataframe as a csv file and the boxplot as a png file

## Assignment Submission:

- Head to Google Collaboratory and upload your Jupyter notebook onto Google Colab. Name the `ipynb` file as `Python for data analysis`. Click Share at the top right of the window, **add brainhackschooltaiwan@gmail.com as an Editor (we must be added, otherwise your email will fail to be uploaded to our Google Drive system)**, and copy the link. An example of a "toy" Google colab notebook is at this link https://colab.research.google.com/drive/132VeOFToryeLkZaWVFLikShG1ECxaGDn?usp=share_link
- Send an email with the subject title `[BHSTW] <Your_Student_ID> Python for data analysis` (e.g., `[BHSTW] B05202021 Python for data analysis`) to brainhackschooltaiwan@gmail.com, where the student ID should have all English letters capitalized, and the module name should be precisely the same as the example, with only the first letter of the first word capitalized. The link to your Colab notebook should be pasted in the email body.
- You will receive an email reply titled `Receipt of submission` about 30 minutes after your submission email has been sent. This email will notify you whether your files have been successfully uploaded.
- Please contact `Amanda Lin #5919` on Discord if your submission email keeps failing.

## Grading:

- Your assignment will be graded on a three-point scale: 0, 0.5, 1. 
- If most of your code works well with very few bugs and you've done all the steps listed in Instructions, a full mark of 1 will be given. If you missed some steps or it seems your code produces lots of errors, one of the TAs will contact you on Discord and walk you through the exercise. A full mark of 1 will also be given as long as you complete the exercise in the end. If, however, we fail to contact you, a partial credit mark of 0.5 will be given. In the case where we don't receive an email from you or you send us a blank Colab notebook and go MIA (missing in action)... Sorry, that's a 0! 
