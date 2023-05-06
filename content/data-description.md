---
title: Data description
prev: "/"
next: network-analysis
---

The dataset that has been used for this project is named StackSample. It contains 10% of stack overflows questions, answers and tags data. 

> The datasets are found on the website: https://www.kaggle.com/datasets/stackoverflow/stacksample

> All the datasets used in this project can be downloaded from here: https://drive.google.com/drive/folders/1RdU0mMRiBL9uTIWgPd8ZTfrs3qKUc8qB?usp=sharing

The files that can be downloaded from the website are:
* Questions.csv - 1.79 Gb
* Answers.csv - 1.5 Gb
* Tags.csv - 65 Mb

There is only need for the Questions and Answers files for this project.

The first dataset Questions.csv is made of 1.249.762 rows x 7 columns. Each row represents a record of the question while each column represents a field name to the question. The field names are Id, OwnerUserId, CreationDate, ClosedDate, Score, Title, Body. An example is shown in the picture below:

<img src="/images/Question.png" width="600" />

The other dataset Answers.csv is made of 2.001.316 rows x 6 columns. It is structured the same way as the Question.csv, but there is only 6 field names. The field names are Id, OwnerUserId, CreationDate, ParentId, Score, Body. An example is shown in the picture below:

<img src="/images/Answer.png" width="600" />

The datasets are made into subsets of questions only from 2009 and answers to only those questions. This is to reduce the cost of time and requests needed to the API.
The data has also been cleaned from missing values.
That makes the new datasets:
* subset_questions.csv - 49.8 Mb
* subset_answers.csv - 86. 6 Mb
 
These new datasets contains 31088 questions and 82497 answers. 

The new datasets are what is used in this project, where there is 30133 of unique users. 