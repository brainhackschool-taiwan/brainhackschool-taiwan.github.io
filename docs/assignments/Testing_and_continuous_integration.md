---
layout: default
title: Testing and continuous integration - Exercise
parent: Modules
nav_exclude: true
---

# Testing and continuous integration - Exercise

## Description:

- This exercise is a copy from [Brainkhack School](https://school-brainhack.github.io/modules/testing/).
- Follow the instruction and submit your assignment to TAs.

## Instructions:

- Watch the video until 55:23.
- Fork this [repo](https://github.com/FrancoisPgm/intro2testing).
- On your fork in github, go to the Actions tab and create a new workflow.
- Modify the action template created by github to :
	- Change the workflow name from “build” to “test”
	- add the following step to setup python :

```
# Set up python to be able to run python scripts
- name: Set up Python
  uses: actions/setup-python@v1
  with:
 	python-version: 3.7
```

  - add the following step to install the dependancies :

```
# Pip install the required packages
- name: Install Dependencies
  run: pip install -r requirements.txt
```

  - Run the test script :

```
# Run the test script
- name: Run test
  run: |
    cd code
    bash test.sh
```

- commit and push this new file to create and run the action.
- go back to the action tab on your repo, you should see an action called “test”.
- verify that the action did run the test, the first one should be passed and the second should fail, so you should be able to see something like that :

![](https://school.brainhackmtl.org/modules/testing/example_action.png)

- Screenshot the whole page, including your username and repository name at top. This is the evidence that you completed this moulde

## Submission:

- You should have a picture file (`*.jpg`, `*.png`, ... etc).
- Please send an email to brainhackschooltaiwan@gmail.com with the subject title `[BHSTW] <Your_Student_ID> Testing and continuous integration` (e.g., `[BHSTW] B05202021 Testing and continuous integration`) 
- Attempts: no limits
- Points: 0 (fail) / 1 (pass)
