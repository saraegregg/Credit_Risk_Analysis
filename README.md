# Module 17 Challenge

---
## Credit Risk Analysis 
---

## Project Overview
Build and evaluate several machine learning models to detirmine which model best predicts credit risk. I oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I use an ensamble approach by applying the SMOTEENN algorithm. Finally, I compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, while predicting credit risk. 

## Challenge Objectives
Produce the following:
Deliverable 1: Resampling Models to Predict Credit Risk
Deliverable 2: The SMOTEENN Algorithm to Predict Credit Risk
Deliverable 3: Ensemble Classifiers to Predict Credit Risk
Deliverable 4: A Written Report on the Analysis (README.md)

## Resources
**Data Sources:** 
- LoanStats_2019Q1.csv

**Software:**
- Python 3.9.7
- Visual Studio Code 1.63.2 
- Anaconda Navigator 1.9.0
- Jupyter Notebook 6.4.5
- scikit-learn libraries
-imbalanced-learn libraries

## Results
### Size of the Data Set
How many Vine reviews and non-Vine reviews were in the data set?
- Total Number of Vine Reviews <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/total_paid_reviews.png"> 
</p>

<br>

- Total Number of Non-Vine Reviews <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/total_unpaid_reviews.png"> 
</p>
<br>

### 5-Star Reviews
How many Vine reviews were 5-stars? How many non-Vine reviews were 5 stars?
- Total Number of Vine Reviews That Awarded 5 Stars <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/fivestar_paid_reviews.png"> 
</p>

<br>

- Total Number of Non-Vine Reviews That Awarded 5 Stars <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/fivestar_unpaid_reviews.png"> 
</p>
<br>

### 5-Star Review Percents
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
- Percentage of Vine Reviews That Awarded 5 Stars <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/percentage_paid_fivestar_reviews.png"> 
</p>

<br>

- Percentage Non-Vine Reviews That Awarded 5 Stars <p align="center">
    <img src="https://github.com/saraegregg/Mod16_BigData/blob/main/images/percentage_unpaid_fivestar_reviews.png"> 
</p>
<br>

## Summary
45.6% of the reviews in the Vine program gave 5 stars and the percentage of non-Vine reviews giving 5 stars is slightly higher at 49.3%. These precentages do not provide any evidence to support a positivity bias for the reviews in the Vine program despite the compensation given to the participants, since the numbers are so similar. It could potentially indicate that reviewers participating in the Vine program are more thourough and critical when writing their reviews. The Vine reviews only constitute 0.8% of the overall reviews within the dataset, so further analysis is recommended.

An additional analysis to perform could be of the percentages of paid and unpaid 5-star reviews for lawn and garden products that have less than 20 votes. It is possible that Amazon Vine Members review these items that other shoppers may not be aware of or are willing to risk buying, unsure if the product is what they need or want. This new dataset could increase the number of total Vine reviews, creating a larger data pool to examine how Vine members review products




Accuracy is defined as the percentage of correct predictions (True Positive = True Negative/True Positive+ True Negative+ False Positive + False Negative)

Precision is defined as the perentage of positive predictions that are correct(True Positive/(True Positive + False Positive)). It is the measure of how reliable the positive classification is.

Sensitivity(Recall) is defined as the percentage of true positive predictions that are correct (True Positive/(True Positive + False Negative)). It is the measure of the number of observations with a positive classification will be correctly diagnosed.

F1 Score is defined as the harmonic mean that balances the precision and sensitivity F1 = 2(precision * sensitivity)/ (precision + sensitivity)

The analysis show that the precision for the high-risk loans were low for all of the models. The sensitivity(recall) for the high-risk loans was different among all of the models. In some cases it was either the model was overfitted or underfitted.

The ClusterCentroid was an example where the high-risk loans underfitted, there is a huge spread in the sensitivity between high and low-risk loans and will have poor results as it does have the correct results or new data cannot be analyed by the model as features are not selected appropriately and only 54% was the balanced accuracy.

Naive Random OverSampling and SMOTEENN models was an example where the high-risk loans were overfitted, it is a possibility that some results or new data may not be picked up in the model. The machine memorized the algorithms, it appears there were more true negatives in the array, and only 66%, and 64% balanced accuracy, respectively.

Recommendation
Easy Ensemble Ada Boost Classifier model had the best accuracy of 93.17% which means the algorithm was just right as well as the sensitivity between high and low-risk loans. The spread was minimal, the F1 Score was also the highest. The bias in this model was also reduced, so all data existing and new was analyzed, which had a better result or outcome.