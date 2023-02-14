# Capstone - Insurance Claims Classification

## Motivation  

Claims processing in insurance refers to the procedures and activities involved in receiving, verifying, and resolving claims filed by policyholders. This process typically includes reviewing the claim details, assessing coverage, investigating the circumstances surrounding the claim, and determining the amount of compensation to be paid.  
Claims classification is a common task in claims processing, in this process claims are clasified by hand, in this case claims classification automation represents a unique opportunity to create efficiencies.

## Goal
The goal of this project is to propose an alternative to claims classification using machine learning.

## Data
The data set for this project consist of +2300 claims in 

|Class|Description|label|
|---|---|---|
|Damage|192|192|
|Fell|509|509|
|Fire|44|44|
|Flood|62|62|
|Injury|842|842|
|Occupational disease/illness|146|146|
|Pollution|62|62|
|Water|157|157|


## Approach

## Preliminary Results

c  
  
|Model|Stemming|Vectorizer|Best Max Features|Best Stop Words|Score|Time|
|---|---|---|---|---|---|---|
|LogisticRegression\_l2|WordNetLemmatizer\(\)|cvect|1000||0\.8892561983471075|8\.88|
|LogisticRegression\_l2|PorterStemmer\(\)|cvect|2000||0\.8859504132231405|27\.86|
|LogisticRegression\_l2|PorterStemmer\(\)|tdif|500||0\.8611570247933884|11\.7|
|LogisticRegression\_l2|WordNetLemmatizer\(\)|tdif|500||0\.859504132231405|8\.23|
|DecisionTree|PorterStemmer\(\)|tdif|4000||0\.8479338842975207|2\.37|
|NaiveBayes|WordNetLemmatizer\(\)|cvect|500||0\.8462809917355372|1\.26|
|NaiveBayes|PorterStemmer\(\)|cvect|500||0\.8429752066115702|1\.2|
|DecisionTree|PorterStemmer\(\)|cvect|3000||0\.8314049586776859|1\.76|
|DecisionTree|WordNetLemmatizer\(\)|tdif|500||0\.8297520661157025|3\.18|
|DecisionTree|WordNetLemmatizer\(\)|cvect|3000||0\.8231404958677686|3\.09|
|NaiveBayes|WordNetLemmatizer\(\)|tdif|100||0\.7950413223140496|1\.32|
|NaiveBayes|PorterStemmer\(\)|tdif|500|english|0\.7917355371900826|1\.31|
  
### BERT
Accuracy: 0.912396694214876
f1 score: 0.9109060191176175
