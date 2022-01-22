# Credit_Risk_Analysis

## Background
Jill commends you for all your hard work. Piece by piece, you’ve been building up your skills in data preparation, statistical reasoning, and machine learning. You are now ready to apply machine learning to solve a real-world challenge: credit card risk.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, you’ll need to employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, you’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, you’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, you’ll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Once you’re done, you’ll evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Overview
**_Explain the purpose of this analysis. _**

The analysis purpose is to develop and show machine learning models in order to predict credit risk, using following methods for every procedure required: 

* Data Oversample using **RandomOverSampler** and **SMOTE** algorithms.
* Data Undersample using **ClusterCentroids** algorithm.
* Over- and undersampling through combinatorial approach using **SMOTEENN** algorithm.
* Machine learning models comparation to bias reduction, using **BalancedRandomForestClassifier** and **EasyEnsembleClassifier.**

Through each method, we Will evaluate the performance of models in order to perform a recommendation based in the accuracy scores, confusion matrix and classification reports. 

## Resources

**_list resources used_**

* **Data Source: ** LoanStats_2019Q1.csv
* **Software: ** Jupyter Notebook 6.3.0, MELNV (python environment)

## Results

**_Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results. _**

### Credit Risk Resampling

   #### Naive Random Oversampling
   * **Accuracy Score: ** 66.2%
   * **Precision High Risk: ** 1%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 72%
   * **Recall Low Risk:** 60%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)

   ####  SMOTE Oversampling
   * **Accuracy Score:** 65.6 %
   * **Precision High Risk:** 1%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 61%
   * **Recall Low Risk:** 70%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)
   
      ####  Cluster Centroid Undersampling
   * **Accuracy Score:** 54.4 %
   * **Precision High Risk:** 1%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 69%
   * **Recall Low Risk:** 40%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)
   
      ####  SMOTEENN Sampling
   * **Accuracy Score:** 54.4 %
   * **Precision High Risk:** 1%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 78%
   * **Recall Low Risk:** 57%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)

### Credit Risk ensemble

      ####  Balanced Random Forest Classifier
   * **Accuracy Score:** 78.8%
   * **Precision High Risk:** 3%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 70%
   * **Recall Low Risk:** 87%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)
  
       ####  Easy Ensemble AdaBoost Classifier
   * **Accuracy Score:** 93.1
   * **Precision High Risk:** 9%
   * **Precision Low Risk:** 100%
   * **Recall High Risk:** 92%
   * **Recall Low Risk:** 94%

   ![](https://github.com/JulioAQuintana/PyBer_Analysis/blob/main/analysis/PyBer_fare_summary.png)


## Summary

**_Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning._**

The Analysis want to get the best model to detect if a loan has high risk or not, due that, is required to find a model that give us the least amount of high-risk loan pass, that is procured by recall rate for high risk, due that we have to look into next model with highest scores:

1. Easy Ensemble AdaBoost Classifier (92%)
2. SMOTEENN Sampling (78%)
3. Naive Random Oversampling (72%)

The Easy Ensemble Classifying model shows a recall of 92% so it detects almost all high-risk credit. in the other side, we also got low precision in credit with high risk, that looks like a not good credit strategy for the bank's due to possible penalizations and missed revenues, in order to maintain healthy finances, I would not recommend the bank to use any of these models to predict credit risk.

