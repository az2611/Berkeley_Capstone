# Capstone - Insurance Claims Classification

## Motivation  

Claims processing in insurance refers to the procedures and activities involved in receiving, verifying, and resolving claims filed by policyholders. This process typically includes reviewing the claim details, assessing coverage, investigating the circumstances surrounding the claim, and determining the amount of compensation to be paid.  
Claims classification is a common task in claims processing, in this process claims are clasified by hand, in this case claims classification automation represents a unique opportunity to create efficiencies.

## Goal
The goal of this project is to propose an alternative to claims classification using machine learning.

## Data
The data set for this project consist of +2300 claims in 9 categories. Data was labeled manually and is part of a research project aimed to better understand claims data.

|Class|Description|label|
|---|---|---|
|Auto-related|233|233|
|Damage|192|192|
|Fell|509|509|
|Fire|44|44|
|Flood|62|62|
|Injury|842|842|
|Occupational disease/illness|146|146|
|Pollution|62|62|
|Water|157|157|

## Approach  

In order to identify the best alternative for Claims Classification a Pipeline and GridSearchCV were created to try different combinations of vectorizers with different estimators. 

The estimators evaluated are:

* Logistic Regression
* Decision Tree 
* Naive Bayes

Text preprocessing: Data pre-processing includes performing both stemming and lemmatizing to normalize the text before classifying. For each technique it was used both the CountVectorizer and TfidifVectorizer, options for stop words and max features to prepare the text.

Additionally, Claims Classification was perfomed using the BERT (Bidirectional Encoder Representations from Transformers) a popular deep learning model for natural language processing. It is a pre-trained language model that can be fine-tuned on specific downstream tasks using additional labeled data.

## Preliminary Results

By comparing model performance in terms of accuracy and speed we can see that Logistic Regression provides an accuracy score on 0.8637.
  
|Model|Stemming|Vectorizer|Best Max Features|Best Stop Words|Score|Time|
|---|---|---|---|---|---|---|
|LogisticRegression\_l2|PorterStemmer\(\)|cvect|500||0\.8637037037037038|12\.37|
|LogisticRegression\_l2|WordNetLemmatizer\(\)|cvect|500||0\.8548148148148148|16\.09|
|LogisticRegression\_l2|WordNetLemmatizer\(\)|tdif|500||0\.837037037037037|16\.62|
|DecisionTree|PorterStemmer\(\)|cvect|2000||0\.8355555555555556|2\.04|
|LogisticRegression\_l2|PorterStemmer\(\)|tdif|500||0\.8340740740740741|12\.5|
|DecisionTree|WordNetLemmatizer\(\)|tdif|1000||0\.8192592592592592|2\.92|
|DecisionTree|WordNetLemmatizer\(\)|cvect|3000||0\.8148148148148148|3\.22|
|DecisionTree|PorterStemmer\(\)|tdif|500||0\.8118518518518518|2\.75|
|NaiveBayes|WordNetLemmatizer\(\)|cvect|500|english|0\.8|1\.22|
|NaiveBayes|PorterStemmer\(\)|cvect|500||0\.797037037037037|1\.22|
|NaiveBayes|WordNetLemmatizer\(\)|tdif|500|english|0\.7822222222222223|1\.34|
|NaiveBayes|PorterStemmer\(\)|tdif|100|english|0\.7762962962962963|1\.31|
  
### BERT
Accuracy: 0.912396694214876  
f1 score: 0.9109060191176175
