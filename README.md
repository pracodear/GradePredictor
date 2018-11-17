# Student Performance Prediction #

## Objective ##

A model that would predict whether or not a student would fail the math course that was being tracked. 

## Process ##

The target value is `G3`, which, according to the accompanying paper of the dataset, can be binned into a passing or failing classification. If `G3` is greater than or equal to 10, then the student passes. Otherwise, she fails. Likewise, the `G1` and `G2` features are binned in the same manner.

The data can be reduced to 4 fundamental features, in order of importance:
1. `G2` score
2. `G1` score
3. `School`
4. `Absences`

When no grade knowledge is known, `School` and `Absences` capture most of the predictive basis. As grade knowledge becomes available, `G1` and `G2` scores alone are enough to achieve over 90% accuracy. I experimentally discovered that the model performs best when it uses only 2 features at a time for each experiment.

The model is a linear support vector machine with a regularization factor of 100. This model performed the best when compared to other models, such as naive bayes, logistic regression, and random forest classifiers.

