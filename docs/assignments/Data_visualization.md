---
layout: default
title: Data visualization - Exercise
parent: Modules
nav_exclude: true
---

# Data visualization - Exercise

## Description:

- This exercise is a copy from [BrainHack School](https://school.brainhackmtl.org/modules/python_visualization/).
- The purpose of this assignment is to ensure that you've become familiarized with basics of plotting in python with some of most commonly used packages, which will come in handy when you're working on your own projects!

## Instructions:

- Please complete the following three exercises in a Google Colaboratory notebook title `<your_name>_data_visualized`.
- This exercise uses a version of the phenotypic data from [ABIDE](http://fcon_1000.projects.nitrc.org/indi/abide/abide_II.html). To download the dataset, click on the link and then click "Kennedy Krieger Institute" on the right-hand side. Then, Downloads -> Phenotypic File. You will need an NITRC account - if you don't have one, you can create one from [NITRC](https://www.nitrc.org/account/register.php).

- Exercise 1 Create a figure with a single axes and replot the second scatterplot to group by sex instead of dx_group.
```
   Set the figure size to a ratio of 8 (wide) x 5 (height)
   Use the colors red and gray
   Set the opacity of the points to 0.5
   Label the axes
   Add a legend
```
- Exercise 2 Using a pairwise plot, compare the distributions of age, viq, and piq with respect to dx_group.
```
    Set a palette
    Set style to ticks
    Set context to paper
    Suppress the dx_group variable from being on the plot
```
- Exercise 3 Using a violin plot separate out viq as a function of sex and dx_group.
```
    Different dx_group should be on each half of each violin
    The x-axis should reflect the different sex categories.
```

## Assignment Submission:

- This exercise should be submitted via a Google Colab notebook link. 
- To share your Colab notebook, simply click on the SHARE button at the top right to get a shareable link. You can select either the commenter or editor option in order for the TAs to grade your work.
- After it's all set, please send an email with the subject title `[bshtw] <Your_Student_ID> Data visualization` (e.g., `[bshtw] B05202021 Data visualization`) to brainhackschooltaiwan@gmail.com, where the student ID should have all English letters capitalized, and the module name should be precisely the same as the example, with only the first letter of the first word capitalized. The link to your Colab notebook should be pasted in the email body.
- You will receive an email reply titled `Receipt of submission` about 30 minutes after your submission email has been sent. This email will notify you whether your files have been successfully uploaded.
- Please contact `Amanda Lin #5919` or `Ki#1892` on Discord if your submission email keeps failing.

## Grading:

- Your assignment will be graded on a three-point scale: 0, 0.5, 1. 
- If you successfully submit your code with very few bugs, a point of 1 will be given, indicating a full mark. If, however, we find that your code doesn't work well enough, one of the TAs will contact you via Discord. Feel free to let us know if you ran into any trouble with the assignment. We'll walk you through the code and, in which case, a full mark of 1 will also be given as long as the code works fine in the end — no worries! A partial credit mark of 0.5 is given in the case where your code produces too many errors and yet we also fail to contact you. A mark of 0 is given, if we don't receive an email from you or you send us a blank notebook.
