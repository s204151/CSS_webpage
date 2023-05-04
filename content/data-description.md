---
title: Data description
prev: "/"
next: network-analysis
---

The dataset that has been used for this project is named StackSample. It contains 10% of stack overflows questions, answers and tags data. 

> The datasets are found on the website: https://www.kaggle.com/datasets/stackoverflow/stacksample

The dataset is downloaded and 3 csv files is received:
* ## [Questions](explainer-notebook.html)
* ## [Answers](explainer-notebook.html)
* ## [Tags](explainer-notebook.html)

There is only need for the Question and Answer files for this project.

The first dataset Question.csv is made of 1.249.762 rows x 7 columns. Each row represents a record of the question while each column represents a field name to the question. The field names are Id, OwnerUserId, CreationDate, ClosedDate, Score, Title, Body. An example is shown in the picture below:

<img src="/images/Question.png" width="600" />

The other dataset Answer.csv is made of 2.001.316 rows x 6 columns. It is structured the same way as the Question.csv, but there is only 6 field names. The field names are Id, OwnerUserId, CreationDate, ParentId, Score, Body. An example is shown in the picture below:

<img src="/images/Answer.png" width="600" />

The datasets are made into subsets of questions only from 2009 and answers to only those questions. This is done to reduce the cost of time and requests needed to the API.
The data has also been cleaned from missing values.
That means the new datasets are:
* ## [Subset_Questions](explainer-notebook.html)
* ## [Subset_Answers](subset_answers.csv)
 
These new datasets contains 31088 questions and 82497 answers. 

These are the datasets used in this project, where there is 30133 of unique users. 

## [Explainer Notebook](explainer-notebook.html)
