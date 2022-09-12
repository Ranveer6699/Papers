## Summary
The paper describes the use of boosted regression trees trained on the EHR medical data to predict cardiac arrest in children in CICU . Since the algorithm uses the Anytime framework, the cardinality of the decision trees increases as new data is received.

The data collected for the model consists of EHR from 48 hours to the hour of cardiac arrest. Moreover, the data collected was discretized into bins using kmeans to accommodate data from children of different age groups. Finally, the data collected is converted into predicate logic to allow the model to work on symbols instead of features, . Once the data is collected, Statistical Relational Learning is used to create models for cardiac arrest. The model uses weakly generated regression trees to get the probability of the target getting cardiac arrest. Since the model uses an anytime framework, regression trees trained on the new data are concatenated to our current trees at each interval. The predicates added to the regression trees maximize the weighted variance.

The model is compared to the ones where the regression trees are learned from scratch at each stage. the model which uses concatenation performs better than the ones trained from scratch from all the data collected so far. The authors theorize that the better result may be because data collected only few hours before the cardiac arrest may be more relevant to the data on hand.

## Positive Points
1. The model described in the paper is much more data efficient than typical neural networks
2. The lack of hyperparameters makes it easy to tune the model when compared to parameterized models
3. The model, with its use of predicate logic, forgoes the need for missing data

## Negative Points
1. Since Cardiac Arrest can be life thereatening, a cost matrix which heavily penalizes a false negative should have been used.

## Extensions
1. To extract the causal graphs from the regression trees created for any possible dependencies between vitals and risk of CA.
2. It might be possible to use logical implementations of other sequential learning methods like LSTMs to better learen the data
