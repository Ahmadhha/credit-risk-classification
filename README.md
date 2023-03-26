# Project Title: CryptoClustering

# Description: 

Training and evaluating a loan risk predicting machine learning model.

# Scope: 

Evaluating the perfomance of a supervised machine learning logistic regression model with and without random over sampling to detect the health of a loan.

View Data: [csv source](https://github.com/Ahmadhha/credit-risk-classification/blob/main/Resources/lending_data.csv)

View Code: [jupyter notebook](https://github.com/Ahmadhha/credit-risk-classification/blob/main/credit_risk_classification.ipynb)

View Report: [summary Report](https://github.com/Ahmadhha/credit-risk-classification/blob/main/report-template.md)

# Conclusion:

The chance that the first model identifies an actual healthy loan as high risk is minor, however, the chance that the it predicts a high risk loan as healthy is approximately 11%.

The first model is better in at predicting healthy loans, compared to its ability to predict high risk loans, and is more likely to give a false negative (miss a high risk identification) than it is to give a false positive (wrongly identify a healthy loan as high risk).

It is not recommended to use this model, since it poses a relateively high risk for missing out on detecting high risk loans.

For the second model, the chance that the it incorrectly identifies an actual healthy loan as high risk or a high risk loan as healthy are both minor, less than 0.5% of the time.

The second model performs similar to the un-sampled previous version in predicting healthy loans, however, it significantly improved in terms of predicting un-healthy loans, and the chances that it wrongly identifies a loan is similar for each category and relatively minor.

It is recommended to use this second model (which improves accuracy using over sample) since it shows a very minor chance of missing out on a identifying a high risk loan.
