In this project, I take a look at call center data.

Goals: 
1. Build a model that achieves >81% accuracy in predicting whether a customer will invest.
2. Identify the most meaningful features for the ML model.
3. Perform customer segmentation.

The final model uses a random forest classifier and achieves an accuracy of 99%, which can be compared to the baseline accuracy of 93% (when choosing "0" every time for this highly imbalanced dataset).
The f1 scores or the "0" and "1" classes are both 0.99. All true positives were found in the test dataset, with a small number of false positives being recorded. No false negatives were found.

The most important feature in the predictive model by far is the duration of the last call with the customer. This may not be causal (i.e., just keep them on the phone and they'll invest!), but rather may simply reflect the length of time in answering the customers' questions prior to their investing or taking down their information as part of an application process.

Customer segmentation...

