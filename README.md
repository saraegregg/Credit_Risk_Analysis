# Module 17 Challenge

---
## Credit Risk Analysis 
---

## Project Overview
Build and evaluate several machine learning models to detirmine which model best predicts credit risk. I oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I use an ensamble approach by applying the SMOTEENN algorithm. Finally, I compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, while predicting credit risk. 

## Challenge Objectives
Produce the following:
- Deliverable 1: Resampling Models to Predict Credit Risk
- Deliverable 2: The SMOTEENN Algorithm to Predict Credit Risk
- Deliverable 3: Ensemble Classifiers to Predict Credit Risk
- Deliverable 4: A Written Report on the Analysis (README.md)

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

There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models


### MODEL 1 Oversampling-RandomOverSampler
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/naiverandom_accscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/naiverandom_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.01 and the sensitivity is 0.72.

### MODEL 2 Oversampling-SMOTE
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/smote_accuscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/smote_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.01 and the sensitivity is 0.62.

### MODEL 3 Undersampling-ClusterCentroids
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/undersampling_accscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/undersampling_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.01 and the sensitivity is 0.69.

### MODEL 4 Combinatorial-SMOTEEN
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/combo_accscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/combo_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.01 and the sensitivity is 0.77.

### MODEL 5 Ensamble-BalancedRandomForestClassifier
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/fandomforest_accscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/fandomforest_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.03 and the sensitivity is 0.70.

### MODEL 6 Ensamble-EasyEnsambleClassifier
**Accuracy Score** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/easyensamble_accscore.png"> 
</p>

<br>

**Classification Report** of the model <p align="center">
    <img src="https://github.com/saraegregg/Mod17_Credit_Risk_Analysis/blob/main/images/easyensamble_report.png"> 
</p>
<br>
The classification report shows that the precision score for identifying high-risk loans is 0.09 and the sensitivity is 0.92.

## Summary

Keeping in mind that the goal is to identify high risk loan applications to protect the financial institution offering the credit, the goal is to find the model that is optimized for sensitivity. A false positive, or a good loan application flagged as possibly defaulting is more acceptable to the bank than false negatives, or a likely-to-default loan application not being detected. The financial institution can then inspect the flagged applications for additional layers of screening before determining whether or not to approve the requested loan. 

The model with the highest sensitivity, the EasyEnsambleClassifier, has a recall of 92%. This is far more sensitive than any of the other models. However, it has a very low precision score of 0.09, which means that many of the low risk credit applications are flagged as high-risk. A consequence of this model's use would be the bank missing the opportunity to earn revenue on those low risk loans if it is the only metric used to detirmine whether or not the financial institution approves a loan application.