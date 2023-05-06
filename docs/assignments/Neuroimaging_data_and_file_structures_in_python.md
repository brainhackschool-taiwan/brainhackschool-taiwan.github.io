---
layout: default
title: Neuroimaging data and file structures in Python - Exercise
parent: Modules
nav_exclude: true
---

# Neuroimaging data and file structures in Python - Exercise

## Description:

- This exercise is a copy from [Brainkhack School](https://school-brainhack.github.io/modules/nibabel/), but have small adaptation and change the recipient.

## Instructions:

- Follow the steps on [Brainhack School](https://school-brainhack.github.io/modules/nibabel/) to install required package and download the data and notebook files. Then open the notebook files with jupyter notebook.
- Watch the video and read through the `Nibabel.py`. You only to learn the basic contents to complete the excercise, some advanced contents (from 1:14:17 to 1:34:38) are optional and you can skip.
- After the tutorial, you should open a separate notebook and complete the following exercises:
  - Use the nilearn library function fetch_atlas_difumo to get the 64 parcellation image. As we learned in the video, the data in this image is just a number array and you can maniputate it with numpy. Please extract the 16th region, binarize it, and save it as a new nifti image.
  - Use the slicer object to view the new nifti file we created in the three different views.
  - Bonus: in 200 words, describe the conceptual differences between array and array proxy images.

## Submission:
- You should have one notebook file containing the code for the exercise, or you can write your code on colab.
- Please send an email to brainhackschooltaiwan@gmail.com with the subject title `[BHSTW] <Your_Student_ID> Neuroimaging data and file structures in Python` (e.g., `[BHSTW] B05202021 Neuroimaging data and file structures in Python`), and include the associated notebook file or colab link.
- Attempts: no limits.
- Points: 0.5 points for each question.