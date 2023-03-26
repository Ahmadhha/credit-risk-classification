# Project Title: CryptoClustering

# Description: 

Training and evaluating a loan risk predicting machine learning model.

# Scope: 

Evaluating the perfomance of a supervised machine learning logistic regression model with and without random over sampling to detect the health of a loan.

View Data: [csv source](https://github.com/Ahmadhha/credit-risk-classification/blob/main/Resources/lending_data.csv)

View Code: [jupyter notebook](https://github.com/Ahmadhha/credit-risk-classification/blob/main/credit_risk_classification.ipynb)

# Report:

### Overview of the Analysis

* Purpose of Analysis: To predict the risk of a loan based on financial information related to the loan and borrower.
* Financial Information: 
  - Load: Size, interest rate.
  - Borrower: Income, dept, number of accounts, deragotary marks, total debt.
* Prediction: The risk of the loan defaulting. 
* Training Data: Total data points: 77,536, Healthy Loans: 75,036, High Risk Loans: 2500
* Stages of Machine Learning: 
  - Data Preparation: Read data, Separate Labels and Features, Split Training and Test data, Resample Training data using RandomOverSampler (second model only)
  - Machine Learning Model Preparation: Create instance of a logistic regression model, fit the training data to the model, predict the outcome using test data
  - Model Evaluation: Create confusion matrix and classification reports to evaluate model performance.
* Logistic Regression: Supervised machine learning model used for classification tasks, where the goal is to predict a binary outcome Uses a logistic function to transform a linear combination of input variables into a probability of belonging to one of the two classes.
* RandomOverSampler: A module from imblearn that increases the number of samples in the minority class by randomly replicating existing samples to balance class distribution.

### Results

#### Machine Learning Model 1:
* Accuracy: The classification model correctly predicted 94.4% of the samples, considering both the minority and majority class, taking into account the class imbalance of the dataset.
* Confusion matrix:
   - 18,679 out of 18,759 healthy loans or true negatives correctly predicted
   - 80 out of 18,759 false positives
   - 558 out of 625 high risk loans or true positives correctly predicted
   - 67 out of 625 false negatives
* Classification Report:
   - Precision: Majority of healthy loans predicted are correct, 87% of high risk loans predicted are correct.
   - Recall: Majority of actual healthy loans were correctly predicted, 89% of actual high risk loans were predicted as high risk.

#### Machine Learning Model 2:
* Accuracy: The classification model correctly predicted 99.6% of the samples, considering both the minority and majority class, taking into account the class imbalance of the dataset.
* Confusion matrix:
   - 18,668 out of 18,759 healthy loans or true negatives correctly predicted
   - 91 out of 18,759 false positives
   - 623 out of 625 high risk loans or true positives correctly predicted
   - 2 out of 625 false negatives
* Classification Report:
   - Precision: Majority of healthy loans predicted are correct, 87% of high risk loans predicted are correct.
   - Recall: Majority of actual healthy loans were correctly predicted, Majority of actual high risk loans were predicted as high risk.


### Summary

In summary, the chance that the first model identifies an actual healthy loan as high risk is minor, however, the chance that the it predicts a high risk loan as healthy is approximately 11%.

The first model is better in at predicting healthy loans, compared to its ability to predict high risk loans, and is more likely to give a false negative (miss a high risk identification) than it is to give a false positive (wrongly identify a healthy loan as high risk).

It is not recommended to use this model, since it poses a relateively high risk for missing out on detecting high risk loans.

For the second model, the chance that the it incorrectly identifies an actual healthy loan as high risk or a high risk loan as healthy are both minor, less than 0.5% of the time.

The second model performs similar to the un-sampled previous version in predicting healthy loans, however, it significantly improved in terms of predicting un-healthy loans, and the chances that it wrongly identifies a loan is similar for each category and relatively minor.

It is recommended to use this second model (which improves accuracy using over sample) since it shows a very minor chance of missing out on a identifying a high risk loan.
