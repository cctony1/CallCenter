In this project, I take a look at call center data.

Goals: 
1. Build a model that achieves >81% accuracy in predicting whether a customer will invest.
2. Identify the most meaningful features for the ML model.
3. Perform customer segmentation.

-----

The final model uses a Light Gradient Boosting Machine and achieves an accuracy of 92%, which can be compared to the baseline accuracy of 93% (when choosing "0" every time for this highly imbalanced dataset).

The advantage of the LGBM over a DummyClassifier stems not from accuracy, but from precision and recall.

The f1 scores for the "0" and "1" classes are 0.96 and 0.54, respectively, with a macro average of 0.75. 

Two-thirds of the true positives were found in the test dataset.

The most important feature (based on SHapely Additive exPlainations) by far is the duration of the last call with the customer. This may not be causal (i.e., just keep them on the phone and they'll invest...), but rather may reflect the length of time in answering the customers' questions prior to their investing or taking down their information as part of an application process. We did not build and test a model without this feature.

Investors can be segmented into 4 groups:

1. Single people in their 20s or 30s with secondary education, having administrative or blue-collar jobs and a lower (than other segments) balance,

2. Single or married people in their upper 20s to 40s with tertiary education, who are in management roles and who have higher balances, on average, than the first segment,

3. Married individuals ranging from 25 to 60 years old, having secondary education, who are in blue-collar or administrative jobs, or retired,

4. Divorced individuals between 25 and 55 years, with secondary or tertiary education and holding administrative or management positions.



7rpqBYJQxTWdDeeI
