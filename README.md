In this project, I take a look at call center data.

Goals: 
1. Build a model that achieves >81% accuracy in predicting whether a customer will invest.
2. Identify the most meaningful features for the ML model.
3. Perform customer segmentation.

-----

The final model uses a Light Gradient Boosting Machine and achieves an accuracy of 91%, which can be compared to the baseline accuracy of 93% (when choosing "0" every time for this highly imbalanced dataset).

The advantage of the LGBM over a DummyClassifier stems not from accuracy, but from precision and recall.

The f1 scores for the "0" and "1" classes are 95% and 54%, respectively, with a macro average of 75%. 

69% of the true positives were found in the test dataset.

The most important feature (based on SHapely Additive exPlainations) by far is the duration of the last call with the customer. This may not be causal (i.e., just keep them on the phone and they'll invest...), but rather may reflect the length of time in answering the customers' questions prior to their investing or taking down their information as part of an application process. Without knowing this, our final model includes the feature. When the duration is excluded, the model suffers considerably.

Investors can be segmented into 6 groups, which we did using Agglomerative Clustering:

The first segment consists largely of single individuals in their upper 20s to lower 40s that have completed high school. They tend to have lower paying jobs (administrative, blue collar, service) and many have a low balance.

Divorced people form the 2nd segment. They are almost evenly split between secondary and tertiary education, are equally distributed among ages over 30 years, and about half of them are managers and half are admin/blue collar types.

The next group are single people in their upper 20s to mid 30s who have completed some form of higher education and hold management positions at their workplace. They tend to have positive to high balances.

The last 3 groups are mostly married people. The main differences are education (cluster4: primary, cluster5: secondary, cluster6: tertiary), age (cluster4 is older), and job (cluster6 is comprised of managers).



7rpqBYJQxTWdDeeI
