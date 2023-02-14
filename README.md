# Capstone - Insurance Claims Classification

## Motivation

## Goal

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
c
