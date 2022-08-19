# Credit Risk Classification

This is the challenge project for UW Fintech 2022 Module 12.

---

# Credit Risk Classification Report

## Background

Credit risk poses a classification problem that’s inherently imbalanced because the number of healthy loans easily outnumber the number of risky loans. This credit risk classification uses various techniques to train and evaluate models with imbalanced classes to better identify the creditworthiness of borrowers.

For both cases, you’ll get the count of the target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Overview of the Analysis

* The purpose of this analysis is to train a machine learning model to help predict risky loans.
* The financial data used to train the model included: loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, total debt, and loan status (healthy vs risky).
* By training on the financial data, the model will try preduct whether a loan's status is healthy or risky (see: 'targets.value_counts()')
* To accomplish this we complete the following stages of the machine learning (ML) process:
** First, split the original data into two sets: one for training the ML model, one for testing the ML model. Note the original data includes "loan_status", which is the value we want to predict.
** Second, create a model and train it with the data set aside for training.
** Third, use the test data to predict the outcome, and then evalute the accuracy, precision, etc. of the model by comparing the predicted outcome against the test outcome.
* The two primary methods used to classify credit risk are: Logistic Regression model (as it's good at predicting discrete outcomes) and RandomOverSampler from the imbalenced-learn library (to improve the predictive capability for riskier loans for which we have less data).

## Results

* Logistic Regression Model results
  * Accuracy: ~95%
  * Precision: 100% for healthy loans, ~85% for high-risk loans
  * Recall: 99% for healthy loans, 91% for high-risk loans
  
* Resampled Logistic Regression model results
  * Accuracy: ~99%
  * Precision: 100% for healthy loans, ~84% for high-risk loans
  * Recall: 99% for healthy loans, 99% for high-risk loans
  
## Summary

* From the results it's clear the Resampled Logistic Regression model performs best. While the precision for prediciting high-risk loans is slightly decreased against the non-resampled model, this is the better model to us as it has a higher overall accuracy, and a near-perfect recall for high-risk loans. 
* Performance in predicting high-risk loans is important as this is what we want to predict with the highest confidence. The vast majority of loans are healthy, so we want to ensure we most accurately identify potentially high-risk loans to make the best decision before loaning money.

---

## Technologies

The stable version of this project can be run on Windows, Mac OS, or Linux as long as the user's 
environment has the following:
- python 3.7
- numpy
- pandas
- pathlib
- sklearn.metrics
- imblearn.metrics
- jupyter lab

---

## Installation Guide

You have a few options to install this application on your computer, two popular options are:

1. Download a ZIP of this repositories files 
[here](url-to-zip)
     example: (https://github.com/Warp-9000/challenge-12-credit-risk-classification/archive/refs/heads/main.zip).

2. [Fork this respository](https://docs.github.com/en/get-started/quickstart/fork-a-repo "Fork a Repo - 
GitHub Docs") to your github account.

<p align="center">
<img src="https://github.com/Warp-9000/uw-fintech-2022-module01-challenge/blob/main/instructions/github-fork-button-screenshot.png?raw=true" 
alt="Fork UI on GitHub.com"
width="55%"/>
</p>

After forking the respository you can use `git clone 
your-username@domain.com:your-git-username/challenge-12-credit-risk-classification.git` 
to download a copy of the forked respository to your computer.

Forking has the added benefit of enabling your to easily keep your copy of the 
application up-to-date should any changes or improvements be made in the future.

---

## Usage

***Please note:*** *these usage instructions assume you have setup an environment where
the python version, libraries, and frameworks listed in [Technologies](#Technologies) are installed.*

1. Navigate to the root folder of your repository.
2. Run the application by (1) launching jupyter lab, and (2) running the credit_risk_resampling.ipynb file.

---

## Contributors

Thanks!

<a href="https://github.com/Warp-9000/challenge-12-credit-risk-classification/graphs/contributors">
<img src="https://contrib.rocks/image?repo=Warp-9000/challenge-12-credit-risk-classification" />
</a>

---

## License

This project is licensed under ... Please see the LICENSE file 
[here](https://github.com/Warp-9000/uw-fintech-2022/blob/main/Module-02/Challenge/loan_qualifier_app/LICENSE).
