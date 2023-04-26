# Keyword Detection on Websites - Guided Project

## Objective 
+ Create an algorithm, that takes html page as input and infers if the page contains the information about cancer tumorboard or not

## What is a tumor board?
+ Tumor Board is a consilium of doctors (usually from different disciplines) discussing cancer cases in their departments

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

Prepare a model using the train.csv and make predictions on the test.csv

## Practicalities

+ How to handle this large amount of data?
A: Using data generators to load the samples disk. The amount of data itself was relatively small.
+ What decisions were made for feature engineering and why?
A: Most of the efforts were spent pre-processing the data. Steps like removing punctuation, multiple white spaces, numbers, etc.
+ What models were used? Why did I choose to use those models?
A: The strategy was to used Siamese Networks. They are popular for this type of task (smaller data set, imbalanced classes)
+ How were the results validated?
A: The validation of the results was handled by Tensorflow. The validation data (20% of the dataset) was passed through it to validate the results.
+ What potential opportunities do you see with your algorithm?
A: Given the fact it is a small dataset with a class imbalance, we should be weary of overfitting
A: There is 0 precision and recall on label 3 which is concerning, and needs to be addressed
