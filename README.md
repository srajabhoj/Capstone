Capstone Project Understanding
==============================

This project is about classifying fraudulent credit card transactions,
to help customers as well as companies to avoid loss.

Given dataset contains of transactions made by credit cards in September
2013 by European cardholders. Dataset has transactions of 2 days. Out of
284,807 transactions only 497 transactions are fraudulent transaction.

It means there is some mechanism already in place to detect frauds but,
existing mechanism is not being able to detect this 492 frauds before
transaction. Our job here to identify correct model and train it to
detect these 492 frauds as well. Same time model should not over fit or
under fit.

As per data, we can say data is highly imbalanced it needs to be treat
before we do modelling or come to the final conclusion. We can treat by
under-sampling or oversampling. Well under-sampling results into data
loss we will use here oversampling. There are multiple techniques of
oversampling like

1.  Uniform over sampling

2.  Random oversampling

3.  SMOTE

4.  ADASYN

We will use SMOTE and ADASYN and test the data and finalize one of them
for further process.

We have been provided only principal components of features instead of
actual data. It has been done due confidentiality issues. This condition
restricts us to study features we can only analyse it for
classification, we cannot recommend anything here.

The only feature those are not PCA transformed are amount and time.

> Time - the seconds elapsed between each transaction and the first
> transaction in the dataset.
>
> Amount - the transaction Amount, this feature can be used for
> example-dependant cost-sensitive learning.

**Class** - the response variable and it takes value 1 in case of fraud
and 0 otherwise.

Here as the data is PCA transformed we will get most of Principal
Components are normally distributed, but many of features are suffered
from skewness. We need to treat skewness here. For skewness we can use
any of following algorithms

1.  Box-cox transform

2.  Yeo-Johnson transformation

3.  Power transformation

4.  Quantile transformation

As **Power transformation** take cares of outliers as well we will use
it for Skewness treatment.

After data preparation we will run model over it, as we have to test 4-5
models we will use following models for initial testing

1.  Logistic regression

2.  Decision trees

3.  K-nearest neighbour

4.  Random forest

And we will choose best performing model for further process.

So here are the decided steps we wish to go with:

1.  Data Preparation (treat skewness)

2.  Oversample the data

3.  Split train test data

4.  Run models

5.  Tune hyper parameters

6.  Choose best model and second best model for further testing.

7.  Evaluate model on test data using AUC curve

8.  Check Sensitivity and Specificity

Once done publish the results.

Target to achieve is identify maximum of 497 frauds without decreasing
specificity i.e. overfitting the model.
