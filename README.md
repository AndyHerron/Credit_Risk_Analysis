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


## Results of the machine learning predictions
Target value count
![Target value count](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/Target%20value%20counts.png)

RandomOverSampler
![RandomOverSampler](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/Random%20Oversampling.png)

SMOTE
![SMOTE](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/SMOTE%20Oversampling.png)

Cluster Centroids
![Cluster Centroids](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/Cluster%20Centroids%20Undersampling.png)

SMOTEEN
![SMOTEEN](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/SMOTEENN%20combination%20sampling.png)

BalancedRandomForestClassifier
![BalancedRandomForestClassifier](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/BRFC%20results.png)

EasyEnsembleClassifier
![EasyEnsembleClassifier](https://github.com/AndyHerron/Credit_Risk_Analysis/blob/main/screenshots/EEC%20results.png)

##Summary 

The goal of this exercise is to find a model that helps predict which loans might default (become bad loans.)  The short answer is that none of
these methods are very good at that.  The ensemble classifiers are better than the over - or undersampling methods.  The Easy Ensemble Classifier method is the 
best out of the six, but it's still not good.  It only correctly predicts high risk loans 0.07% of the time - and that's the best of the bunch. 
It predicted 979 false positives, while correctly predicting 79 true positives. That's not good.  
If I was a loan officer and was in charge of finding a method to help predict bad loans, I would keep looking for a better solution than any of these options.
I would look for a solution that had higher precision and lower sensitivity.

	Predicted True	Predicted False 
Actually True	TRUE POSITIVE	FALSE NEGATIVE 
Actually False	FALSE POSITIVE	TRUE NEGATIVE 

Precision = TP/(TP + FP)
Sensitivity is a measure of how many loans which actually are bad were correctly predicted.
Highly sensitive tests and algorithms tend to be aggressive, as they do a good job of detecting the intended targets, 
but also risk resulting in a number of false positives. High precision, on the other hand, is usually the result of a 
conservative process, so that predicted positives are likely true positives; but a number of other true positives may not be predicted. 
In practice, there is a trade-off between sensitivity and precision that requires a balancing act between the two.


