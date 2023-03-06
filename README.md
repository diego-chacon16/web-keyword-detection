# Keyword Detection on Websites

## Objective 
+ Create an algorithm, that takes html page as input and infers if the page contains the information about cancer tumorboard or not

## Data Description

#### Files:

+ train.csv contains next columns: url, doc_id and label
+ test.csv contains next columns: url and doc_id
+ htmls contains files with names {doc_id}.html
+ keyword2tumor_type.csv contains useful keywords for types of tumorboards

#### Description of tumor board labels:

+ 1 (no evidence): tumor boards are not mentioned on the page
+ 2 (medium confidence): tumor boards are mentioned, but the page is not completely dedicated to tumor board description
+ 3 (high confidence): page is completely dedicated to the description of tumor board types and dates

You are asked to prepare a model using htmls, referred to in train.csv, and make predictions for htmls from test.csv




