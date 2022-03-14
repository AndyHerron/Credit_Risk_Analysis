# Credit Risk Analysis

## Overview of analysis
Using machine learning, we were asked to analyse credit risk using several different methods to try to predict which loans might default.
Credit risk is an inherently unbalanced classification problem because good loans vastly outnumber bad loans.

### Resources
* Data Sources: 'LoanStats_2019Q1.csv' from LendingClub.com
* Software: Jupyter Notebook, Python, machine learning algorithms sklearn, imblearn

## GitHub has disabled LFS for my account due to the fact that I have exceeded my data storage limit. 
### I have added "*.csv" to my .gitignore file, so my datafiles are not uploaded to my GitHub page.

## Methods used in the analysis
- imbalanced-learn and scikit-learn libraries
- Oversampling methods
	- RandomOverSampler
	- SMOTE
- Undersampling methods
	- ClusterCentroids
- Combination (over and under) sampling
	- SMOTEENN
- Ensemble classifiers
	- BalancedRandomForestClassifier
	- EasyEnsembleClassifier


## data tables in pgAdmin
Customers table
![customers_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_customers_table.png)

Products table
![products_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_products_table.png)

Review ID table
![review_id_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_review_id_table.png)

Vine table
![vine_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_vine_table.png)

## Results
---
Customers table
![customers_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_customers_table.png)

Products table
![products_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_products_table.png)

Review ID table
![review_id_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_review_id_table.png)

Vine table
![vine_table](https://github.com/AndyHerron/Amazon_Vine_Analysis/blob/main/resources/pgAdmin_vine_table.png)

## Summary 
There is a positive effect of Vine reviews within the dataset. When looking at the subset of data with 20 or more votes and more than 50% helpful reviews,
the products with Vine reviews had a higher percentage of 5 star reviews.  The percentage of 5 star reviews for non-Vine reviewed products is essentially the same as the percentage
of the helpful reviews at just a bit over 46%.  (46.33% and 46.43% respectively) The products with Vine reviews get 5 star reviews 57.2% of the time.

As an additional analysis, I also calculated the number of 5 star reviews for the raw data.  63.98% of the reviews were 5 stars.  There could be many factors as to why this percentage is
higher than the percentages in our subset of data.  It's possible that many of those reviews were not considered helpful by other reviewers.  It's also likely that people who are happy
with the product are more likely to take the time to provide a review.  5 star reviews that did not receive at least 20 votes may indicate that other users didn't have quite the same experience (even if they also
left a 5 star review.) 

=======
	Predicted True	Predicted False
Actually True	TRUE POSITIVE	FALSE NEGATIVE
Actually False	FALSE POSITIVE	TRUE NEGATIVE
Precision = TP/(TP + FP)
Sensitivity is a measure of how many people who actually have cancer were correctly diagnosed.
Highly sensitive tests and algorithms tend to be aggressive, as they do a good job of detecting the intended targets, but also risk resulting in a number of false positives. High precision, on the other hand, is usually the result of a conservative process, so that predicted positives are likely true positives; but a number of other true positives may not be predicted. In practice, there is a trade-off between sensitivity and precision that requires a balancing act between the two.


